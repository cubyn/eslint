# Cubyn ANgular/babelify/browserify Style Guide

*A mostly reasonable approach to React and JSX*

## Table of Contents

  1. [Basic Rules](#basic-rules)
  1. [Naming](#naming)
  1. [Declaration](#declaration)

## Basic Rules

  - Only include one React component per file.
  - Always use JSX syntax.
  - Do not use `React.createElement` unless you're initializing the app from a file that is not JSX.

## Class vs React.createClass

  - Use class extends React.Component unless you have a very good reason to use mixins.

  ```javascript
  // bad
  angular.controller('controller', [function() {}]);

  // good

  class Controller {}

  Controller.$inject = [];

  angular.controller('controller', Controller);

  ```

## Naming

  - **Extensions**: Use `.controller.js` extension for controllers.
  - **Extensions**: Use `.route.js` extension for routes.
  - **Extensions**: Use `.config.js` extension for config.
  - **Extensions**: Use `.js` extension for module declaration.


## Declaration

  - **Modules**:

    ```javascript
    // good

    import angular from 'angular';
    import appRoutes from 'app.route';
    import appController from 'app.controller';

    const MODULE_NAME = 'app';
    const MODULE_DEPENDENCIES = [];

    angular.module(MODULE_NAME, MODULE_DEPENCIES)
           .config(appRoutes)
           .controller(appController.NAME, appController);

    export default ReservationCard;
    ```

**[⬆ back to top](#table-of-contents)**
