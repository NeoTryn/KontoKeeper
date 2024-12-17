<template>
    <header class="nav-header">
        <ul class="nav-list">
            <li class="nav-element">
                <NuxtLink class="nav-link" to="/login">Log In or Sign Up</NuxtLink>
            </li>
            <li class="nav-element"><NuxtLink class="nav-link" to="/about">About KontoKeeper</NuxtLink></li>
        </ul>
    </header>
    <slot></slot>
</template>

<style>
@import url('./../assets/palette.css');

:root {
    --transition-time: 100ms;
}

* {
    font-family: "Montserrat",  sans-serif;
    font-weight: 300;
    font-style: normal;
    margin: 0;
    padding: 0; 
}

.nav-header {
    position: fixed;
    width: 100vw;
    height: 10vh;

    background-color: var(--primary-dark);
}

.nav-list {
    display: flex;
    flex-direction: row;

    justify-content: left;
    align-items: center;

    width: 100%;
    height: 100%;

    gap: 2rem;

    list-style-type: none;
}

.nav-element {
    margin-left: 1rem;
}

.nav-link {
    text-decoration: none;

    color: whitesmoke;
    font-size: large;

    transition: color var(--transition-time) ease-in;
}

.nav-link:hover {
    color: var(--primary);
}
</style>