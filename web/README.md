# Next Dashboard Front Server

## Installation

```
git clone https://github.com/imfsdev/React-Redux-Relay-Next.js-dashboard.git
cd React-Redux-Relay-Next.js-dashboard/web
cp .env.example .env
```

Edit **.env** file and set your options

### Run Production

```
cd React-Redux-Relay-Next.js-dashboard.git/common
yarn install --prod

cd ../web
yarn install --prod
yarn relay
yarn build
yarn start
```

### Run Static Mode Production

```
cd React-Redux-Relay-Next.js-dashboard.git/common
yarn install --prod

cd ../web
yarn install --prod
yarn relay
yarn build
yarn export
```

Point your HTTP server to **/out** subdirectory or just do **yarn serve**

### Run Development

```
cd React-Redux-Relay-Next.js-dashboard.git/common
yarn install

cd ../api
yarn install
yarn schema

cd ../web
yarn install
yarn relay
yarn dev
```

### System service

#### systemd

```
cp systemd.service /etc/systemd/system/next-dashboard-web.service
systemctl daemon-reload
systemctl enable next-dashboard-web
systemctl start next-dashboard-web
```

#### PM2

```
pm2 start pm2.config.js
```
