# treblle-sails
Sails hook for [Treblle](https://treblle.com)

This hook wraps the official [Treblle package for Node](https://github.com/Treblle/treblle-node) and it provides conventions and configurations that a Sails developer will love.

## Installation

To install this hook run the below command in your terminal:

```sh
npm i --save treblle-sails
```

## Setting up credentials
Treblle needs you to specify your project Id and API key. treblle-sails makes this easy to do by expecting you to set it up in `config/local.js` as:

```js
// config/local.js
treblle: {
  apiKey: '<YOUR_TREBLLE_API_KEY>',
  projectId: '<YOUR_TREBLLE_PROJECT_ID>'
}
```

`treblle-sails` will also check your environment for the following environment variables:

* `TREBLLE_API_KEY`
* `TREBLLE_PROJECT_ID`

## Config options
`treblle-sails` also checks `config/treblle.js` for config options like `apiKe`, `projectId`, etc. So you can create a `config/treblle.js` file in your project to look like this:

```js
// config/treblle.js
module.exports.treblle = {
  apiKey: '<YOUR_TREBLLE_API_KEY>',
  projectId: '<YOUR_TREBLLE_PROJECT_ID>',
  additionalFieldsToMask: ['key1', 'key2'], // optional
  showErrors: true, // Optional, defaults to true
}
