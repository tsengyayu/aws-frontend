<template>
  <div class="upload-section">
      <img class="robot-img" src="@/components/home/content/assets/robot_icon.png" />
      請匯入論文PDF完整檔案
    <button class="pdf-input" @click="uploadPDF">
      匯入 PDF
    </button>
  </div>
</template>

<script>
export default {
  name: 'UploadPage',
  methods: {
    selectFile() {
      this.$refs.fileInput.click();
    },
    handleFileUpload(event) {
      const file = event.target.files[0];
      if (file) {
        console.log('File selected:', file);
        // 在這裡處理文件上傳邏輯
      }
    },
  },
};
</script>

<style>
.upload-section {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #FFFFFF;
  padding: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  margin-bottom: 20px;
  font-size: 10px;
  /* width: calc(100% - 700px); */
  
}
.robot-img{
  height: 30px;
  padding: 10px 10px 10px 10px;
}
.pdf-input{
  background-color: #4285F4;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  margin-right: 10px;
  margin-left: 500px;
  display: flex;
  align-items: center;
  border-radius: 10;
  font-size: 10px;
}

</style>
