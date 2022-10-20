# yolov5-feat

## This is a clothing retrieval project. based on large-scale clothing mixture dataset, based on the feature map of the backbone of yolov5 for similarity retrieval of clothing patterns. <br>
<br>Project Phase:<br>
<br>1. Train yolov5 and extract feature codes<br>
<br>Second, server-side flask deployment<br>

<br>Phase 1:<br>
1. Download the marked clothing dataset deepfashion2, and use deepfashion2coco.py to convert a certain number of datasets into coco format, modify the parameters to run twice to generate training.json and val.json respectively, and then run extrect_some_example.py to extract the image to the specified folder, the number of pictures is the same as in the deepfashion2coco.py file. <br>
<br>2. Modify the path information in example.py and run it, convert the json file of coco to the txt format required by yolov5. <br>
<br>3. Modify the path information and parameter settings in train.py to train. The trained model is saved under runs/train/weights. <br>
<br>4. Run detect.py to complete inference and modify corresponding parameters. <br>
<br>5. Run search_demo.py to retrieve images, put an image to be retrieved into the newly created demo folder, and then modify some parameters in search_demo.py to retrieve images based on similarity.
The feature vector of yolov5 itself is used, and no new network is introduced. The output results will be saved under runs/detect/exp..., the query accuracy rate is 90%+<br>

<br>Phase II:<br>
<br>A Flask server side, the deployed code is in the model_sever folder. <br>
<br>Modify the parameters of search_rank_5.py, and then run python, I believe you can understand. <br>
<br>Return to the 5 pictures in the gallery folder that are most similar to the query picture. If you don't understand, ask, welcome to star and leave a message. <br>


