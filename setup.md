To use `@testing-library/reac`t in your React app, you will need to do the following:

1. Install the `@testing-library/react` package by running `npm install --save-dev @testing-library/react` or `yarn add --dev @testing-library/react`.

2. In your `jest.config.cjs` file, add the following code to specify the test environment:

```js
module.exports = {
  testEnvironment: '@testing-library/react/environment',
  setupFilesAfterEnv: ['@testing-library/react/cleanup-after-each'],
};

```
3. In your `bsconfig.json` file, add the following line to include the `bs-react-testing-library` dependency:
```js
"bs-dev-dependencies": ["bs-react-testing-library"]
```
4. In your `babel.config.cjs` file, make sure that you have the `@babel/preset-react` preset installed, as it is required for transpiling JSX:
```js
module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['@babel/preset-env', '@babel/preset-react'],
  };
};

```
5. Create a `__tests__/` folder in your project root directory and add your React component tests inside it.