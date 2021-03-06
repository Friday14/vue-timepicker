# vue-timepicker
[![npm](https://img.shields.io/npm/dw/vue-simple-timepicker.svg)]()

Simple vue timepicker

## Screenshot
<img src="https://image.prntscr.com/image/Y0-gz4YyTiy_LfXlsAFPJw.png">

## Future
1. Switch AM/PM time
3. update styles

## Install
_npm i vue-simple-timepicker --save_

## Usage

```Vue
<template>
  <div id="app">
      <Timepicker v-model="timepicker" :options="pickerSetting"></Timepicker>
      
      <!-- View time -->
      <div>
        {{ timepicker.hours }} : {{ timepicker.minutes }}
      </div>
  </div>
</template>

<script>
  import Timepicker from 'vue-simple-timepicker';

  export default {
    name: 'app',
    components: {Timepicker},
    data() {
        return {
            timepicker: {
                hours: 0,
                minutes: 0,
            },
            pickerSetting: {
              headerShow: false,
            },
        }
    }
  };
</script>
```
### Options
**_Default Options:_**
```js
options : {
  headerShow: true, /* Show/Hide Header  */
  headerText: 'Friday Time Picker' /* Text Header a Picker */
};
```

_**Usage Custom options:**_

<Timepicker **_:options="pickerSetting"_**></Timepicker>

To use the settings you need to send them to the component as shown above

**_Custom trigger:_**
```vue
<Timepicker v-model="picker" :options="pickerSetting">
  <div>Click for show timepicker!</div>
</Timepicker>
```
