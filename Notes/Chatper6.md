# Setting Up Your Database

- To set up a database, navigate to Vercel and import the github repository.

- It is important to note where you package.json file exists in your project directory when selecting the root directory. For instance, I altered my directory from the tutorial becasue I added an additional directory for note taking. This change required me to explictly define the root directory instead of using the preconfigured option of './'.

- Before realizing this recieved deployment errors stating 
> Error: No Next.js version could be detected in your project. Make sure `"next"` is installed in "dependencies" or "devDependencies"

- Despite having the files installed properly. This, in the end was due to the deployment builder, rightfully so, being unable to find the package.lock.json file.