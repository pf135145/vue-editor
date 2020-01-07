<template>
    <div class="edt-header-btn" @mouseleave="hideSlot">
        <span class="btn-cont" @click="showSlot">
            <img :src="require(`../assets/icon/${conf.cmdName}.png`)" :title="conf.title">
        </span>
        <slot v-if="show"></slot>
    </div>
</template>
<script>
export default {
    props: {
        conf: Object
    },
    data: function() {
        return {
            show: false
        }
    },
    methods: {
        showSlot () {
            this.show = this.show === false ? true : false
        },
        hideSlot () {
            this.show = false
        }   
    }
}
</script>
<style>
    .edt-header-btn {
        position: relative;
        border-radius: 4px;
        outline: 0;
        cursor: pointer;
        background-color: transparent;
        border: none;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0 5px;
        padding: 0;
    }
    .vm-editor-button:first-child {
        margin-left: 0;
    }
    .btn-cont {
        width: 24px;
        height: 24px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .btn-cont:hover{
        background-color: #eee;
    }
    .btn-cont img {
        width: 16px;
        height: 16px;
    }
</style>
