<template>
    <div class="img-container" :style="styleObject">
        <img id="outputImage"> {{displayImage}}
    </div>
</template>

<script>
export default {
    props: {
        displayImage: {
            type: String
        },
        conainterHeight: {
            type: Number,
            default: 200
        }
    },
    computed: {
        styleObject: function(){
            return{
                height: this.containerHeight + 'px'
            }
        }
    }
}
</script>

<style>
    .img-container{
        border: 1px dotted grey;
        overflow: hidden;
        margin: 5px 0;
        /* height: 350px; */
    }
</style>