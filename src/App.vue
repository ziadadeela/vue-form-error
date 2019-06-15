<template>
    <div id="app">
        <div id="header" class="">
            <h1>Vue Form Error</h1>
        </div>
        <div id="container">

            <div class="d-flex flex-column">
                <div class="p-2">
                    <FormError :errors="formErrors.name">
                        <label for="Name">Name</label>
                        <input type="text" class="form-control" id="Name"
                               placeholder="Name">
                    </FormError>

                </div>
                <div class="p-2">
                    <FormError :errors="formErrors.age">
                        <label for="Age">Age</label>
                        <input type="number" class="form-control" id="Age"
                               placeholder="Age">
                    </FormError>

                </div>
                <div class="p-2">
                    <FormError :errors="formErrors.email">
                        <label for="Email">Email</label>
                        <input type="email" class="form-control" id="Email"
                               placeholder="Email">
                    </FormError>

                </div>
                <div class="p-2">
                    <FormError :errors="formErrors.gender">
                        <label for="Gender">Gender</label>
                        <select name="Gender" id="Gender" class="form-control">
                            <option value="M">Male</option>
                            <option value="F">Female</option>
                        </select>
                    </FormError>

                </div>

            </div>
            <div class="d-flex flex-column align-items-end">
                <div class="p-2">
                    <div id="displayBtn">
                        <button type="button" class="btn btn-dark" @click="toggleErrors">Toggle Errors</button>
                    </div>

                </div>

            </div>

            </div>
    </div>
</template>

<script>
    import 'bootstrap/dist/css/bootstrap.min.css'

    import FormError from './components/FormError';
    import FormErrorMixin from './mixins/FormErrorMixin';

    export default {
        name: 'app',
        components: {
            FormError
        },
        mixins:[FormErrorMixin],
        data() {
            return {
                errors: {
                    name: [
                        'The name is required',
                        'The name length must be at least 8 characters'
                    ],
                    age: [
                        'The age must be a number',
                    ],
                    email: [
                        'The input must be a valid email'
                    ],
                    gender:[
                        'The gender is required'
                    ]
                }
            }
        },
        mounted() {

        },
        methods: {
            toggleErrors(){
                if(Object.keys(this.formErrors).length === 0){
                    this.formErrors = this.errors;
                }
                else{
                    this.formErrors = {}
                }
            }

        }
    }
</script>

<style>
    html{
        background: #ebebeb;

    }
    #app{
        font-family: Cambria,serif;
        background: #ebebeb;
    }
    #header {
        margin: 25px auto;
        width: 800px;
        text-align: center;
    }

    #container {
        display: flex;
        width: 500px;
        height: 550px;
        margin: 25px auto;
        box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.10);
        border: 1px solid rgba(0, 0, 0, 0.10);
        background: #fff;
        padding: 4px;
    }

</style>
