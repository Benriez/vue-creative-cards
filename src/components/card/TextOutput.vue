<template>
    <div>
        <p :style="styleObject">
            {{displayText}}
        </p>
    </div>
</template>

<script>
export default {
    //props passes data from parent to child component
    props: {
        //data validation
        displayText: [String],
        //because more then 1 type of validation
        //this needs to me an object
        containerHeight: {
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


<style scoped>
    p {
        font-family: 'Tangerine', cursive;
        font-size: 42px;
        line-height: 42px;
        text-shadow: 2px 2px 2px #aaa;
        color: #4d4d4d;
        margin: 5px 0;
        border: 1px dotted grey;
        white-space: pre-line;
        overflow: hidden;
    }
</style>