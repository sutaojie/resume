<template>
<div class="pdf-wrap" id="pdfWrap">
 <button v-on:click="getPdf">点击下载PDF</button>
 <div class="pdf-dom" id="pdfDom"></div>
</div>
</template>
<style >

</style>
<script type="text/ecmascript-6">
 import html2Canvas from 'html2canvas'
 import JsPDF from 'jspdf'

 export default {
  methods: {
   getPdf: function () {
    let _this = this
    let pdfDom = document.querySelector('#pdfDom')
    html2Canvas(pdfDom, {
     onrendered: function(canvas) {
      let contentWidth = canvas.width
      let contentHeight = canvas.height
      let pageHeight = contentWidth / 592.28 * 841.89
      let leftHeight = contentHeight
      let position = 0
      let imgWidth = 595.28
      let imgHeight = 592.28 / contentWidth * contentHeight

      let pageData = canvas.toDataURL('image/jpeg', 1.0)

      let PDF = new JsPDF('', 'pt', 'a4')

      if (leftHeight < pageHeight) {
       PDF.addImage(pageData, 'JPEG', 0, 0, imgWidth, imgHeight)
      } else {
       while (leftHeight > 0) {
        PDF.addImage(pageData, 'JPEG', 0, position, imgWidth, imgHeight)
        leftHeight -= pageHeight
        position -= 841.89
        if (leftHeight > 0) {
         PDF.addPage()
        }
       }
      }
      PDF.save(_this.pdfData.title + '.pdf')
     }
    })
    html2Canvas()
   },
  }
 }
</script>