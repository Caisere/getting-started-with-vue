<template>
    <form @submit.prevent="handleSubmit">
        <div>
            <label for="name">Name</label>
            <input type="text" placeholder="Enter your name" name="name" id="name" />
        </div>
        <div>
            <label for="email">Email</label>
            <input type="email" placeholder="Enter your email" name="email" id="email" />
        </div>
        <div>
            <label for="password">Password</label>
            <input type="password" placeholder="Enter your password" name="password" id="password" />
        </div>
        <button type="submit">Submit</button>
    </form>

    <div v-show="showInfo">
        <p>Name: {{ name }}</p>
        <p>Email: {{ email }}</p>
        <p>Password: {{ password }}</p>
    </div>
</template>

<script>
    export default {
        name: 'FormComponent',
        data() {
            return {
                name: '',
                email: '',
                password: '',
                showInfo: false
            }
        },
        methods: {
            handleSubmit (event) {
                // event.preventDefault();
                // Handle form submission logic here
                const formData = new FormData(event.target);
                this.name = formData.get('name');
                this.email = formData.get('email');
                this.password = formData.get('password');
                this.showInfo = true;
                console.log(`Name: ${this.name}, Email: ${this.email}, Password: ${this.password}`);
            }
        },
    }
</script>

style <style scoped>
    form, div {
        display: flex;
        flex-direction: column;
        width: 300px;
        margin: 0 auto;
    }

    label {
        margin-bottom: 5px;
        font-weight: bold;
    }
    
    input {
        margin-bottom: 10px;
        padding: 8px;
        border: 1px solid #ccc;
        border-radius: 4px;
    }
    
    button {
        padding: 10px;
        background-color: #42b983;
        color: white;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }
    
    button:hover {
        background-color: #369f7a;
    }

    p {
        font-weight: bold;
        font-size: 16px;
    }
</style>