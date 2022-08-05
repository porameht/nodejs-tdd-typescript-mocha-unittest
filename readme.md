**TDD With TypeScript, Express, NodeJS, and Mocha Unit Tests**

- install package.json by comman `npm init -y`
- install dependencys by command `npm i -save express dotenv`
- install dependencys on development by command `npm i -D mocha chai typescript nodemon supertest ts-node tsconfig-paths`
- install @types `npm i -D @types/chai @types/mocha @types/node @types/supertest @types/express`
- add script for run build, dev and test

  ```
  "test": "NODE_ENV=test mocha --check-leaks -r tsconfig-paths/register -r ts-node/register \"test/**/*.spec.ts\"",
  "buile": "tsc -p .",
  "dev": "NODE_ENV=dev nodemon -r tsconfig-paths/register src/app.ts"
  ```

- initial typescript by command `tsc --init` and config within file tsconfig.json open `"rootDir": "./src"`, `"moduleResolution": "node"`, `"baseUrl": "./"`, `"outDir": "./dist"`

- create folder test and within folder create file `index.spec.ts` and create folder server then create file `server-runs.spec.ts` in folder server

- after create file spec.ts edit the scripts like so: file

- in file `server.spec.ts` import assertion libary and request by command `import request from "supertest" import {expect} from 'chai'`

- create folder src then create file server.ts and import express `import express, { Application, Request, Response, NextFunction } from "express"`

- navigate to file server.spec.ts and import function form file src/server.ts defind const `app`

- create folder route within test and create file index.spec.ts this folder

- create folder route within folder src and after create folder we will create file index.ts and auth.th `build test case /auth and test failing result`

- after create file and implement route /auth then import to file server.ts by import command `import routes from "./routes/index"` and use `app.use(routes);` run test again result with test case /auth are `passing`

- create file `dashboard.ts` within folder routes and implement route /dashboard then create folder dashboard within folder `test/routes` and create file index.spec.ts then add script test case `build test case /dashboard and test passing result`

- create file app.ts within folder src and import `import createServer from './server'` and create function `startServer` and call backfunction startServer
