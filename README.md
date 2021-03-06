# react-templates
A curated list of React starter templates for various project types.

## React Web App

Create React App?

## React Component Library

TODO

## React Desktop App

[Electron React Boilerplate](https://github.com/electron-react-boilerplate/electron-react-boilerplate)

* Electron
* TypeScript
* React
* CSS Modules (+ SCSS)
* [React Router 5](https://reactrouter.com/web/guides/quick-start)
* [Fast Refresh](https://github.com/pmmmwh/react-refresh-webpack-plugin)
* Yarn

Works out of the box. Doesn't screw up `fs` and other node built-ins (use them directly in your components!)

### Install

```sh
git clone --depth 1 --single-branch https://github.com/electron-react-boilerplate/electron-react-boilerplate.git your-project-name
cd your-project-name
yarn
```

### Run

```
yarn run start
```

## Static Website

Gatsby? Next.js? react-static?

## TypeScript Node App

esbuild

Use [`cli-api`](https://github.com/mnpenner/node-cli-api) for a command-line interface.

## TypeScript Node Library

esbuild

## GraphQL Server

[Apollo Server](https://www.apollographql.com/docs/apollo-server/). I used to recommend writing the schema using the GraphQL definition language (SDL) and using a loader/plugin to compile it, but now I think the language is [too weak](https://github.com/graphql/graphql-spec/issues/190), so we might be better off doing it the other way around -- write the schema in TypeScript and compile it back to SDL if desired, or just use GraphiQL or [GraphQL Playground](https://github.com/graphql/graphql-playground#faq).

I prefer a relational database on the backend (MariaDB or PostgreSQL). To generate optimal queries, there's a few approaches...

* [DataLoader](https://github.com/graphql/dataloader) -- load more data than needed and cache
* JoinMonster -- generate optimal queries

## GraphQL Client

I used to think Apollo Client was the obvious choice, but it has [weird caching behaviour](https://github.com/apollographql/apollo-client/issues/5963) out of the box. Would like to try [URQL](https://formidable.com/open-source/urql/docs/comparison/).

## Build Tools/Bundlers

|    | App  | Lib |
| --- | --- | --- |
| Web  | Webpack? (esbuild splitting is WIP and doesn't have same set of loaders) | `esbuild --bundle --minify --sourcemap --target=chrome58,firefox57,safari11,edge16`[??](https://esbuild.github.io/getting-started/#bundling-for-the-browser) |
| Node  | `esbuild src/main.ts --bundle --outfile=dist/onemig.js --platform=node [--minify] [--target=node14 --sourcemap --watch]`[??](https://esbuild.github.io/getting-started/#bundling-for-node)  | esbuild + `tsc --emitDeclarationOnly` ? |

## Package Managers

- [npm](https://www.npmjs.com/)
- [yarn](https://classic.yarnpkg.com/lang/en/)
- [yarn 2](https://yarnpkg.com/)
- [pnpm](https://pnpm.io/)
