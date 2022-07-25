# yolov7-opencv-dnn-cpp
使用opencv模块部署yolov7-0.1版本和yolov5-6.0以上版本<br>

基于yolov5-6.0版本的yolov5:https://github.com/ultralytics/yolov5 <br>
基于yolov7-0.1的版本https://github.com/WongKinYiu/yolov7 <br>

OpenCV>=4.5.0 <br>

> python path/to/export.py --weights yolov5s.pt --img [640,640] --opset 12 --include onnx
> python path/to/export.py --weights yolov7.pt --img [640,640]

可以通过yolo.h中定义的YOLOV5宏定义来切换yolov5和yolov7两个版本，(其实两个版本onnx后处理方式差不多的说<br>
>通过yolo.h中定义的YOLO_P6来切换是否使用两者的P6模型。<br>
> YOLOV5:true -->yolov5.onnx<br>
> YOLOV5:false-->yolov7.onnx


另外关于换行符，windows下面需要设置为CRLF，上传到github会自动切换成LF，windows下面切换一下即可。<br>
贴个yolov7.onnx和yolov5s.onnx的对比<br>
![yolo](https://user-images.githubusercontent.com/52729998/180824922-0c7dc3f9-fbda-497b-9ae3-3f299b8c0452.png)