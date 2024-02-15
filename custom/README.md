# Steps for generating training data

1. Run `main_app_single_file.py` to generate track data. Note: If you don't want 400x400 images, will have to updated code in `tracker.py`
2. Run `track_gif.py` to generate gifs of track images
3. Run `gen_csv.ipynb` to generate unlabeled csv file that you will use to label the tracks. The gifs generated earlier can be used to assist
4. After track labeling is complete, run `gen_labels.ipynb` to generate the YOLOv8 format labels
5. Run `train_val_split` to split your dataset into train and validation sets. Recommendation for test set is to use roboflow to label full res images in COCO format. 

Improvements to the cleanliness of the code can definitely be made, feel free to touchup as needed. 
-Aaron