<img  width="700" height="500" alt="github pages" src="https://user-images.githubusercontent.com/30548190/88172166-29d3b380-cc3e-11ea-816f-73fbee51d467.jpeg">
<hr>

<p>So, You have built a React app. </p>
<p>Next step? Deploying. </p>
<p>How you gonna do it?? Just follow along!! </p>

## Step 1: Add homepage to package.json
This is a very important step. DONT skip it.

<li> Open your package.json and add a homepage field for your project:
for example: </li>

```"homepage": "https://myusername.github.io/my-app"```

<li> for a GitHub user page:</li>

```"homepage": "https://myusername.github.io"```

<li> for a custom domain page:</li>

```"homepage": "https://mywebsite.com"```



Create React App uses the homepage field to determine the root URL in the built HTML file.

<hr>


## Step 2: Install gh-pages and add deploy to scripts in package.json

<li>To publish it at homepage, run:</li>

```npm install --save gh-pages```

<li>You may use yarn for the same:</li>

```yarn add gh-pages```

<li>Now, add the following scripts in your package.json:</li>

``` 
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build" 
```
    
The predeploy script will run automatically before deploy is run.

<li>If you are deploying to a GitHub user page instead of a project page you'll need to make one additional modifications.

Modify your package.json scripts to push deployments to master:</li>

``` 
    "predeploy": "npm run build",
-   "deploy": "gh-pages -d build",
+   "deploy": "gh-pages -b master -d build"

```

<hr>


## Step 3: Deploy the site by running npm run deploy

<li>Then run:</li>
    
```npm run deploy```

<hr>


## Step 4: For a project page, ensure your project’s settings use gh-pages

<li>Finally, make sure GitHub Pages option in your GitHub project settings is set to use the gh-pages branch</li>
<img align = 'center' width="516" alt="github pages enabling" src="https://user-images.githubusercontent.com/30548190/88172305-669faa80-cc3e-11ea-9608-f609fc467493.png">


And tadaa! :tada:  You have published your application successfully. 
<p>It might take some time to actually be available but you have done your part.:metal: Give yourself a high five!!</p>
 <hr>
 <hr>

