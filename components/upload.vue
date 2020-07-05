<template>
    <div>
    <div>
    <vue-dropzone ref="myVueDropzone" id="dropzone" class="py-0" :options="dropzoneOptions" :useCustomSlot=true style="border: none">
        <b-card no-body class="pt-0 dropzoneBorder">
        <div class="dropzone-custom-content heightContent" >
            <i class='fa fa-cloud-upload fa-4x position'></i>
        <!-- <h3 class="dropzone-custom-title">Drag and drop to upload content!</h3> -->
      </div>
        </b-card>
      <b-button variant="warning" size="sm" style="marginTop: 15px; width:110px"><span style="color:white; fontSize: 12px">UPLOAD KTP</span></b-button>
    </vue-dropzone>
     <div class="text-muted small textExt">
         Ekstensi file yang diperbolehkan: <b>.JPG .JPEG .PNG</b>
     </div>
    </div>
    </div>

</template>
<script>
import vue2Dropzone from 'vue2-dropzone'
import 'vue2-dropzone/dist/vue2Dropzone.min.css'
export default {
  name: 'app',
  components: {
    vueDropzone: vue2Dropzone
  },
  data: function () {
    return {
      dropzoneOptions: {
          url: 'https://httpbin.org/post',
          thumbnailWidth: 150,
          thumbnailHeight: 165,
          maxFilesize: 3,
          maxFiles:1,
            acceptedFiles: '.jpg, .png, .jpeg',
            addRemoveLinks: true
      },
      methods: {
  }
    }
  }
}
</script>
<style>
      @import url("https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css");

    .dropzone .dz-message {
        margin-top: 0;
        margin-bottom: 0
    }
    .dropzone-custom-content {
        margin-top: 0;
    }
    .heightContent {
        height: 150px;
    }
    .position {
        vertical-align: -webkit-baseline-middle;
        margin-top: 20px;
    }
    .dropzoneBorder {
        box-shadow: 1px 8px 20px #c2c1c181;
        border: none
    }
    .textExt {
        font-size: 11px;
        text-align: center;
        margin-top: 15px;
    }
    .vue-dropzone:hover {
        background-color: transparent;
    }
</style>