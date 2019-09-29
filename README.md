**Referenced REPO** :  https://github.com/AlexeyAB/darknet

I cannot load up my trained weights file which is more than 25 MB.  But you can run the training on your own.
The data files is uploaded with labels.

Do a build to get the executable darknet file 1st by **make clean** followed by **make**

Train for yolov3 TINY and get the weights file

```
./darknet detector train cfg/pmd/pmd-yolov3-tiny_obj.data cfg/pmd/pmd-yolov3-tiny_obj.cfg yolov3-tiny.conv.15 -dont_show -map
```
Then test the detection

Detecting single image by
```
./darknet detect cfg/pmd/pmd-yolov3-tiny_obj.data ./data/pmd/weights-tiny/pmd-yolov3-tiny_obj_last.weights ./data/pmd/JPEGImages/s1.jpg
```
Detect a VIDEO by
```
./darknet detector demo cfg/pmd/pmd-yolov3-tiny_obj.data data/pmd/weights-tiny/pmd-yolov3-tiny_obj_final.weights data/pmd/pmd.mp4
```
