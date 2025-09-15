# Digital Pathology Classification

This work was done for a Kaggle competition. The data contained a set of pathology images labelled into integer categories ranging 0-19, each representing a different tissue type (the specific tissue type that each numeric label correponds to were not provided).

I used ```fastai``` to finetune various pretrained computer vision models to this dataset and classified images. I achieved a final accuracy of 0.96. 

I also deployed the final model as an [app](https://huggingface.co/spaces/layaasiv/digital-pathology) on HuggingFace Spaces.
