<script setup>
const props = defineProps[{
    icon:{required: true},
    title:{required: true}
}]

</script>
<template>
<div class="card-container">
    <div class="icon">{{ props.icon }}</div>
    <div class="title">{{ props.title }}</div>
</div>
</template>
<style>

</style>