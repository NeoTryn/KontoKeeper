<script setup lang="ts">
    import { ref } from 'vue';

    let hasAccount = ref(true);
</script>

<template>
    <div class="container">
        <div class="flex">
            <form name="login-form" id="login-form" v-if="hasAccount">
                <input type="text" id="username">
                <input type="password" id="password">
                <button class="login-button" type="submit" id="login">Log In</button>
            </form>
            <form name="signup-form" id="signup-form" v-if="!hasAccount">
                <input type="text" id="username-signup">
                <input type="email" id="email">
                <input type="text" id="full-name">
                <input type="password" id="password-signup">
                <button class="login-button" type="submit" id="signup">Sign Up</button>
            </form>
            <button class="login-button" id="login-switch" v-if="!hasAccount" @click="hasAccount = true">Log-In</button>
            <button class="login-button" id="signup-switch" v-if="hasAccount" @click="hasAccount = false">Sign-Up</button>
        </div>
    </div>
</template>

<style>
    body {
        background-color: #EFF2F1;
    }

    .login-button {
        padding: 1rem 2rem 1rem 2rem;
        color: var(--primary-light);

        border-radius: 0.5rem;
        border: none;

        background-color: var(--primary);
        transition: 100ms ease-out;
    }

    .login-button:hover {
        background-color: var(--primary-mid-dark);
    }

    .container {
        margin-top: 10vh;
    }
</style>