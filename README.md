# React imagesLoaded

<small>The [imagesLoaded](http://imagesloaded.desandro.com) library as a React Component</small>

## Current API
<small>Still missing some implementation details, but events is currently working.</small>

<strong>Props</strong>

If you want to change the element type of the imagesLoaded container,
you can set `elementType` as a prop on ` <ImagesLoaded />`

<strong>Events</strong>

```
onAlways(instance)

onProgress(instance, image)

onFail(instance)

done(instance)
```

## Example usage

```jsx
import React, { Component } from 'react';
import ImagesLoaded from 'react-images-loaded';

class App extends Component {
  handleOnAlways = (instance) => {

  }

  handleOnProgress = (instance, image) => {

  }

  handleOnFail = (instance) => {

  }

  handleDone = (instance) => {

  }

  render() {
    return (
      <ImagesLoaded
        elementType={"ul"} // defaults to 'div'
        onAlways={this.handleOnAlways}
        onProgress={this.handleOnProgress}
        onFail={this.handleOnFail}
        done={this.handleDone}
      >
        {/* Your images */}
      </ImagesLoaded>
    );
  }
}
```

## install and Contribute
Defaulting to yarn, but npm works just as well.

```
$ git clone https://github.com/oyvindhermansen/react-images-loaded.git
$ cd react-images-loaded
$ yarn install
```

<strong>Local development</strong>

Developing on this repo locally is a breeze. Just run `yarn demo`, and the webpack-dev-server will render demo. Here you can make changes in `/src`-folder and it will hot reload into the demo-page. Same goes for changes from `/demo/demo.js`.

<strong>Testing</strong>

Using `jest` because it's the `best` ;)

`yarn test` for running the tests one time.
`yarn test:watch` for running tests in watch mode

<strong>Contribute</strong>

Feel free to make pull requests or issues if something doesn't work/could be better :)
