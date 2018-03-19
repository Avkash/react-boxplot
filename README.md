react-boxplot
=============

Simple SVG box plots in React.

[![NPM](https://img.shields.io/npm/v/react-boxplot.svg)](https://www.npmjs.com/package/react-boxplot) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)


Install
-------

```bash
yarn add react-boxplot
npm install --save react-boxplot
```


Usage
-----

```jsx
import React, { Component } from 'react'
import { Boxplot, computeBoxplotStats } from 'react-boxplot'

const values = [
  14, 15, 16, 16, 17, 17, 17, 17, 17, 18, 18, 18, 18, 18, 18, 19,
  19, 19, 20, 20, 20, 20, 20, 20, 21, 21, 22, 23, 24, 24, 29,
];

class Example extends Component {
  render () {
    return (
      <Boxplot
        width={ 400 } height={ 20 } orientation="horizontal"
        min={ 0 } max={ 30 }
        stats={ computeBoxplotStats(values) } />
    )
  }
}
```

<img src="https://paulmelnikow.github.io/react-boxplot/example1.png" width="400">

Or you can compute the stats yourself:

```jsx
class Example extends Component {
  render () {
    return (
      <Boxplot
        width={ 400 } height={ 25 } orientation="horizontal"
        min={ 0 } max={ 300 }
        stats={ {
          whiskerLow: 194.3,
          quartile1: 201,
          quartile2: 234.5,
          quartile3: 254.6,
          whiskerHigh: 257.95,
          outliers: [ 50, 75, 184.25, 268, 290 ],
        } } />
    )
  }
}
```

<img src="https://paulmelnikow.github.io/react-boxplot/example2.png" width="400">


Features
--------

- Pure SVG.
- Horizonal or vertical orientation.
- The scale of the major axis matches the original data.


Development
-----------

```sh
yarn install
yarn start
```

Or, using npm:

```sh
npm install
npm run start
```

Contribute
----------

- [Issue tracker][issues]
- [Source code][source]

Pull requests welcome!


License
-------

The project is licensed under the two-clause BSD license.


[issues]: https://github.com/paulmelnikow/react-boxplot/issues
[source]: https://github.com/paulmelnikow/react-boxplot
