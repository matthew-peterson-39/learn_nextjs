# Creating Lyaouts and Pages

# Nested Routing

- Next.js uses file-system routing. This approach uses folders to created nested routes. 

- Each folder respresnts a route segment that maps to a URL segment.

- You can create separate UIs for each route using layout.tsx and page.tsx files.

- page.tsx is a special NExt.js file that exports a React component and it is required for the route to be accessible.

- In this example app, the /app/page.tsx is the home page assosciated with the route '/'

- To create a nested route, you can nest folders inside each other and add page.tsx files inside of them.

# Creating the Dashboard Page

- one of the benefits of Next.js use of layouts is that only the page components update while the layout wont re-render. This term is coined [partial_rendering](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating#3-partial-rendering)

# Root Layout

- a root layout is required in Next.js any UI that is added to the root layout will be shared across all pages in the application. 

- The root layout can be use to modify the \<html> and \<body> tags and add meta data.

- However, since the layout was added to the /app/dashboard/layout.tsx, there is no need to add UI to the root layout.

-Q: What is the purpose of the layout file in Next.js? A: To share UI across multiple pages.

