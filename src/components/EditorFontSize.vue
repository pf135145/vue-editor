<template>
    <ul class="edt-ul">
        <li @click="setFont('fontSize', 7)">
            <button style="font-size: 24px">7</button>
        </li>
        <li @click="setFont('fontSize', 6)">
            <button style="font-size: 22px">6</button>
        </li>
        <li @click="setFont('fontSize', 5)">
            <button style="font-size: 20px">5</button>
        </li>
        <li @click="setFont('fontSize', 4)">
            <button style="font-size: 18px">4</button>
        </li>
        <li @click="setFont('fontSize', 3)">
            <button style="font-size: 16px">3</button>
        </li>
        <li @click="setFont('fontSize', 2)">
            <button style="font-size: 14px">2</button>
        </li>
        <li @click="setFont('fontSize', 1)">
            <button style="font-size: 12px">1</button>
        </li>
    </ul>
</template>
<script>
export default {
    methods: {
        setFont(commandName, valueArgument) {
            if (!valueArgument) {
                valueArgument = null;
            }
            document.execCommand(commandName, false, valueArgument);
        },
    }
}
</script>
<style>
    .edt-ul li{
      width: 72px;
      height: 40px;
      display: flex;
      justify-content: center;
    }
    .edt-ul li:hover{
        background: #f8f8f8;
    }
    .edt-ul li button{
        color: inherit;
        flex: 1;
        width: 100%;
        height: 100%;
        background: transparent;
        border: none;
        outline: none;
        cursor: pointer;
    } 
</style>
