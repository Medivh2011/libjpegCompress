# libjpegCompress
Android libjpegCompress supported armeabi armeabi-v7a arm64-v8a,x86,x84_64</br>

### 1.在项目build.gradle添加
   <pre> <code>
allprojects {
	repositories {
		maven { url 'https://jitpack.io' }
		    }
	    }
	</code></pre>
	
### 2.在App module build.gradle添加
  
  <pre><code>
  dependencies {
	        compile 'com.github.Medivh2011:libjpegCompress:0.5.3'
	         compile 'com.android.support:support-v4:buildVersion'
	}
	</code></pre>
	
### 3.Use
  <pre><code>
  ImageCompress
  .with(getApplicationContext())
  .load(imagePath)//需要压缩图片的路径
  .ignoreBy(100)//压缩100K以上的图片
  .fileName(...)//压缩文件名
  .setTargetDir(savedir)//保存压缩图片的位置
  .setOnCompressListener(new ImageCompress.OnCompressListener() 
  {
      @Override
      public void onStart() {
        //todo doStart
      }

      @Override
      public void onSuccess(String filePath) {
        //todo doSuccess
      }

      @Override
      public void onError(Throwable e) {
        //todo doError
      }
    }).launch();
    </code>
    <pre>
    
  
