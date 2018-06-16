# Hacker Newz

A React application that uses the HackerNews API to retrieve computer science and technology-related articles from the [Hacker News site](https://news.ycombinator.com/).

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

You can find the most recent version of this guide [here](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md).

## Table of contents

* [Live](#live)
* [Screenshots](#screenshots)
* [About this project](#about-this-project)
* [Getting started](#getting-started)
* [Deployment](#react-deployment)
* [Technologies used to create app](#technologies-used)
* [Direction for future development](#future)
* [Issues](#Issues)

## <a name="live"></a>Live

<https://hacker-newz.herokuapp.com/>

## <a name="screenshots"></a> Screenshots

<img src="readme_images/hackernews.png">

## <a name="about-this-project"></a> About this project

* [How the app works](#how-app-works)
* [How the app is built](#how-the-app-is-built)

### <a name="how-app-works"></a> How the app works


### <a name="how-the-app-is-built"></a> How the app is built

This project was built using React, which is an open-source Javascript library developed at Facebook specifically for the task of developing user interfaces. React relies on a component-based architecture where elements of the user interface are broken into self-contained components.

For a high level overview of React, check out this video: <https://www.youtube.com/watch?v=x7cQ3mrcKaY>.

The React documentation is available at <https://reactjs.org/>.

For more information on how this project is structured and broken into various components, see [Structure of the project](#structure-of-project).

The app also uses the HackerNews API to retrieve computer science and tech-related articles from the [Hacker News site](https://news.ycombinator.com/)  For more information about this API, see the [HackerNews API documentation](https://github.com/HackerNews/API).

## <a name="getting-started"></a> Getting started

The following section will take you through the steps of setting up this application and getting it running locally on your computer.

If you don't want to set up this project locally and just want to see the deployed application, go to <https://hacker-newz.herokuapp.com/>.

To set up this application locally on your computer, perform the following steps:

1. [Clone the repository](#clone-repository)

2. [Install Node.js](#install-node)

3. [Install yarn](#install-yarn)

4. [Install the dependencies](#dependencies)

5. [Install MongoDB](#install-mongo)

6. [Start the React development server](#start-server)


### <a name="clone-repository"></a> 1. Clone the repository

The first step is to clone the project repository to a local directory on your computer. To clone the repository, run the following commands:
<pre>
  git clone https://github.com/philipstubbs13/hackernews.git
  cd hackernews
</pre>

#### <a name="structure-of-project"></a> Structure of the project

<p>After you clone the repository, navigate to the project root directory (hackernews). The project directory structure is set up as follows:</p>


* <b>node_modules</b>: This folder contains the project dependencies. It is ignored by git when committed to GitHub and Heroku. You install the project dependencies by running <b>yarn install</b> from the project root directory. For more information about installing dependencies for this project, go to [Install the dependencies](#dependencies).
* <b>public</b>: The public folder contains the index.html file. This HTML file is a template. The file is empty. So, if you open it directly in a browser, you will get an empty page. Rather than placing the HTML code directly in index.html, this app uses a React component-based architecture to create, build, and render UI components to the page. This folder also contains the favicon that is displayed on the browser tab.
* <b>readme_images</b>: Contains the screenshots that are used in the project README file.
* <b>src</b>: The src folder is where the React app components reside.
    * <b>index.js</b>: The index.js file is the top level file of the React app. In index.js, the App.js file is imported, and the ReactDOM.render method is used to render App.js to the page.
    * <b>App.js</b>: The App.js file is where the React components are defined and rendered and where the routes are set up. This file also contains the axios request to grab Hacker News articles from the Hacker News site using the HackerNews API.
    * <b>App.css</b> and <b>index.css</b>: The external css stylesheets for the app.
* <b>package.json</b>: Lists the project dependencies and their version numbers. It also contains various scripts to start the server, create a production build, and run tests.
* <b>yarn.lock</b>: Dependency tree for the project. Lists all the client dependencies and their versions.
* <b>.gitignore</b>: Anything listed inside this file (for example, node_modules) will not be tracked by GitHub or Heroku when code is committed.

### <a name="install-node"></a> 2. Install Node.js

<p>If you don't already have Node.js installed on your computer, you can install the latest version here: https://nodejs.org/en/.</p>

### <a name="install-yarn"></a> 3. Install yarn

To be able to install the dependencies and start the application locally, you will need to install yarn. Yarn is a package manager like npm.

To install yarn, run the following command:
<pre>
  npm install -g yarn
</pre>

For more information about yarn and other installation options, see the yarn documentation: <https://yarnpkg.com/en/>.

### <a name="dependencies"></a> 4. Install the dependencies

<p>The following packages are dependencies to the project.<p>

<ul>
  <li><b>axios</b> - a promise based HTTP client for the browser and node.js (https://www.npmjs.com/package/axios)</li>
  <li><b>classnames</b> - A JavaScript utility for conditionally joining classNames together. (https://www.npmjs.com/package/classnames)</li>
  <li><b>lodash</b> - A JavaScript utility library (https://www.npmjs.com/package/lodash)</li>
  <li><b>prop-types</b> - Used to document the intended types of properties passed to components. React checks props passed to components against those definitions, and warn in development if they don’t match.(https://www.npmjs.com/package/prop-types)</li>
  <li><b>react</b> - package for accessing React (https://www.npmjs.com/package/react)</li>
  <li><b>react-dom</b> - serves as the entry point of the DOM-related rendering paths (https://www.npmjs.com/package/react-dom).</li>
  <li><b>react-scripts</b>: package that includes scripts and configuration used by Create React App. (https://www.npmjs.com/package/react-scripts)</li>
  <li><b>react-test-renderer</b> -  this package makes it easy to grab a snapshot of the "DOM tree" rendered by a React DOM component without using a browser or jsdom. (https://www.npmjs.com/package/react-test-renderer)</li>
</ul>

<p>Version information for each of these packages is available in the <b>package.json</b> file in the project root directory and in the <b>client</b> directory.</p>

<p>After you clone the repository to a local directory, change directory to the project root directory and run the following command to install the required packages:</p>
<pre>yarn install</pre>

### <a name="start-server"> 5. Start the React development server.</a>

<p>After performing all of the setup steps in the <b>Getting started</b> section, navigate to the project root directory (hackernews) and run the following command to start the React development server:</p>
<pre>
yarn start
</pre>

<p>After the development server has started, a Chrome browser window should open, and you should see the application. If the browser does not automatically open after the server starts, you can verify that the application is working locally on your computer by manually opening Chrome and going to <a href="http://localhost:3000">http://localhost:3000</a>.</p>

<p><b>Tip</b>: If you are still unable to see the application in the browser at <a href="http://localhost:3000">http://localhost:3000</a>, ensure that no other applications/processes are using port 3000. If port 3000 is in use by another process, kill that process and then restart the server.</p>

## <a name="react-deployment"></a> Deployment

This app is deployed to Heroku. To deploy the app, you will need to build a production version of the app as well as have Heroku CLI installed.

1. Download and install the Heroku CLI. You can install the Heroku CLI <a href="https://devcenter.heroku.com/articles/heroku-cli">here</a>.</p>

2. If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key.
<pre>heroku login</pre>

3. Change directory to the project root directory (<b>NYT-React-Search</b>).

4. If you have deployed the app before, delete the <b>NYT-React-Search/client/build</b> folder.

5. Run the following command to build a clean production version of the app.
<pre>yarn build</pre>
<p>This command creates a folder called <b>build</b> inside of the <b>client</b> folder. </p>

6. Deploy your changes
<pre>
git add .
git commit -am "heroku commit message"
git push heroku master
</pre>

<p>If you run into any issues with deploying the app to Heroku, run the following command in the project root directory to see the Heroku logs.</p>
<pre>heroku logs</pre>

## <a name="technologies-used"></a> Technologies used to build app

* HTML
* CSS
* Javascript
* React (<https://reactjs.org/>)
* Node.js (<https://nodejs.org/en/>)
* HackerNews API (<https://github.com/HackerNews/API>)

## <a name="future"></a> Direction for future development
Source code will be developed over time to handle bug fixes and new features.

The following is a list of potential enhancements for future code development.

* Add feature to save articles to a MongoDB database.

* Add second page to the app that allows users to see saved articles.

* Add feature that allows users to leave comments on saved articles.

* Update css/styling  of app.

## <a name ="Issues"></a> Issues

<p>If you find an issue while using the app or have a request, <a href="https://github.com/philipstubbs13/hackernews/issues/" target="_blank">log the issue or request here</a>. These issues will be addressed in a future code update.</p>