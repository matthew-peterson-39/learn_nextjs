# Streaming
- Streaming helps to improve the UX when there are slow data requests.

# What is streaming?

- It is a data transfer technique that allows you to break down a route into smaller "chunks" and progressible stream them from the server to the client as the are ready.

- Streaming prevents slow data requests from blocking the whole page. Letting the user interact with parts of the page without waiting for all the data to load before any UI can be shown to the user.

- Streaming works will with react, as each component can be considered a "chunk"

- One can implement streaming in Next.js at the page level using loading.tsx file and also for specific components with \<Suspense>

# Streaming a While Page with loading.tsx

- loading.tsx is a special Next.js file that is built ontop of Suspsense, allowing one to create a fallback UI to show as ar eplacement while page content loads

- Because the SideNav is static, it is shown immediately. The user can interact with the navbar while the dynamic content is laoding

- The user can navigate away prior to the page loading. Known as interruptable navigation.

# Adding Loading Skeletons

- A loading skeleton is a simpleified version of the UI. This is often used as placeholders to indicte that the content is loading. ANy UI to embed into loading.tsx will be embedded as part of the static file, and sent first. Then the rest of the dynamic content will be streamed from the server to the client.

- Creating a new directory named (overview) makes it so the loading.tsx file will only apply to your dashboard.

- The route groups allow you to organize files into logical groups without affecting the URL path structure. WHen a new folder is created using the parentheses (), the name wont be included in the URL path. 

- In this case, /dashboard/(overview)/page.tsx becaomes /dashboard

- In sum, a route group is used to ensure loading.tsx only applies to the dashboard overpage. However, route groups can be used to separate an applications into sections (e.g (marketing) routes and (shop) routes) or by teams for larger applications.

# Streaming a Component

- Instead of streaming a whole page, a specific component can be streamed using React Suspense

- Suspense allows you to defer rendering parts of your applciation until some condition is met. (e.g. data is loaded). You can wrap your dynamic components in Suspense. Then, pass it a fallback component to show while the dynamic component loads.

# Grouping Components

- When adding streaming to the card component, wrapping each card in a suspense could lead to a popping effect as the cards load in which is not good UX design.

- To create a staggered effect, you can group the cards using a wrapper component.