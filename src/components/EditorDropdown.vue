<template>
    <div class="edt-dropdown">
        <slot></slot>
    </div> 
</template>
<script>
export default {
    
}
</script>
<style>
.edt-dropdown{
    position: absolute;
    background: #fff;
    left: 0;
    top: 35px;
    border-radius: 4px;
    border: 1px solid #eeeff1;
    box-shadow: 0 0 4px rgba(0,0,0,.05);
}
.edt-dropdown :before {
    content: '';
    width: 100%;
    height: 15px;
    background: red;
    position: absolute;
    left: 0;
    top: -15px;
    opacity: 0;
}
</style>
