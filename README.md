## Next.js App Router Course - Starter

### Why I'm using Tailwind for style?
Tailwind is a CSS framework (frameworks lower drastically the threshold for personal opinions and bias when writing the code base 🥳) that speeds up the development process by allowing you to quickly write utility classes directly in your TSX markup. Although the CSS styles are shared globally, each class is singularly applied to each element. This means if you add or delete an element, you don't have to worry about maintaining separate stylesheets, style collisions, or the size of your CSS bundle growing as your application scales:
```tsx
<h1 className="text-blue-500">I'm blue!</h1>
```
The main directives are collected into `/app/ui/global.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
