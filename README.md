# vue-form-error
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
## License
```
Released under the MIT License.
```
