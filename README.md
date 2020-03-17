# babel-plugin-polished-fork

Compile away [polished](https://polished.js.org/) helpers.
This is a fork from the original package to overcome dependency stuck at v.1.0.0 of polished package.

## Installation

```sh
$ npm install  babel-plugin-polished-fork

```

or

```sh
$ yarn add  babel-plugin-polished-fork

```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  	"plugins": [
		[
			"babel-plugin-polished-fork",
			{
				"module": "polished"
			}
		]
	]
}
```

### Via CLI

```sh
$ babel --plugins polished script.js
```

## Example

**In**

```js
import * as polished from 'polished';

let value = polished.clearFix();
```

or

```js
import { clearFix } from 'polished';

let value = polished.clearFix();
```

**Out**

```js
let value = {
  '&::after': {
    clear: 'both',
    content: '',
    display: 'table'
  }
};
```