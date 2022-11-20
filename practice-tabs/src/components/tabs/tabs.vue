<script setup>
    import { ref, useContext } from 'vue';

    const selectedIndex = ref(0);
    const tabs = ref([]);
    const { slots } = useContext()

    tabs = slots
</script>

<template>
    <div>
        <ul class="tabs_header">
            <li v-for="tab in tabs" :key="tab.title">{{ tab.title }}</li>
        </ul>
        <slot></slot>
    </div>
</template>