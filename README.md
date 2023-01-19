# med-portal

The project has been published to Github Pages, namely to https://iburskiy.github.io/med-portal.

To publish the project:
1) Make some changes
1) Build the project with `npm run build`. It builds the static content into `dist` folder.
1) Publish the project: commit changes including `dist` folder. A build happens on each commit that publishes content to the link above.

I created package.json and "scripts" section that copies `images` and `index.html` to `dist` folder.
It also compiles scss files to css file in `dist` folder. 
I checked in the repo to my github and then went to project settings > Pages > Build and deployment > Github Actions.
It produced `.github/workflows/static.yml` in my project that I committed right into github web interface.
Then I pulled it in IDE and changed the following line: `path: './dist'`. 
Then after each commit I could see that new workflow appears in my project in Actions tab in github.

`sass` package is installed only locally. It's automatically added to `node_modules/.bin`. It lets running the command in "scripts":
`sass --embed-sources styles.scss dist/styles.css`