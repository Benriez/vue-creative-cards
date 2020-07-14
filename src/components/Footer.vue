<template>
    <footer>
        <!-- nested content will not show without slot -->
        <slot>
            <!-- fallback content -->
            <!-- if the content is not immediately available-->
            <p>Footer text</p>
        </slot>
    </footer>    
</template>

<script>
export default {
    
}
</script>

<style>

</style>