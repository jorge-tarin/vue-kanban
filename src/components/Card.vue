<template>
    <div class="card">
        <slot />
    </div>
</template>

<style scoped>
.card{
    background: var(--color-white);
    padding: 1.4rem;
    border-radius: 0.4rem;
    box-shadow: 0 1px 0 rgba(9, 30, 65, 0.25);
    margin: 0.8rem;
    font-size: 1.6rem;
    cursor: pointer;
}
</style>