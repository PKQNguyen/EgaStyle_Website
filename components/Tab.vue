<template>
    <div class="tab-content" v-show="title == selectedTitle">
       
        <slot />
    </div>
</template>
<style>
    .tab-content {
        margin-top: 30px;
    }
</style>
<script>
import { inject } from 'vue';
export default {
    props: ['title'],
    setup () {
        const selectedTitle = inject('selectedTitle');

        return {
            selectedTitle,
        }
    }
}
</script>