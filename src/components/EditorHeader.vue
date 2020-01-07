<template>
    <div class="edt-header">
        <EditorBtn :conf="editorConf.bold" @click.native="execCommand('bold')"></EditorBtn>
        <EditorBtn :conf="editorConf.italic" @click.native="execCommand('italic')"></EditorBtn>
        <EditorBtn :conf="editorConf.underline" @click.native="execCommand('underline')"></EditorBtn>
        <EditorBtn :conf="editorConf.strikeThrough" @click.native="execCommand('strikeThrough')"></EditorBtn>
        <EditorBtn :conf="editorConf.fontColor">
            <EditorDropdown>
                <EditorFontColor/>
            </EditorDropdown>
        </EditorBtn>
        <EditorBtn :conf="editorConf.fontSize">
            <EditorDropdown>
                <EditorFontSize/>
            </EditorDropdown>
        </EditorBtn>
        <span class="line"></span>
        <EditorBtn :conf="editorConf.removeFormat" @click.native="execCommand('removeFormat')"></EditorBtn>
    </div>
</template>
<script>
import EditorBtn from './EditorBtn.vue';
import EditorDropdown from './EditorDropdown.vue'
import EditorFontColor from './EditorFontColor.vue'
import EditorFontSize from './EditorFontSize.vue'
import Conf from './EditorConf.js';

export default {
    components: {
        EditorBtn,
        EditorDropdown,
        EditorFontColor,
        EditorFontSize
    },
    data: function () {
        return {
            editorConf: Conf
        }
    },
    methods: {
        execCommand(commandName, valueArgument) {
            if (!valueArgument) {
                valueArgument = null;
            }
            document.execCommand(commandName, false, valueArgument);
        },
    }
}
</script>
<style>
.edt-header {
    width: 100%;
    box-sizing: border-box;
    display: flex;
    height: 40px;
    align-items: center;
    padding: 0 15px;
    background-color: #fafbfc;
    border-bottom: 1px solid #eeeff1;
    position: relative;
}
.line{
      display: inline-block;
      width: 1px;
      height: 40px;
      margin: 0 10px;
      background-color: #eeeff1;
    }
</style>
