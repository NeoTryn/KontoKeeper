<template>
    <div class="container">
        <div class="flex">
            <form name="login-form" id="login-form">
                <input type="text" id="username">
                <input type="password" id="password">
                <button type="submit" id="login">Log In</button>
            </form>
            <form name="signup-form" id="signup-form">
                <input type="text" id="username-signup">
                <input type="email" id="email">
                <input type="text" id="full-name">
                <input type="password" id="password-signup">
                <button type="submit" id="signup">Sign Up</button>
            </form>
            <button id="login-switch">Switch to Log-In</button>
            <button id="signup-switch">Switch to Sign-Up</button>
        </div>
    </div>
</template>

<style>
    .container {
        position: absolute;
        width: 100%;
        height: 100%;

        display: flex;
        align-items: center;
        justify-content: center;
    }

    .flex {
        min-width: 30%;
        min-height: 25%;
        width: fit-content;
        height: fit-content;

        display: flex;
        flex-direction: row;

        gap: 2rem;

        justify-content: center;
        align-items: center;

        background-color: var(--purple_light);
        border: 0.3rem solid var(--purple);
        border-radius: 2rem;
    }

    form {
        display: grid;
        grid-template-rows: repeat(3, 1fr);
        gap: 0.7rem;

        width: 25%;
    }

    @keyframes switch {
        from {
            visibility: hidden;
        }
        to {
            visibility: visible;
        }
    }

    #signup-form {
        animation: switch 1000000ms ease-out;
        animation-fill-mode: backwards;
    }
</style>