# Image Optimization

Use `next/image` for automatic image optimization.

## Always Use next/image

```tsx
// Bad: Avoid native img
 

// Good: Use next/image
import Image from 'next/image'
 
```

## Required Props

Images need explicit dimensions to prevent layout shift:

```tsx
// Local images - dimensions inferred automatically
import heroImage from './hero.png'
 

// Remote images - must specify width/height
 

// Or use fill for parent-relative sizing
 
 
 
```

## Remote Images Configuration

Remote domains must be configured in `next.config.js`:

```js
// next.config.js
module.exports = {
 images: {
 remotePatterns: [
 {
 protocol: 'https',
 hostname: 'example.com',
 pathname: '/images/**',
 },
 {
 protocol: 'https',
 hostname: '*.cdn.com', // Wildcard subdomain
 },
 ],
 },
}
```

## Responsive Images

Use `sizes` to tell the browser which size to download:

```tsx
// Full-width hero
 

// Responsive grid (3 columns on desktop, 1 on mobile)
 

// Fixed sidebar image
 
```

## Blur Placeholder

Prevent layout shift with placeholders:

```tsx
// Local images - automatic blur hash
import heroImage from './hero.png'
 

// Remote images - provide blurDataURL
 

// Or use color placeholder
 
```

## Priority Loading

Use `priority` for above-the-fold images (LCP):

```tsx
// Hero image - loads immediately
 

// Below-fold images - lazy loaded by default (no priority needed)
 
```

## Common Mistakes

```tsx
// Bad: Missing sizes with fill - downloads largest image
 

// Good: Add sizes for proper responsive behavior
 

// Bad: Using width/height for aspect ratio only
 

// Good: Use actual display dimensions or fill with sizes
 

// Bad: Remote image without config
 
// Error: Invalid src prop, hostname not configured

// Good: Add hostname to next.config.js remotePatterns
```

## Static Export

When using `output: 'export'`, use `unoptimized` or custom loader:

```tsx
// Option 1: Disable optimization
 

// Option 2: Global config
// next.config.js
module.exports = {
 output: 'export',
 images: { unoptimized: true },
}

// Option 3: Custom loader (Cloudinary, Imgix, etc.)
const cloudinaryLoader = ({ src, width, quality }) => {
 return `https://res.cloudinary.com/demo/image/upload/w_${width},q_${quality || 75}/${src}`
}

 
```
