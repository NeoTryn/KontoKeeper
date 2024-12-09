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
* {
    font-family: "Inter", sans-serif;
}
</style>