## Training Custom Dataset on Colab for YoloV3
Refer to this Colab File: [LINK](https://colab.research.google.com/drive/1LbKkQf4hbIuiUHunLlvY-cc0d_sNcAgS)

Refer to this GitHub Repo [REPO](https://github.com/theschoolofai/YoloV3)

Collect a dataset of 500 images and annotate them. Please select a class for which you can find a YouTube video as well. Steps are explained in the readme.md file on GitHub.
Once done:

1) Download a very small (~10-30sec) video from youtube which shows your class.

2) Use ffmpeg to extract frames from the video. 

3) Upload on your drive (alternatively you could be doing all of this on your drive to save upload time)

4) Inter on these images using detect.py file. **Modify** detect.py file if your file names do not match the ones mentioned on GitHub. 
`python detect.py --conf-thres 0.3 --output output_folder_name`

5) Use ffmpeg to convert the files in your output folder to video

6) Upload the video to YouTube. 

7) Share the link to your GitHub project with the steps as mentioned above

8) Share the link of your YouTube video


------------------------------------
## V1 - Only 1 class

1) Initially trained the model with just one class. Have taken 350 images from google.

2) Resized all images to be below 1300x800 customizing the given resize code

3) Made changes to the cfg file 

  Search for 'filters=255' (you should get entries entries). Change 255 to 18 = (4+1+1)*3
  
  Search for 'classes=80' and change all three entries to 'classes=1'

  burn_in to 100
  
  max_batches to 5000
  
  steps to 4000,4500
  
4) Uploaded the files and the custom.txt, custom.names and custom.data to colab.

5) Finished training the model after which video part 1 is released. 

[Jerry detector](https://www.youtube.com/watch?v=1j1q8uaPmOk)

-------------------------------------

## V2 Training for 2 classes

1) Same code just updated cfg file to have 2 classes and changed filters to  (4+1+2)*3 = 21

2) Trained the same Yolo model again 

[Tom And Jerry detector](https://www.youtube.com/watch?v=QW6WJoRNK-o)
