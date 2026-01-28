# RSC Boundaries

Detect and prevent invalid patterns when crossing Server/Client component boundaries.

## Detection Rules

### 1. Async Client Components Are Invalid

Client components **cannot** be async functions. Only Server Components can be async.

**Detect:** File has `'use client'` AND component is `async function` or returns `Promise`

```tsx
// Bad: async client component
'use client'
export default async function UserProfile() {
 const user = await getUser() // Cannot await in client component
 return {user.name} 
}

// Good: Remove async, fetch data in parent server component
// page.tsx (server component - no 'use client')
export default async function Page() {
 const user = await getUser()
 return 
}

// UserProfile.tsx (client component)
'use client'
export function UserProfile({ user }: { user: User }) {
 return {user.name} 
}
```

```tsx
// Bad: async arrow function client component
'use client'
const Dashboard = async () => {
 const data = await fetchDashboard()
 return {data} 
}

// Good: Fetch in server component, pass data down
```

### 2. Non-Serializable Props to Client Components

Props passed from Server → Client must be JSON-serializable.

**Detect:** Server component passes these to a client component:
- Functions (except Server Actions with `'use server'`)
- `Date` objects
- `Map`, `Set`, `WeakMap`, `WeakSet`
- Class instances
- `Symbol` (unless globally registered)
- Circular references

```tsx
// Bad: Function prop
// page.tsx (server)
export default function Page() {
 const handleClick = () => console.log('clicked')
 return 
}

// Good: Define function inside client component
// ClientButton.tsx
'use client'
export function ClientButton() {
 const handleClick = () => console.log('clicked')
 return Click 
}
```

```tsx
// Bad: Date object (silently becomes string, then crashes)
// page.tsx (server)
export default async function Page() {
 const post = await getPost()
 return // Date object
}

// PostCard.tsx (client) - will crash on .getFullYear()
'use client'
export function PostCard({ createdAt }: { createdAt: Date }) {
 return {createdAt.getFullYear()} // Runtime error!
}

// Good: Serialize to string on server
// page.tsx (server)
export default async function Page() {
 const post = await getPost()
 return 
}

// PostCard.tsx (client)
'use client'
export function PostCard({ createdAt }: { createdAt: string }) {
 const date = new Date(createdAt)
 return {date.getFullYear()} 
}
```

```tsx
// Bad: Class instance
const user = new UserModel(data)
 // Methods will be stripped

// Good: Pass plain object
const user = await getUser()
 
```

```tsx
// Bad: Map/Set
 

// Good: Convert to array/object
 
 
```

### 3. Server Actions Are the Exception

Functions marked with `'use server'` CAN be passed to client components.

```tsx
// Valid: Server Action can be passed
// actions.ts
'use server'
export async function submitForm(formData: FormData) {
 // server-side logic
}

// page.tsx (server)
import { submitForm } from './actions'
export default function Page() {
 return // OK!
}

// ClientForm.tsx (client)
'use client'
export function ClientForm({ onSubmit }: { onSubmit: (data: FormData) => Promise }) {
 return... 
}
```

## Quick Reference

| Pattern | Valid? | Fix |
|---------|--------|-----|
| `'use client'` + `async function` | No | Fetch in server parent, pass data |
| Pass `() => {}` to client | No | Define in client or use server action |
| Pass `new Date()` to client | No | Use `.toISOString()` |
| Pass `new Map()` to client | No | Convert to object/array |
| Pass class instance to client | No | Pass plain object |
| Pass server action to client | Yes | - |
| Pass `string/number/boolean` | Yes | - |
| Pass plain object/array | Yes | - |
