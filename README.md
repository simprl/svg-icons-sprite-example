# SVG Icons Sprite Generator & Publisher Example Template

Welcome to the SVG Icons Sprite Generator and Publisher template! This template is designed to generate SVG sprite icons using the [react-svg-sprite-generator](https://www.npmjs.com/package/react-svg-sprite-generator) library and then publish them as an npm module.

## Generated documentation: [Your GitHub pages link](https://simprl.github.io/svg-icons-sprite-example/)
## Published npm module: [svg-icons-sprite-example](https://www.npmjs.com/package/svg-icons-sprite-example)
[![](https://img.shields.io/npm/v/svg-icons-sprite-example?style=flat)](https://www.npmjs.com/package/svg-icons-sprite-example)

## Features
- Automatic generation of SVG sprite icons.

- Documentation generation for the SVG sprite.

- Automated version bumping.

- Compilation of TypeScript.

- Publication to npm registry.

- Continuous Deployment to GitHub Pages for documentation. 

## How It Works
Upon a push to the **master** branch or when triggered manually from the GitHub Actions tab, the tool performs the following:

- Sets up the required Node.js environment. 
- Generates the SVG sprite icons and the associated documentation. 
- Bumps the npm package version. 
- Compiles any TypeScript code. 
- Publishes the updated npm package. 
- Deploys the generated documentation to GitHub Pages.

## Getting Started
### Creating your repository from a template:
   https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template

### Setting Up NPM Access Token
For publishing packages to the npm registry, you need to authenticate your GitHub Actions workflow with npm. This can be achieved by using an NPM_TOKEN. Here's how you can set it up:

#### 1. Generating the NPM Token
- **Login to npm:** Go to **npmjs.com** and log in to your account. 
- **Create a new token:** Once logged in, click on your profile picture at the top right and select **Auth Tokens** from the dropdown. 
- Click on **Create New Token**. 
- Choose the **Read and Publish** permission level to give the token both read and publish rights. This will allow your GitHub Action to publish packages on your behalf. 
- Click on **Create Token**.
- **Copy your token**: Once created, you'll see your new token. Make sure to copy this immediately! For security reasons, you will not be able to see the token again.

#### 2. Adding the NPM Token to GitHub
- **Go to your GitHub repository:** Navigate to your GitHub repository where you're running the workflow. 
- **Settings:** Click on the **Settings** tab of the repository. 
- **Secrets:** On the left sidebar, click on **Secrets**. 
- Click on the **New repository** secret button. 
- Enter name **NPM_TOKEN** and value (Paste the token you copied from npm)
- Click on **Add secret**.

**NPM_TOKEN** is now set up. Your GitHub Actions workflow can use this token by referencing ${{ secrets.NPM_TOKEN }}, as shown in your .github/workflows/githubpages.yml file.


### Update svg files 
Place your SVG icons in the src/assets/icons directory.
Upon pushing to the master branch, the SVG sprite and documentation will be generated, and the module will be updated on npm with a new version.

### Customizing the README.md
#### Adjusting the Template:
The **README.md** file in this repository is dynamically generated. The content is primarily sourced from the **readme.template.md** file. If you want to make changes to the introductory part or the general documentation of the README, you should make edits to this template file.

#### SVG Icons Table:
At the end of the **README.md** file, a table containing the list of generated SVG icons is automatically appended. This provides an organized and visual representation of all the SVG icons that are available in the sprite.

#### How to Update:
If you add, remove, or modify SVG icons in the **src/assets/icons** directory, the table in the **README.md** file will be updated automatically upon pushing to the **master** branch.

In essence, to adjust the primary content of the **README.md**, modify the **readme.template.md** file. For changes to the list of SVG icons, simply update the icons in the specified directory, and the table in the README will reflect these changes after the workflow runs.
# List of icons
| Source | Name | Path |
|---|---|---|
|  ![](/src/assets/icons/arrows/bottom.svg) | ARROWS_BOTTOM | arrows/bottom.svg |
|  ![](/src/assets/icons/arrows/left.svg) | ARROWS_LEFT | arrows/left.svg |
|  ![](/src/assets/icons/arrows/right.svg) | ARROWS_RIGHT | arrows/right.svg |
|  ![](/src/assets/icons/arrows/top.svg) | ARROWS_TOP | arrows/top.svg |