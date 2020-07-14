<template>
    <footer>
        <!-- nested content will not show without slot -->
        <slot name="app-name">
            <!-- fallback content -->
            <!-- if the content is not immediately available-->
            <p>Footer text</p>
        </slot>
        <!-- renders rest -->
        <slot></slot>
    </footer>    
</template>

<script>
export default {

}
</script>

<style>

</style>