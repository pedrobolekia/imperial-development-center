## Requirements

- [node](https://nodejs.org/en) >= 12.0
- [npm](https://www.npmjs.com) >= 6.0

## Getting Started

**1. Install all of the dependencies:**

```sh
yarn
```

**2. Start to run it:**

```sh
yarn build  # Building bundle
yarn start  # Running production server
```

Now the app should be running at [http://localhost:8080](http://localhost:8080)

> Note: You can change the port that you want from the `./src/config`.

## Script Commands

I use [cross-env](https://github.com/kentcdodds/cross-env) to set and use environment variables across platforms. All of the scripts are listed as following:

| `yarn <script>`  | Description                                                                        |
| ---------------- | ---------------------------------------------------------------------------------- |
| `dev`            | Runs your app on the development server at `localhost:3000`. HMR will be enabled.  |
| `dev:build`      | Bundles server-side files in development mode and put it to the `./public/server`. |
| `start`          | Runs your app on the production server only at `localhost:8080`.                   |
| `build`          | Bundles both server-side and client-side files.                                    |
| `build:server`   | Bundles server-side files in production mode and put it to the `./public/server`.  |
| `build:client`   | Bundles client-side files in production mode and put it to the `./public/assets`.  |
| `analyze:server` | Visualizes the bundle content of server-side.                                      |
| `analyze:client` | Visualizes the bundle content of client-side.                                      |
| `lint`           | Lints all `.tsx?`, `.jsx?` and `.scss` files.                                      |
| `lint:code`      | Lints all `.tsx?` and `.jsx?` files (With `--fix` to auto fix eslint errors).      |
| `lint:type`      | Runs type checking for `.tsx?` files.                                              |
| `lint:style`     | Lints all `.scss` files (With `--fix` to auto fix stylelint errors).               |
| `lint:format`    | Formats all files except the file list of `.prettierignore`.                       |
| `test`           | Runs testing.                                                                      |
| `test:watch`     | Runs an interactive test watcher.                                                  |
| `test:cov`       | Runs testing with code coverage reports.                                           |
| `test:update`    | Updates jest snapshot.                                                             |

### How to Deploy

To deploy you app to cloud service (e.g. AWS, GCP, Azure etc.), you can follow the instructions below.

1. Build then install production dependencies:

```sh
yarn build                  # Building bundle
rm -rf node_modules         # After building remove node modules
yarn install --production   # Then install dependencies only
```

2. Pack necessary folders/files to your Node.js server:

- ✅ public
- ✅ node_modules
- ✅ package.json

1. Run your app:

```sh
yarn start
```
