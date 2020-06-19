# Banana-AR
> 这是一个AR的demo/ This is a demo about ar run in web
## 预览/PreView
> 1. 首先，打开你的手机, 确保你使用的浏览器支持WEBGL1.0和WebRTC平台, 安卓已支持谷歌浏览器,QQ和微信的内置浏览器, I0S系统需要版本11以上，使用系统自带扫码打开页面，在Sarari中运行, 需要注意的，IOS微信内置浏览器并不支持webRTC标准/Now, Openinig your phone please, you sholud make sure your Browser can support WEBGL1.0 and webRTC
> 2. 扫码/Useing your phone's camera to scan qrcode 
> 3. ![alt text](https://skadieyes.github.io/Banana-AR/img/qrcode.png "qrCode")
> 4. 确保扫码后打开页面，并允许了相机的授权, 把相机对准下面的Maker（也就是这张图片）/ opening this page and allow camera authorizationinig to camera, using camera to this picture
> 5. ![alt text](https://skadieyes.github.io/Banana-AR/maker/banana.png "bananaMaker")
> 6. 现在你可以看到banana拉～/ now you can see the banana on your screen
> 3. ![alt text](https://skadieyes.github.io/Banana-AR/img/banana.jpeg "bananaOnScreen")
## 实现/How to do it
> 1. 项目主要依赖ar.js和three.js, ar.js基于增强显示的SDK-ARToolkit,是我们实现web-ar的基础，使得我们在浏览器上也可以使用相机跟踪和识别标记卡(maker), 计算摄像机和标记卡之间的位置，让我们能够把虚拟的事物覆盖到真实的标记卡上。three.js在此处的作用主要是识别maker后的显示，跟踪到maker后我们可以精确地将模型渲染到maker上。
> 2. 所以第一步先引入ar.js和three.js/ import ar.js and three.js
> 3. 创建renderer, WebGLRenderer
> 4. 在画布中创建场景scene和相机camera
> 5. 引入ArToolkitSource, ArToolkitContext, 获取相机和使用相机实时跟踪标记卡
> 6. 使用ArMarkerControls引入训练后的标记卡(maker), 使相机跟踪和识别标记卡，并重新计算和更新maker的位置到计算机视图
> 7. 在跟踪maker位置后计算的位置上，我们可以放置我们的Mesh, 或者引入的模型（模型可以贴上好看的材质和纹理～).
> 8. 在requestAnimationFrame中调用onRenderFcts,  onRenderFcts中有我们的renderer, 不停更新的arToolkitContext, smoothedControls（可以获得匹配market之后在计算机视图中的位置信息), mesh的变化（旋转等）。

## 如何训练获得我们的maker
>  https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html  训练工具
>   或者你可以使用ARToolKit的SDK获得maker，详见文档
## 如何获得摄像机校准参数
> 练习用的话直接使用ar.js的demo包中的校准文件即可

## 代码
> :heart:  [一个ar Banana](https://github.com/skadieyes/Banana-AR)

## 最后
> 有不足和错误的地方欢迎指出
