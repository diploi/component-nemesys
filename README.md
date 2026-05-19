<img alt="icon" src=".diploi/icon.svg" width="32">

# Nemesys Component for Diploi

An internal component for Nemesys. Based on the [Node.js](https://github.com/diploi/component-nodejs) component that can be used to run any Node.js app.

Uses the official [node](https://hub.docker.com/_/node) Docker image.

## Operation

### Development

Will run `npm install` when component is first initialized, and `npm run dev` when deployment is started.

### Production

Will build a production ready image. Image runs `npm install` & `npm build` when being created. Once the image runs, `npm start` is called.

### Notes

- If you are using packages that use native libraries (like `node-canvas` e.g.), it is a good idea to switch the `Dockerfile` and `Dockerfile.dev` to use `node:XX` instead of `node:XX-slim`. You can also add any missing libraries with `RUN apt update && apt install -y <package>` in the dockerfiles.

## Links

- [Adding Node.js to a project](https://docs.diploi.com/building/components/nodejs)
- [Node official page](https://nodejs.org/en)
