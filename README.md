ImageCompression
================

这是一个基于canvas，应用在移动端的前端图片压缩的JS，其修正了移动端即时拍照上传时图片倒转等问题。

使用方法:

步骤一：
      链接exif.js和processImg.js，如下:

        <script src="js/exif.min.js"></script>
        <script src="js/processImg.min.js"></script>

步骤二：
      写入HTML，其必备要素是一个input file图片上传按钮和一个图片预览也是压缩后图片base64数据存储的img标签。
      例:

      <div class="imageFrame">
          <input name="upimage" id="upimage" type="file">
          <input type="button" id="upimageButton" onclick="upimage.click()">
          <img id="showimage" src="images/dengni37.jpg" alt="">
      </div>

步骤三：
      调用compressImg方法，如下：
      
      compressImg('upimage','showimage',480,function(src){
            //此处为回调函数，当图片压缩完成并成功显示后执行
            //可得到图片数据值src
            console.log(src);
      });
      'upimage'为图片上传按钮ID，
      'showimage'为图片预览按钮ID，
      最后一个参数为被压缩后图片的宽度。
