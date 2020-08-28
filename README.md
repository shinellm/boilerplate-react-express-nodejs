# create-react-app with a custom Node Server

This is a simple website boilerplate that uses a [React](https://github.com/facebook/create-react-app) frontend and a custom Node backend (server for API, proxy, & routing).

* 🗂 [File Layout](#user-content-file-layout)
* 💻 [Local Development](#user-content-local-development)

This boilerplate can be used as a starting point for projects, which are intended to be deployed to a hosting service such as Heroku or other fullstack applications. 
#### 📚 Helpful Links/Projects to Reference
* [Deploying create-react-app](https://create-react-app.dev/docs/deployment/)
* [React Production Deployment on Netlify, Vercel and Heroku](https://github.com/esausilva/react-production-deployment)
* [create-react-app with a Node server on Heroku](https://github.com/mars/heroku-cra-node)

## File Layout

This project consists of a client folder, which contains the React frontend UI, and a server folder, which contains the Node backend server. The boilerplate is a combination of two npm projects, so there are two `package.json` configs and therefore two places to run `npm` commands:

  1. [**Node server**](server/): [`./package.json`](package.json)
      * contains express starter code in the [`server/app.js`](server/app.js) file
      * contains example api routing in the [`server/api/index.js`](server/api/index.js) file
  2. [**React client**](client/): [`client/package.json`](client/package.json)
      * generated by [create-react-app](https://github.com/facebook/create-react-app)
      * production build generated via `build` script in the Node server's [`./package.json`](package.json)

## Local Development

Because this app is made of two npm projects, there are two places to run `npm` commands:

1. **Node API Server** at the root `./`
2. **React Frontend UI** in `client/` directory.

* 📝 **Note:** To simplify this process, `"npm-run-all"` was added to the devDependencies. Local development can instead be started at the root `./` by running:
```bash
# Initial setup
npm install

# Start the backend and frontend servers
npm run dev
```

### Run the Node API Server

In a terminal:

```bash
# Initial setup
npm install

# Start the server at http://localhost:8080/
npm start
```

Install new npm packages for Node:

```bash
npm install package-name --save
```


### Run the React Frontend UI

The React app is configured to proxy backend requests to the local Node server. (See [`"proxy"` config](client/package.json))

In a separate terminal from the API server, start the UI:

```bash
# Always change directory, first
cd client/

# Initial setup
npm install

# Start the server http://localhost:3000/
npm start
```

Install new npm packages for React Frontend UI:

```bash
# Always change directory, first
cd client/

npm install package-name --save
```
