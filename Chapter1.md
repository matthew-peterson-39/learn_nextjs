# How to Start Next Project:

- This command creates a new nextjs app using the latest version, with a name of nextjs-dashboard. It uses NPM and for this tutorial, it is using an --example flag to get the starting template to save time for the tutorial.

```bash 
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" 
```

# Folder Strucutre:

- /app - Contains all the routes, components and logic for app. Most of the work is done here.

- /app/lib - Contais functions used in app, ie. reuseable utility functions and data fetching

- /app/ui - Contains al the UI components for app, ie. cards, tables, and forms. These were presetyled for this tutorial for time saving.

- /public - contains all the static assests for your application, such as images.

- /scripts - contains a seeding script that you'll use to populate your database at a later point of the tutorial.

- Config Files - Most of the time, these files are preconfigured when running the create-next-app. These will not need modification for the tutorial.

# Placeholder Data

- Placeholder data is used as a placeholder for data that is not yet retrieved by, say a Database or API. A placeholder may be stored in JSON format, a JavaScript obejct, or a 3rd party service ie mockAPI.

- This tutorial provides an /app/lib/placeholder-data.js file.

# TypeScript

- TypeScript is used largley in modern web development. One of the many benefits of TypeScript is that it ensures you don't accidentally pass the wrong data format to your components or databse. IE. passing a string instead of a number to the invoice amount.

- Frameworks such as [Prisma](https://www.prisma.io/) automatically generate types based on a database schema. In this tutorial, the data types are manually declared.

- Next.js detects if your projects uses TypeSript and automatically installs the nexecssary packages and configuration. Next.js also comes with TypeScript [plugin](https://nextjs.org/docs/app/building-your-application/configuring/typescript#typescript-plugin) for your code editor.

# Running a Dev Server

- First install the packages using 
```bash
npm i
```

- Then,

```bash
npm run dev
```

- Next.js useses port 3000 for the development server.