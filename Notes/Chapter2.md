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
- One of the benefits of Tailwind is that when you add or delete an element, you no longer need to worry about maintaining a seperate style sheets, style collisions, or the size of your CSS bundle. This benefit scales as the program scales as well.

- create-next-app will ask during the setup process if you want to use Tailwind. Selecting yes, enables the project to be setup and configured for Tailwind use.

- /app/pages.tsx shows an example of the Tailwind classes in use for this tutorial

# CSS Modules 

- [CSS_Modules](https://nextjs.org/docs/basic-features/built-in-css-support) allow one to scope CSS to a component by automatically creating unique class, names so you dont have to worry about style collision. 

- The same styling previously added could be done with a CSS Module instead of Tailwind styling.

- One of the benefits of CSS modules is they provide a way to make CSS classes locally scoped to components by default, reducing the risk of styling conflicts. 


