<template>
  <div id="editor"></div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Editor from '@toast-ui/editor';
import 'codemirror/lib/codemirror.css'; // Editor's Dependency Style
import '@toast-ui/editor/dist/toastui-editor.css'; // Editor's Style



export default defineComponent({
  name: 'App',
  components: {
       
  },
  mounted(){
    const editor = new Editor({
    el: document.querySelector('#editor'),
    height: '500px',
    initialEditType: 'markdown',
    previewStyle: 'vertical'
  });
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>