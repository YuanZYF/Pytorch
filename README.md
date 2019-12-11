# FaceNet
* 人脸预测
  * 数据准备：
    * 在pictures文件夹中新建以目标人物名称命名的文件夹并将目标人物的图片放入其中。每个目标人物数量一致。其中pictures名称可以更改。
    ```
    picetures
    │     
    │
    └───person1
    │     img1.jpg
    │     img2.jpg
    │   
    │   
    └───person2
          img1.jpg
          img2.jpg
    ```
    * 将寻找目标人物的视频放入output文件夹。output文件夹名称可以更改。
    ```
     outputs
    │     
    │
    └───test_video.mp4
   
    ```
  * 运行：
  进入test文件夹运行main.py,文件夹以/结尾
  ```
  python main.py --input ../pictures/ --output ../outputs/ --video_path test_video.mp4 --THRED 0.0013
  ```
  * 阈值设定：
	设置原则为：当把目标任务当成others时，增加阈值；相反减小。先确定小数点后3位，微调后4，5位。
	阈值为0.0012-0.0013
