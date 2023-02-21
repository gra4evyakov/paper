<template>
    <button class="btn">
        <slot />
    </button>
</template>

<script>
</script>

<style scoped>
.btn {
    cursor: pointer;
    padding: 20px 65px;
    border: 1px solid #FFFFFF;
    color: #FFFFFF;
    border-radius: 30px;
    background: transparent;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.5px;
    transition: .3s;
}
.btn:hover {
    transform: scale(1.1);
}
</style>