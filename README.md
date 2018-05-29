# ng-number-picker
[![Build Status](https://api.travis-ci.org/wajdibeltaifa/ng-number-picker.svg?branch=master)](https://travis-ci.org/wajdibeltaifa/ng-number-picker)
[![License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](http://www.opensource.org/licenses/MIT)
[![NPM Release](https://img.shields.io/npm/v/ng-number-picker.svg?style=flat-square)](https://www.npmjs.com/package/ng-number-picker)
[![NPM Monthly Downloads](https://img.shields.io/npm/dm/ng-number-picker.svg?style=flat-square)](https://www.npmjs.com/package/ng-number-picker)

> A number picker input for `angular 2+` & `bootstrap 4+`. It supports the mousewheel and the up/down keys.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

## Try it
Try it on: [Plunker](https://embed.plnkr.co/JUEIfo/)
## Requirements

1. `Angular` ≥ `2.0`
1. `Bootstrap` ≥ `4.x`

## Installation
Run `npm install --save ng-number-picker` from the command line, then import the `NgNumberPickerModule` into your `appModule` : 
```javascript
import {NumberPickerModule} from 'ng-number-picker';

@NgModule({
  imports: [
    NumberPickerModule
  ],
  ...
  ...
})
```

Run `npm install --save bootstrap` from the command line to install `Bootstrap` ≥ `4.x`, then include the style into your `angular.json` file (or `angular-cli.json` for `angular` version < 6.0) similar to the following:

```javascript
"styles": [
  "node_modules/bootstrap/dist/css/bootstrap.min.css"
],
...
```
## Usage
Add the following line into your html template :
```html
<ng-number-picker [(value)]="value"></ng-number-picker>
```
## Options
The following options are the available component inputs : 

| INPUT        | TYPE | DEFAULT | DISCRIPTION |
| ------------- | :-------------: | :-------------: |:-------------|
| `min`   | `number` | `0` | Minimum value |
| `max`   | `number` | `100` | Maximum value |
| `step`   | `number` | `1` | The step value for up/down change |
| `value`   | `number` |  `null` | Initial input value |
| `pickStartAfter`   | `number` | `500` | The time in milliseconds before start picking values. Used when holding click on up/down buttons. |
| `pickTimer` | `number` | `100` | The time in milliseconds for step auto incrementation/decrementation. Used when holding click on up/down buttons. |
| `prefix`   | `string` | `null` | Text value before the input |
| `postfix`   | `string` | `null` | Text value after the input |
| `placeholder`   | `string` | `null` | Input placeholder |
| `size`   | `sizeType` | `md` | The input size. Please take a look at [the available size types](https://github.com/wajdibeltaifa/ng-number-picker/blob/cf3d0ec9d2f1ac1d94ebd2107df406d50dd988bc/src/lib/number-picker.config.ts#L4). |
| `buttonsOrientation`   | `buttonsOrientationType` | `h` | The orientation strategy for up/down buttons. Please take a look at [the available orientation types](https://github.com/wajdibeltaifa/ng-number-picker/blob/cf3d0ec9d2f1ac1d94ebd2107df406d50dd988bc/src/lib/number-picker.config.ts#L3).|
| `customClass`   | `CustomClasses` | `{}` | Set custom css classes around the component. Please take a look at [the available custom classes options](https://github.com/wajdibeltaifa/ng-number-picker/blob/cf3d0ec9d2f1ac1d94ebd2107df406d50dd988bc/src/lib/number-picker.config.ts#L6).| |
| `mouseWheel`   | `boolean` | `false` | Enable/disable change input value with mouseWheel|
| `arrowKeys`   | `boolean` | `true` | Enable/disable change input value with up/down arrow keys |
| `inputReadOnly`   | `boolean` | `false` | Readonly input |
| `showUpButton`   | `boolean` | `true` | Show/hide upward button |
| `showDownButton`   | `boolean` | `true` | Show/hide downword button |


## Events
**Triggered events**

The following events are triggered on the input and can be listened on.

| EVENT        | DISCRIPTION |
| ------------- |:-------------:|
| `valueChange`   | Triggered when the value is changed with one of the +/- buttons |
| `minReached`      | Triggered when the input value hit the limit set by the `min` option |
| `maxReached`   | Triggered when the input value hit the limit set by the `max` option |
| `pickStarted`   | Triggered when start picking numbers upwards or downwards |
| `pickStoped`   | Triggered when stop picking numbers upwards or downwards |
| `pickUpStarted`   | Triggered when start picking numbers upwards |
| `pickUpStoped`   | Triggered when stop picking numbers upwards |
| `pickDownStarted`   | Triggered when start picking numbers downwards |
| `pickDownStoped`   | Triggered when stop picking numbers downwards |

