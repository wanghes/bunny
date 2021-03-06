
# BunnyJS v 0.9.63

## ES6 browser framework

#### "It's like a next-generation jQuery with jQuery UI"

[![NPM downloads/month](http://img.shields.io/npm/dm/bunnyjs.svg?style=flat-square)](https://www.npmjs.org/package/bunnyjs) [![NPM version](http://img.shields.io/npm/v/bunnyjs.svg?style=flat-square)](https://www.npmjs.org/package/bunnyjs)

For help & ideas - [DM me on Twitter](https://twitter.com/Mevrael)


Lightweight native JavaScript and ECMAScript 6 library and next generation front-end framework. BunnyJS is package of small stand-alone components without dependencies:

1. Powerful native lightweight JavaScript Form processing with native API, AJAX submit, file upload, image preview, data binding and more.
2. Powerful native lightweight JavaScript HTML5 validation
3. DOM utils, ready()
4. Libraries for Date, URL, File, Image
5. Ajax
6. Routing
7. Template engine
8. DataTable and Pagination
9. Calendar and DatePicker
10. Autocomplete, Dropdown
11. Element, positions, coordinates, smooth scrolling
12. Dependency Injection, Inversion of control

Architecture:

1. Separation of concerns, loose coupling, modularity
2. Functional programming
3. ES6 import/exports, Promises
4. Native Browser API, polyfills were needed
5. Object literal notation, no prototypes, "classes" , "new"
6. Object composition over inheritance
7. Dependency injection

Browser Support: IE9+, last 2 versions of Chrome, Firefox, Safari, Android 4.4+, iOS 9+

Designed in mind for best compatibility with Laravel 5 and Bootstrap 4, however can be used anywhere.

Rollup.js with babel and npm plugins is recommended for transpiling and bundling.

Install via `npm install bunnyjs --save`

Example usage:

```javascript
import { Route } from 'bunnyjs/src/bunny.route';

Route.get('/', function() {
    console.log('You are on main page!');
});

// or create your own functions/closures/controllers, import them and pass to route
import { UsersController } from './Controllers/UsersController';
Route.get('/users', UsersController.index);
Route.get('/users/{id}', UsersController.showUser);
```

For documentation go to Wiki.

Currently only [Template documentation](https://github.com/Mevrael/bunny/wiki/Template) available.

There is also [example](https://github.com/Mevrael/bunny/blob/master/examples/container/index.js) for IOC Container.

[Autocomplete example](http://htmlpreview.github.io/?https://github.com/Mevrael/bunny/blob/master/examples/autocomplete/index.html)


Valdiator is only 150 lines and adds JS validation above native HTML5 valdiation attributes. For example,
```html
<input type="file" accept="image/*" ... required>
``` 
will be required and only images will be accepted. Error message is displayed after input.


DatePicker by default used as a fallback for browsers not supporting `<input type="date">` and initiated using `DatePicker.create(input_id)` .

DatePicker as any BunnyJS component is easily **extendable**. Basicly DatePicker is a calendar builder/framework. You can build your own calendar and datepicker very fast.

Default theme of DatePicker:

![bunnyjs-calendar-default](https://cloud.githubusercontent.com/assets/7879528/13051623/ef4e1a62-d402-11e5-8d9c-aae0fd5494c3.png)

&copy; Mev-Rael

GPL 3.0
