# Navigating between Pages

# Why Optimize Navigation?

- Using the typical \<a> element to link pages renders a full page refresh each time.

- The \<Link> component lets you link between pages in the application using client side navigation.

# Automatic code-splitting and prefetching

- Next.js auto code splits applications by route segement. This differs from the tradtional React [SPA](https://developer.mozilla.org/en-US/docs/Glossary/SPA) where the browswer loads all your application code on the initial load.

- Additionally, in production, whenever <Link> components appear in the borwswers viewport, Next.js auto prefetches the code for the linked route in the background. Making page transitions near-instant.

# Common UI Pattern - Showing Active Links

- A common UI pattern is to show an active link so the user knows what page they are currently on.

- This can be done using the hook usePathname()

- To enable hooks to be used in the nav-links.tsx component, a "use client" directive must be added to the top of the file , followed by importing the usePathname() hook from next/navigation

