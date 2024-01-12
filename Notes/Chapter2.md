# CSS Styling

# Global Styles

- Inside of /app/ui there is a global.css file. This file enables adding rules to all routes in the app

- Though you can import the global.css  within any component, the best practice is to import at the top-level component.

- Typical Next.js app will use the RootLayout as the top-level component. 

- Once done importing, there was a noticeable difference in the page layout. This styling came from the global.css file, specifically the @tailwind directives.