# Flask Image Classification

This repo comprises of training ResNeXt from scratch on cifar10 and then using Flask for Model serving.




## Setting up the Environment

To setup the environment 
```bash
python3 -m pip install -U virtualenv # install the virtualenv
virtualenv -p python3 dev_env # creating an environment
source dev_env/bin/activate # activate environment
git clone https://github.com/abhiroop10/Image-Classification-and-Deployment-ResNeXt #clone the repo
cd Image-Classification-and-Deployment
pip install -r requirements.txt # install the requirements
```



## For Training

[Run Training Notebook file](TrainingNotebook.ipynb)



## For Inference

 we need Cifar-10 data for inference. Execute the below to generate 10 random images from cifar-10 test data.

```bash
cd data
python generate_valid_data.py
```

Run [Inference Notebook file](InferenceNotebook.ipynb)




## Model Serving on Flask.

For Serving this model as a website. First generate  test images by executing above commands and then.


```bash
python flask_api/app.py
```


## Further improvements on the model:

1. Added normalization.
2. Tried with dropout, no major change
3. Changed our model from ResNeXt29 2x64d to ResNeXt29 32x4d(with the addition of the above features)
4. Also added Vertical flip data augmentation. 
5.Trained the model for 100 epochs
6. Resulted in a better model with no overfitting.


Group Members:
1. Abhiroop Choudhury   E20002
2. Satish Kumar         E20029
3. Anindita Das         E20006
4. Arshan
5. Anuj

 