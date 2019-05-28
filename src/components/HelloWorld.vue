<template>
    <div id="ckEditor">
        
    </div>
</template>

<script>
import ClassicEditor from '@ckeditor/ckeditor5-editor-classic/src/classiceditor';
import Essentials from '@ckeditor/ckeditor5-essentials/src/essentials';
import Paragraph from '@ckeditor/ckeditor5-paragraph/src/paragraph';
import Bold from '@ckeditor/ckeditor5-basic-styles/src/bold';
import Italic from '@ckeditor/ckeditor5-basic-styles/src/italic';

export default {
  name: "app",
  data() {
    return {};
  },
  mounted() {
    ClassicEditor.create(document.getElementById("ckEditor"), {
      plugins: [Essentials, Paragraph, Bold, Italic],
      toolbar: ["bold", "italic"]
    })
      .then(editor => {
        console.log(editor);
      })
      .catch(e => {
        console.log(e);
      });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

