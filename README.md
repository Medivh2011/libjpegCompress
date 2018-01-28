# libjpegCompress
Android libjpegCompress supported arm64,x86,x84_64
1.在项目build.gradle添加
allprojects {
		repositories {
			maven { url 'https://jitpack.io' }
		}
	}
  2.在App module添加
  dependencies {
	        compile 'com.github.Medivh2011:libjpegCompress:1.1'
	}
  3.Use
  ImageCompress.with(getApplicationContext()).load(imagePath).ignoreBy(100).setTargetDir(savedir).setOnCompressListener(new ImageCompress.OnCompressListener() {
      @Override
      public void onStart() {
        //todo doStart
      }

      @Override
      public void onSuccess(String filePath) {
        //todo douccess
      }

      @Override
      public void onError(Throwable e) {
        //todo doError
      }
    }).launch();
    
  
