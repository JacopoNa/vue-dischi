<template>
    <div>
        <header></header>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
    @import '../scss/variables.scss';
    header {
        height: 80px;
        background-color: $_primaryColor;
    }
</style>