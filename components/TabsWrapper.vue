<template>
    <div class="tabs">
        <ul class="tabs__header">
            <li 
                v-for="title in tabTitles" :key="title" @click="selectedTitle = title" :class="{selected: title === selectedTitle}"
            >
                {{ title }}
            </li>
        </ul>
        <slot />
    </div>
</template>

<style>
    .tabs {
        max-width: 1230px;
        margin: 0 auto;
    }

    .tabs__header {
        margin-bottom: 10px;
        list-style: none;
        padding: 0;
        display: flex;
    }

    .tabs__header li {
        position: relative;
        border-radius: 4px;
        white-space: nowrap;
        color: #9c9c9c;
        font-size: 18px;
        user-select: none;
        position: relative;
        padding-bottom: 5px;
        font-weight: 500;
        cursor: pointer;
    }

    .tabs__header li:not(:last-of-type) {
        margin-right: 0.5rem;
    }

    .tabs__header li.selected {
        border-radius: 0;
        color: #000;
    }

    .tabs__header li:hover {
        color: #080808;
    }

    .tabs__header li::after {
        content: '';
        background-color: currentColor;
        bottom: 0;
        content: "";
        height: 2px;
        left: 0;
        position: absolute;
        width: 0;
        transition: width .2s ease-in-out;
    }

    .tabs__header li.selected::after {
        width: 100%;
        background-color: #080808;
    }

</style>

<script>
    import { ref, provide } from 'vue';
    export default {
        setup (props, {slots}) {
            const tabTitles = ref(slots.default().map((tab) => tab.props.title));
            const selectedTitle = ref(tabTitles.value[0]);

            provide('selectedTitle', selectedTitle);
            return {
                selectedTitle,
                tabTitles,
            };
        }
    }
</script>