<template>
    <header>
        <ul>
            <li><NuxtLink to="/login">Log In or Sign Up to KontoKeeper</NuxtLink></li>
            <li><NuxtLink to="/about">About KontoKeeper</NuxtLink></li>
        </ul>
    </header>
    <slot />
</template>

<style>
@import url('./../assets/palette.css');

* {
    font-family: "Inter", sans-serif;
    color: var(--grey);
    margin: 0;
    padding: 0;
}
</style>