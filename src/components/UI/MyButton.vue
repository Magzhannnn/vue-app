<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: "my-button"
}
</script>

<style scoped>
.btn {
    padding: 10px 15px;
    color: #fff;
    background-color: teal;
    border: none;
    font-size: 20px;
    border-radius: 8px;
    width: max-content;
}

.btn:hover {
    cursor: pointer;
    background-color: rgb(19, 152, 152);
}
</style>