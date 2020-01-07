<template>
    <div class="edt-cont">
        <EditorHeader/>
        <EditorBody/>
    </div>
</template>
<script>
import EditorHeader from './EditorHeader.vue';
import EditorBody from './EditorBody.vue';

export default {
    components: {
        EditorHeader,
        EditorBody
    },
    data: function () {
        return {
            
        }
    },
    methods: {
    }
}
</script>
<style>
    .edt-cont {
        margin: 0 auto;
        width: 950px;
        height: 400px;
        background-color: #fff;
        border-radius: 4px;
        border: 1px solid #eeeff1;
        min-width: 900px;
        overflow: hidden;
    }  
</style>
