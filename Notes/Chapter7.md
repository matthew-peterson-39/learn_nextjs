# Fetching Data

# Choosing How to Fetch Data

## API Layer

- 3rd party service provider of API

- If youre fetching data from the client, you want ot hav an API layer that runs on the server to avoid exposing your databse secrets to the client.

## Database Queries

- When creating API endpoiints, you neeed to write logic to interact with your databse.

- If you are using react server components (fetching data on the server), you can skip the API layer and query your databse directly without risking exposing your database secrets to the client. 

- Q: When should you not query your databse directly?
- A: When you're fetching data on the client

# Using SQL

- For this project, I will use database quesries using vercel postgres SDK and sql.

- The reason for this is that SQL is industry standard for relational databses.

- Strengthening my knowledge of SQL will thus strengthen my fundamental knowledge of which many frameowkrs are built.

- SQL is versatile alllowing both fetching and manipulating of data

- The Vercel Postgres SDK provides protection against SQL injections.

- To enable the querying of the database, an import function defined in /app/lib/data.ts named sql. can be used within any server component. 

# Fetch Data for Dashboard Overview Page

# Using Server Components to Fetch Data

- By default, Next.js use React Server Components. This is a relatively new approach but comes with the following benefits:

1. Server components support promises, providing a simpler solution for asynchronous tasks like data fetching. It allows you to use async/await syntax without reaching out for useEffect, useState or data fetching libraries.

2. Server Components execute on the server, so you can keep expensive data fetches and logic on the server and only send the result to the client.

3. Since they execute on the server, you can query the databse directly without an additional API layer.

- Q: What is one advantage of using React Server Components to fetch data?
- A: They allow you to query the databse directly from the server without an additional API layer.

# What are request waterfalls?

- A "waterfall" refers to a sequence of network requests that depend on the completion of previous requests. In the case of data fetching, each request can only begin once the previous request has returned data.

- Though this pattern is not necessarily bad, there are cases where you want waterfalls because you want a condition to be satisifed before you make the next request.

- For example, you might want to fetch a user's ID and profile information first. Once you have the ID, you then proceeed to fetch their list of frients. This is a clear example of how one request is relient on the data returned from the previous request.

- However, when not done intentionally, a waterfall can impact performance

# Paralle Data Fetching

- To combat waterfalls, one can request data at the same time in parallel.

- In JavaScript one can use Promise.all() or Promise.allSettled() to initiate the promises at the same time.

- The downside of this technique is seen when one data request is slower than the others.

