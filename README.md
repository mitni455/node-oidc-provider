# Node OpenID Connect Server 

oidc-provider is a bla bla bla who cares your a busy developer here's how to get this thing actually working.

# Server
## step 1 - install and run
```
git clone https://github.com/mitni455/node-oidc-provider node-oidc-server 
cd node-oidc-server/example
npm install
npm start
```

👉The server is known as the `issuer` in OIDC. 

## step 2 - review and/or configure Client settings
We need to setup a `client` app to interact with this server. 

We will use the `implicit` flow for a SPA (see Client setup below). Rule of thumb use `implicit` for frontend apps, and `authorization code` for a client server (e.g. if you serve the front end with express, koa, ect)

👻open `example/settings.js` and edit the `module.exports.clients`

* 💻client_id: `put_a_unique_client_id_here`,
* 💻client_secret: `put_a_unique_client_secret_here`,
* 👉grant_types: `['implicit']`,
* 💻redirect_uris: `['http://client_browser_app_goes_here/callback_handler_page.html'],`

*e.g.* 
``` javascript
module.exports.clients = [{
    client_id: 'oidcCLIENT',
    client_secret: '91c0fabd17a9db3cfe53f28a10728e39b7724e234ecd78dba1fb05b909fb4ed98c476afc50a634d52808ad3cb2ea744bc8c3b45b7149ec459b5c416a6e8db242',
    grant_types: ['implicit'],
    redirect_uris: ['http://localhost:5000/oidc-client-sample.html'],
}];
```


## step 3 - review/configure User settings
We need to setup a `user` to login 



# Client

# How it works 


