<template>
    <ul class="edt-fontcolor">
        <li @click="setColor('#1d8ce0')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#41b883')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#ffa000')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#f60000')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#f0e02f')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#00dc77')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#e6e41c')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#e026a0')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#555555')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#324057')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#8492a6')">
            <button class="btn"></button>
        </li>
        <li @click="setColor('#99a9bf')">
            <button class="btn"></button>
        </li>
    </ul>
</template>
<script>
export default {
    methods: {
        setColor: function (valueArgument) {
            if (!valueArgument) {
                valueArgument = null
            }
            document.execCommand('foreColor', false, valueArgument)
        }
    }
}
</script>
<style>
    .edt-fontcolor{
        margin: 3px;
        width: 107px;
        padding: 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    .edt-fontcolor li{
      float: left;
      width: 20px;
      height: 20px;
      background: black;
      margin: 3px;
      border-radius: 2px;
    }
    .edt-fontcolor li:nth-child(1){
        background-color: #1d8ce0;
      }
    .edt-fontcolor li:nth-child(2){
        background-color: #41b883;
      }
    .edt-fontcolor li:nth-child(3){
        background-color: #ffa000;
      }
    .edt-fontcolor li:nth-child(4){
        background-color: #f60000;
      }
    .edt-fontcolor li:nth-child(5){
        background-color: #f0e02f;
      }
    .edt-fontcolor li:nth-child(6){
        background-color: #00dc77;
      }
    .edt-fontcolor li:nth-child(7){
        background-color: #e6e41c;
      }
    .edt-fontcolor li:nth-child(8){
        background-color: #e026a0;
      }
    .edt-fontcolor li:nth-child(9){
        background-color: #555555;
      }
    .edt-fontcolor li:nth-child(10){
        background-color: #324057;
      }
    .edt-fontcolor li:nth-child(11){
        background-color: #8492a6;
      }
    .edt-fontcolor li:nth-child(12){
        background-color: #99a9bf;
    }
    .btn{
        width: 100%;
        height: 100%;
        border: none;
        background: transparent;
    }
</style>
