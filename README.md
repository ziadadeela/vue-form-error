
# vue-form-error
[![NPM Version](https://img.shields.io/npm/dt/vue-form-error.svg)](https://www.npmjs.com/package/vue-form-error)[![npm-version](https://img.shields.io/npm/v/vue-form-error.svg)](https://www.npmjs.com/package/vue-form-error)[![license](https://img.shields.io/npm/l/vue-form-error.svg)](https://yarnpkg.com/en/package/vue-form-error)

A simple Vuejs component that can be used to display form validation errors  on inputs.


## Installation
```
npm install vue-form-error --save
```

## Usage

```html
<template>
    <div>
        <FormError :errors="formErrors.name">
            <label for="Name">Name</label>
            <input type="text" class="form-control" id="Name"
                   placeholder="Name">
        </FormError>
    </div>
</template>

<script>
    // Import component
    import FormError from 'vue-form-error';
    
    export default {
        data() {
            return {
                formErrors:{}
            }
        },
        components: {
            FormError
        },
        methods: {
        }
    }
</script>
```

## Run Examples Locally

- Clone this repo
- Install dependencies: **npm install**
- Run dev server and it will open on http://localhost:8080 : **npm run serve** 

## License
```
Released under the MIT License.
```
