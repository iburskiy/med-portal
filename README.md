# med-portal

The project has been published to Github Pages, namely to https://iburskiy.github.io/med-portal.
It builds the static content into `dist` folder. A build happens on each commit that publishes content to the link above.
I created package.json and "scripts" section that copies `images` and `index.html` to `dist` folder.
It also compiles scss files to css file in `dist` folder. 
I checked in the repo to my github and then went to project settings > Pages > Build and deployment > Github Actions.
It produced `.github/workflows/static.yml` in my project that I committed right into github web interface.
Then I pulled it in IDE and changed the following line: `path: './dist'`. 
Then after each commit I could see that new workflow appears in my project in Actions tab in github.
