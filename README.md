# Object detection with Tensorflow
<p>This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API.

# Steps
<br />
<b>Step 1.</b> Clone this repository: https://github.com/anhduy412/object-detection
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
virtualenv env
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source object-detection/bin/activate # Linux
.\env\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Collect images using the Notebook <b>img-collect.ipynb</b> - ensure you change the kernel to the virtual environment as shown below
<br/>
<br/>
<b>Step 5.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
<pre>\object-detection\data\workspace\images\train<br /></pre>
<pre>\object-detection\data\workspace\images\test</pre>
<b>Step 6.</b> Begin training process by opening <b>training-and-detecting.ipynb</b>, this notebook will walk you through installing data Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 7.</b> During this process the Notebook will install data Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<br> <br>
<b>Step 8.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<img src="https://i.imgur.com/K0wLO57.png"> 
<br />
<b>Step 9.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
