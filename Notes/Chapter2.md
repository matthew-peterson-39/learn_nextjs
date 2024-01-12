# CSS Styling

# Global Styles

- Inside of /app/ui there is a global.css file. This file enables adding rules to all routes in the app

- Though you can import the global.css  within any component, the best practice is to import at the top-level component.

- Typical Next.js app will use the RootLayout as the top-level component. 

- Once done importing, there was a noticeable difference in the page layout. This styling came from the global.css file, specifically the @tailwind directives.

# Tailwind

- [Tailwind](https://tailwindcss.com/) is a CSS framework that speeds up the development by allowing quick writing of [utility-classes](https://tailwindcss.com/docs/utility-first) directly to a .tsx markup.

- tailwind styles elemets by adding classnames with instructional rulesets. Such as: 
```.tsx 
<h1 className="text-blue-500">I'm blue!</h1>
```



