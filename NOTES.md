How to Start Next Project:

- This command creates a new nextjs app using the latest version, with a name of nextjs-dashboard. It uses NPM and for this tutorial, it is using an --example flag to get the starting template to save time for the tutorial.

```bash 
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" 
```

Folder Strucutre:

- /app - Contains all the routes, components and logic for app. Most of the work is done here.

- /app/lib - Contais functions used in app, ie. reuseable utility functions and data fetching

- /app/ui - Contains al the UI components for app, ie. cards, tables, and forms. These were presetyled for this tutorial for time saving.

- /public - contains all the static assests for your application, such as images.

- /scripts - contains a seeding script that you'll use to populate your database at a later point of the tutorial.

- Config Files - Most of the time, these files are preconfigured when running the create-next-app. These will not need modification for the tutorial.

