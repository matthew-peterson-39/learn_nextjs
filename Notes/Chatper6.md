# Setting Up Your Database

- To set up a database, navigate to Vercel and import the github repository.

- After deployment, setup a database by navigating to the dashboard, selecting databse, and creating a database connection of the language of your choosing. I chose postgresSQL. 

- Ensure the database region selected is Washing (iad1), the default, but keep in mind that this database region cannot be changed once initialized.

- Once initialized, navigate to the .env.local, reveal the secret key and copy the snippet. 

- Then, change the .env.example file within the local project directory. To be '.env' and paste the copied snippet into here.

## Deployment Error

- It is important to note where you package.json file exists in your project directory when selecting the root directory. For instance, I altered my directory from the tutorial becasue I added an additional directory for note taking. This change required me to explictly define the root directory instead of using the preconfigured option of './'.

- Before realizing this recieved deployment errors stating 
> Error: No Next.js version could be detected in your project. Make sure `"next"` is installed in "dependencies" or "devDependencies"

- Despite having the files installed properly. This, in the end was due to the deployment builder, rightfully so, being unable to find the package.lock.json file.

