# Hydrant

A generic JavaScript helper library to query and manipulate Drupal 8 via core REST

---

## Setup

* Run `npm i` to install development dependencies.
* Run `npm t` to run tests and check coverage.
* Run `npm run build` to create a browser version; located in `dist/hydrant.js`.

## Usage

First, ensure that you have set up cross-origin resource sharing on your Drupal site to enable Hydrant to perform necessary tasks.

From a server environment,

```javascript
const Hydrant = require('./lib/hydrant');

const hydrant = new Hydrant('http://test.dev', {username: 'admin', 'password': '1234'});

hydrant.get('node', 1)
  .then(res => {
    // res
  })
  .catch(err => {
    // err
  });
```

From the browser,

```javascript

const hydrant = new window.Hydrant('http://test.dev', {username: 'admin', 'password': '1234'});

hydrant.get('node', 1)
  .then(res => {
    // res
  })
  .catch(err => {
    // err
  });
```
