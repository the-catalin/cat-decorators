<!--
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/the-catalin/cat-decorators)
-->
# cat-decorators

`cat-decorators` is a helper element that allows you to decorate Polymer elements.

includes:
`cat-border`
`cat-shadow`
`cat-position`

## Demo

Currently, there is no dedicated demo, but the above decoratrs are used in the [Live Demo](http://webcomponents.online/cat-image/) of [cat-image](https://www.webcomponents.org/element/the-catalin/cat-image)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install --save cat-decorators
```

Or [download as ZIP](https://github.com/the-catalin/cat-decorators/archive/master.zip)

## Usage

1. Import Web Components' polyfill (if needed):

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import behavior and decorators:

    ```html
    <!-- Import the behavior that allows you to add decorators to your elements -->
    <link rel="import" href="bower_components/cat-decorators/cat-decorator-runner-behavior.html">

    <!-- Import the decorators that you want to use: -->
    <link rel="import" href="bower_components/cat-decorators/decorators/cat-border.html">
    <link rel="import" href="bower_components/cat-decorators/decorators/cat-shadow.html">
    <link rel="import" href="bower_components/cat-decorators/decorators/cat-position.html">
    ```

3. Add `CatDecoratorRunnerBehavior` to your Polymer element:

	```js
	Polymer({      

	    is: 'my-custom-element',

	    behaviors: [Polymer.CatDecoratorRunnerBehavior],

	    properties: {
	    	...
	    }
	    ...
	```

4. Initialize an element with a desired decorators:

	```js
	this.addDecorator({
	    name: 'cat-border',
		node: this,
		color: '#777',
		width: 3,
		side: 'all',
		radius: 4
	});
	```
	
	'node' can be `this` (the Polymer element itself), or any other element inside it.


## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## History

For detailed changelog, check [Releases](https://github.com/the-catalin/cat-decorators/releases).

## License

[The MIT License (MIT)](https://opensource.org/licenses/MIT)

Copyright (c) 2017 Catalin Ungureanu