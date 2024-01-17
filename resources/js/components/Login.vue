<template>
    <div>
        <h2>Login</h2>
        <form @submit.prevent="login">
        <div class="form-group">
            <label for="username">Username:</label>
            <input
                type="text"
                id="username"
                v-model="username"
                class="form-control"
                required
            />
        </div>
        <div class="form-group">
            <label for="password">Password:</label>
            <input
                type="password"
                id="password"
                v-model="password"
                class="form-control"
                required
            />
        </div>
        <button type="submit" class="btn btn-primary">Login</button>
    </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                username: '',
                password: ''
            };
        },
        methods: {
            login() {
                // Authentication logic
                console.log('Logging in with:', this.username, this.password);
            }
        }
    };
</script>

