## Next.js App Router Course - Starter

### Why I'm using Tailwind for style?

Tailwind is a CSS framework (frameworks lower drastically the threshold for personal opinions and bias when writing the code base 🥳) that speeds up the development process by allowing you to quickly write utility classes directly in your TSX markup. Although the CSS styles are shared globally (`37.73 kB`), each class is singularly applied to each element. This means if you add or delete an element, you don't have to worry about maintaining separate stylesheets, style collisions, or the size of your CSS bundle growing as your application scales:

```tsx
<h1 className="text-blue-500">I'm blue!</h1>
```

The main directives are collected into `/app/ui/global.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Tailwind and CSS modules are the two most common ways of styling Next.js applications. Whether you use one or the other is a matter of preference - you can even use both in the same application!

### Why I'm using the `clsx` library to toggle class names

There may be cases where you may need to conditionally style an element based on state or some other condition. `clsx`
is a library that lets you toggle class names easily:

```tsx
import clsx from 'clsx';

export default function InvoiceStatus({ status }: { status: string }) {
  return (
    <span
      className={clsx(
        'inline-flex items-center rounded-full px-2 py-1 text-sm',
        {
          'bg-gray-100 text-gray-500': status === 'pending',
          'bg-green-500 text-white': status === 'paid',
        },
      )}
    >
)}
```
