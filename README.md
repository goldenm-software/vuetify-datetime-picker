
# vuetify-datetime-picker

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/goldenm-software/vuetify-datetime-picker/blob/master/LICENSE)
[![npm version](https://img.shields.io/npm/v/@goldenm/vuetify-datetime-picker.svg?style=flat)](https://www.npmjs.com/package/@goldenm/vuetify-datetime-picker)

DatetimePicker component for Vuetify.js.

## Credits
Credits for the original library author <b>[Darren Fang](https://github.com/darrenfang/vuetify-datetime-picker)</b>
## Installation

```shell
npm install --save vuetify-datetime-picker

or

yarn add vuetify-datetime-picker
```

```js
import Vue from 'vue'
import DatetimePicker from 'vuetify-datetimepicker'
// (Optional) import 'vuetify-datetimepicker/src/scss/main.scss'

Vue.use(DatetimePicker)
```

If use the `main.scss`, you should configure the `sass-loader` in `webpack.config.js`, or just ignore this style sheet.

## Usage

Once installed, it can be used in a template as simply as:

```html
<v-datetime-picker label="Select Datetime" v-model="datetime"> </v-datetime-picker>
```

## Properties

| Name             | Type        | Default Value | Description                                                                                                 |
| ---------------- | ----------- | ------------- | ----------------------------------------------------------------------------------------------------------- |
| datetime (model) | Date/String |               | Time picker model.                                                                                          |
| disabled         | Boolean     | false         | Input is disabled.                                                                                          |
| loading          | Boolean     | false         | Input is loading.                                                                                           |
| label            | string      |               | Sets input label.                                                                                           |
| dialogWidth      | Number      | 340           | The width of the dialog.                                                                                    |
| dateFormat       | string      | yyyy-MM-dd    | Defines the format of a date.                                                                               |
| timeFormat       | string      | HH:mm         | Defines the format of a time.                                                                               |
| clearText        | string      | CLEAR         | Sets the text of the clear button.                                                                          |
| okText           | string      | OK            | Sets the text of the ok button.                                                                             |
| textFieldProps   | Object      |               | Text fields properties. See [Vuetify Docs](https://vuetifyjs.com/en/components/text-fields 'Vuetify Docs')  |
| datePickerProps  | Object      |               | Date pickers properties.See [Vuetify Docs](https://vuetifyjs.com/en/components/date-pickers 'Vuetify Docs') |
| timePickerProps  | Object      |               | Time pickers properties.See [Vuetify Docs](https://vuetifyjs.com/en/components/time-pickers 'Vuetify Docs') |
| solo             | Boolean     | false         | Text field style. See [Vuetify Docs](hhttps://vuetifyjs.com/en/components/text-fields 'Vuetify Docs')       |
| outlined         | Boolean     | false         | Text field style. See [Vuetify Docs](hhttps://vuetifyjs.com/en/components/text-fields 'Vuetify Docs')       |

## Events

| Name  | Arguments           | Description             |
| ----- | ------------------- | ----------------------- |
| input | value (Date/String) | The updated bound model |

## Slots

| Name     | Description                                                                                 |
| -------- | ------------------------------------------------------------------------------------------- |
| dateIcon | Slot to put custom icon in the date tab.                                                    |
| timeIcon | Slot to put custom icon in the time tab.                                                    |
| actions  | Slot to put custom buttons in the dialog.                                                   |
| progress | Slot for custom progress linear (displayed when loading prop is not equal to Boolean False) |
