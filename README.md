# persian-datetime-picker-vue2 (based on dayjs)

[![npm version](https://badge.fury.io/js/persian-datetime-picker-vue2.svg)](https://www.npmjs.com/package/persian-datetime-picker-vue2)

> A vue plugin to select jalali date and time based on `dayjs`

See documentation and demo at [vue-persian-datetime-picker](https://talkhabi.github.io/vue-persian-datetime-picker)

If you are using vuejs 3, please refer to [this repository](https://github.com/imanmalekian31/vue3-persian-datetime-picker).

## Installation

### browser

```html
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/dayjs/1.11.5/dayjs.min.js"></script>
<script src="/dist/persian-datetime-picker-vue2.umd.min.js"></script>
<div id="app">
  <date-picker v-model="date"></date-picker>
</div>
<script>
  var app = new Vue({
    el: '#app',
    data: {
      date: '1401/08/02'
    },
    components: {
      DatePicker: VuePersianDatetimePicker
    }
  })
</script>
```

### npm

```bash
npm install persian-datetime-picker-vue2 --save
```

### Usage

```javascript
// main.js
//...
import VuePersianDatetimePicker from 'persian-datetime-picker-vue2'
Vue.component('date-picker', VuePersianDatetimePicker)
//...
```

Or in component

```html
<template>
  <div>
    <date-picker v-model="date"></date-picker>
  </div>
</template>

<script>
  import VuePersianDatetimePicker from 'persian-datetime-picker-vue2'
  export default {
    data() {
      return {
        date: ''
      }
    },
    components: {
      datePicker: VuePersianDatetimePicker
    }
  }
</script>
```

## You can also set default values:

```javascript
// main.js
import VuePersianDatetimePicker from 'persian-datetime-picker-vue2'
Vue.use(VuePersianDatetimePicker, {
  name: 'custom-date-picker',
  props: {
    inputFormat: 'YYYY-MM-DD HH:mm',
    format: 'YYYY-MM-DD HH:mm',
    editable: false,
    inputClass: 'form-control my-custom-class-name',
    placeholder: 'Please select a date',
    altFormat: 'YYYY-MM-DD HH:mm',
    color: '#00acc1',
    autoSubmit: false
    //...
    //... And whatever you want to set as default
    //...
  }
})
```

Then use in component

```html
<custom-date-picker v-model="date" />
```

### [Click to see full documentation and demo](https://talkhabi.github.io/vue-persian-datetime-picker)

## License

This project is licensed under the MIT License
