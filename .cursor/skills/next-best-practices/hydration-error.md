# Hydration Errors

Diagnose and fix React hydration mismatch errors.

## Error Signs

- "Hydration failed because the initial UI does not match"
- "Text content does not match server-rendered HTML"

## Debugging

In development, click the hydration error to see the server/client diff.

## Common Causes and Fixes

### Browser-only APIs

```tsx
// Bad: Causes mismatch - window doesn't exist on server
 {window.innerWidth} 

// Good: Use client component with mounted check
'use client'
import { useState, useEffect } from 'react'

export function ClientOnly({ children }: { children: React.ReactNode }) {
 const [mounted, setMounted] = useState(false)
 useEffect(() => setMounted(true), [])
 return mounted ? children : null
}
```

### Date/Time Rendering

Server and client may be in different timezones:

```tsx
// Bad: Causes mismatch
 {new Date().toLocaleString()} 

// Good: Render on client only
'use client'
const [time, setTime] = useState ()
useEffect(() => setTime(new Date().toLocaleString()), [])
```

### Random Values or IDs

```tsx
// Bad: Random values differ between server and client
 

// Good: Use useId hook
import { useId } from 'react'

function Input() {
 const id = useId()
 return 
}
```

### Invalid HTML Nesting

```tsx
// Bad: Invalid - div inside p
 Content 

// Bad: Invalid - p inside p
 Nested 

// Good: Valid nesting
 Content 
```

### Third-party Scripts

Scripts that modify DOM during hydration.

```tsx
// Good: Use next/script with afterInteractive
import Script from 'next/script'

export default function Page() {
 return (
 
 )
}
```
