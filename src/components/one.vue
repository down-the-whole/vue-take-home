<template>
    <div class="box border">
        <div v-for="item in parentData" v-bind:key="item">
            {{ item }}
        </div>
    </div>
</template>

<script lang="ts">
export default {
    name: 'One',
    props: ['parentData']
}
</script>

<style lang="scss">
.border{
    border: 1px solid black;
}
</style>
