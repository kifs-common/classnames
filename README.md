# React-Context-Reducer

[![Release](https://badgen.net/github/release/kifs-common/classnames/main)](https://www.npmjs.com/package/@kifs-common/classnames)
[![Minified](https://badgen.net/bundlephobia/min/@kifs-common/classnames)](https://bundlephobia.com/package/@kifs-common/classnames)
[![Minified + zip](https://badgen.net/bundlephobia/minzip/@kifs-common/classnames)](https://bundlephobia.com/package/@kifs-common/classnames)
[![Dependencies](https://badgen.net/github/dependents-pkg/kifs-common/classnames)](https://bundlephobia.com/package/@kifs-common/classnames)
[![Tech Debt](https://badgen.net/codeclimate/tech-debt/kifs-common/classnames)](https://codeclimate.com/github/kifs-common/classnames)
[![Maintainability](https://badgen.net/codeclimate/maintainability/kifs-common/classnames)](https://codeclimate.com/github/kifs-common/classnames)

Lightweight – no dependencies – functions helper to handle classnames.

## Install

- `npm i @kifs-common/classnames`

## Usage

```js
import { join, } from '@kifs-common/classnames'

console.log(join())
// -> undefined

console.log(join('hello', 'world'))
// -> "hello world"

const hero = {
  firstname: 'Gerard',
  lastname: 'Pichon'
}
console.log(join(obj.firstname, obj.age, false, !obj.age && obj.lastname))
// -> "Gerard Pichon"
```

This is pretty usefull in a css-module context like:

```js
import { join, } from '@kifs-common/classnames'

import style from 'style.css'

function createButton (color, disabled) {
  const button = document.createElement('button')
  button.className = join(style.button, style[color || 'primary'], disabled && style.disabled)
  return button
}

// Or JSX/react

function renderButton (color, disabled) {
  return (
    <button
      className={join(
        style.button,
        style[color || 'primary'],
        disabled && style.disabled
      )}>
    </button>
  )
}

```
