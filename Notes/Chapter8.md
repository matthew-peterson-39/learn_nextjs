# Static and Dynamic Rendering

# What is Static Rendering?

- With static rendering, data fetching and rendering happens on the server at build time (when you deploy) or during [revalidation](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#revalidating-data). The result can then be distrubted and cached in a [Content_Deliver_Network](https://nextjs.org/docs/app/building-your-application/rendering/server-components#static-rendering-default).

- When a user visits the application, the cached result is served. The static rendering has benefits of:

1. Faster websites - prerendered content can be cached and globally distrubted. This allows users around the works to access the website more quickly and reliably.

2. Reduced server load - cached content allows the server to not have to dynamically generate content for each user request.

3. SEO - Search Engine Optimization - Prendered content is easier for search enginer crawlers to index, as the content is already availble when the page loads. Leading to improved search engine rankings.

- Static rendering is useful for UI with no data or data that is shared across users, such as a static blog post or a prouct page. It might not be a good fit for a dashboard that has personalized adata that is regularly updated.

- The opposite of static rendering is dynamic rendering.

# What is Dynamic Rendering?

- With dynami rendering, content is rendered on the server for each user at request time (when the user visits the page)

1. Real-Time Data : Dynamic rendering allows an application to display real-time or frequently updated data. This is ideal for appliaction where data changes often.

2. User-Specific Content : It's easier to serve personalized content, such as dashboards or user profiles, and update the data based on user interaction

3. Request Time Information : Dynamic rendering allows one to access information that can only be known at request time such as cookies or the URL search parameters.

# Making the Dashboard Dynamic

- By default @vercel/postgres doesnt set its own caching semantics. This allows the framework to set its own static and dynamic behavior

- You can use a Next.js API called unstable_noStore isnide your server components or data fetching functions to opt out of static rendering. Let's add this.
