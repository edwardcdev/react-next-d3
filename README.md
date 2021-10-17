# Simple Dashboard using multiple JS stack

A simple React/Redux/Relay/Next.js dashboard template with perfect benchmarks using Material UI.

![Dark Theme](docs/dark.png "Dark Theme")

![Light Theme](docs/light.png "Light Theme")

## Specification

- React/Redux with Immutable, Thunk, Reselect, etc.

- GraphQL with subscriptions using React Relay Modern (not Apollo)

- Next.js with Webpack and Babel doing cached Server Side Rendering (SSR) on an Express.js backend with Redis and MongoDB via Mongoose

- Material UI with custom dark and light themes

- Formik, Mapbox GL, Victory Chart, React Intl, React Virtualized, etc.

- Email/password or Twitter/Google/Facebook authorization using Passport.js

- Caching service worker from Google Workbox

- Modular "ducks" project structure with Dependency Injection Container

## Running

- **MongoDB** for the data

- **Redis** for the cache and PubSub

- API Server: **[api/](api)**

- Frontend App: **[web/](web)**
