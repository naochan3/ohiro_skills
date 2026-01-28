# Scripts

Loading third-party scripts in Next.js.

## Use next/script

Always use `next/script` instead of native ` ` tags for better performance.

```tsx
// Bad: Native script tag
 

// Good: Next.js Script component
import Script from 'next/script'

 
```

## Inline Scripts Need ID

Inline scripts require an `id` attribute for Next.js to track them.

```tsx
// Bad: Missing id
 

// Good: Has id
 

// Good: Inline with id
 
 {`document.getElementById('banner').classList.remove('hidden')`}
 
```

## Don't Put Script in Head

`next/script` should not be placed inside `next/head`. It handles its own positioning.

```tsx
// Bad: Script inside Head
import Head from 'next/head'
import Script from 'next/script'

 
 
 

// Good: Script outside Head
 
 Page 
 
 
```

## Loading Strategies

```tsx
// afterInteractive (default) - Load after page is interactive
 

// lazyOnload - Load during idle time
 

// beforeInteractive - Load before page is interactive (use sparingly)
// Only works in app/layout.tsx or pages/_document.js
 

// worker - Load in web worker (experimental)
 
```

## Google Analytics

Use `@next/third-parties` instead of inline GA scripts.

```tsx
// Bad: Inline GA script
 
 
 {`window.dataLayer = window.dataLayer || [];
 function gtag(){dataLayer.push(arguments);}
 gtag('js', new Date());
 gtag('config', 'G-XXXXX');`}
 

// Good: Next.js component
import { GoogleAnalytics } from '@next/third-parties/google'

export default function Layout({ children }) {
 return (
 
 {children} 
 
 
 )
}
```

## Google Tag Manager

```tsx
import { GoogleTagManager } from '@next/third-parties/google'

export default function Layout({ children }) {
 return (
 
 
 {children} 
 
 )
}
```

## Other Third-Party Scripts

```tsx
// YouTube embed
import { YouTubeEmbed } from '@next/third-parties/google'

 

// Google Maps
import { GoogleMapsEmbed } from '@next/third-parties/google'

 
```

## Quick Reference

| Pattern | Issue | Fix |
|---------|-------|-----|
| ` ` | No optimization | Use `next/script` |
| ` ` without id | Can't track inline scripts | Add `id` attribute |
| ` ` inside ` ` | Wrong placement | Move outside Head |
| Inline GA/GTM scripts | No optimization | Use `@next/third-parties` |
| `strategy="beforeInteractive"` outside layout | Won't work | Only use in root layout |
