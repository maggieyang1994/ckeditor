<template>
  <div id='ckEditor'>
    <ckeditor :editor='editor' v-model='editorData' :config='editorConfig'></ckeditor>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      editor: window.ClassicEditor,
      editorData: '<p>Content of the editor.</p>',
      editorConfig: {
        toolbar: {
          items: ['bold', 'italic', 'link', 'undo', 'redo']
        }
      }
    }
  }
}
</script>
