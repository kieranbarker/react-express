# React/Express

This is one way you can use React and Express together.

## Usage

In one terminal tab/window, navigate to the `react` directory, install the dependencies, and run the `build` script. This will bundle the React app for production and put it in the `react/dist` directory.

```sh
cd react
npm install
npm run build
```

In a separate terminal tab/window, navigate to the `express` directory, install the dependencies, and run the `start` script. This will start the Express server and serve the static files from the `react/dist` directory.

```sh
cd express
npm install
npm start
```

Open up http://localhost:3000 and you should see the React app being served.

## Setup

Assuming you had empty `react` and `express` directories, here's how you could set this up.

Navigate to the `react` directory and set up a Vite project in the current directory (note the `.` at the end):

```sh
npm init vite@latest .
```

Choose `React`, then `JavaScript`, then install the dependencies as instructed.

Navigate up one directory and into the `express` directory, create a `package.json` file, and install Express:

```sh
cd ../express
npm init --yes
npm install express
```

## Notes

You don't actually need the Express server for development. In the `react` directory, you can just run `npm run dev` and away you go. But if you were using an Express server in production, you would need to build the project and then serve it as shown in this repo.
