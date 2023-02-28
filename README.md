# med-portal

The project has been published to Github Pages, namely to https://iburskiy.github.io/med-portal.

To create a new repository:
In the upper-right corner of any page on Github, use the  drop-down menu, and select New repository.
Add a name of the repository, select Private or Public, follow further instructions to run Git commands in CMD for the project.

To build the project locally:
- Run `npm run build`. It builds the static content into `dist` folder. Open index.html in browser.

To publish the changes to Github public URL:
- build the project locally with `npm run build`
- commit changes including `dist` folder. A build happens on each commit that publishes content to the link above.

What I did:
Found the following info:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow
I created package.json. `scripts > copy` section copies `images` and `index.html` to `dist` folder.
`scripts > scss` compiles scss files to css file to `dist` folder. `sass` package is installed only locally. It's automatically added to `node_modules/.bin`. 
It lets running the command in `scripts > scss`:
`sass --embed-sources styles.scss dist/styles.css`
I added the repo to my github and then went to `Settings > Pages > Build and deployment > Github Actions`.
Then selected `Static Html` option. It produced `.github/workflows/static.yml` in the project asked to commit it right into Github web interface.
I changed the following line: `path: './dist'` to make Github take static content from `dist` folder.
Then I pulled the change in IDE. Then after each commit I could see that a new workflow (or build) appears in my project in `Actions` tab of the project in Github.

