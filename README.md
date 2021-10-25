# Simple Dashboard using multiple JS stack

A simple React/Redux/Relay/Next.js dashboard template with perfect benchmarks using Material UI.

![Dark Theme](docs/dark.png "Dark Theme")

![Light Theme](docs/light.png "Light Theme")

## Specification

- React/Redux with Hooks, Immutable, Thunk, Reselect, etc.

- GraphQL with subscriptions using React Relay Modern (not Apollo)

- Next.js with Webpack and Babel doing cached Server Side Rendering (SSR) on an Express.js backend with Redis and MongoDB via Mongoose

- Material UI with custom dark and light themes

- Internationalization using React Intl (Format.js) which supports ICU message syntax

- Formik, Mapbox GL, DeckGL, D3, Victory Chart, React Intl, React Virtualized, etc.

- Email/password or Twitter/Google/Facebook authorization using Passport.js

- Caching service worker from Google Workbox

- Modular "ducks" project structure with Dependency Injection Container

## Architecture

This project is comprised of 4 servers:

- **MongoDB** for the data

- **Redis** for the cache and PubSub

- One or more API Servers: **[api/](api-server)**

  These are serving API requests from the browser and the Front Server. Access to MongoDB and to Redis is required.

- Optionally, one or more Front Servers: **[web/ssr-server](web/ssr-server)**

  These are doing (cached) SSR for the user. The public domain name of the site is pointing to this server.

  Only access to Redis is required.

  If you don't need SSR you could also switch to static site mode, in which case you don't need Front Servers at all (any http server, like nginx, could serve the static files)

**NOTE** Please make sure both Mongo and Redis is password protected or not accessible from the public network
