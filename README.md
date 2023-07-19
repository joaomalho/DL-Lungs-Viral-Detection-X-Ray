### Lung Virus Detection

📖 Introduction
* Within the scope of Deep Learning, it was proposed a project, where the student's ability to build an Image Classification model following a specific challenge would be tested. It was proposed to create a sequencial model in a greedy iterative manner so that the students would be able to test several parameters and analyze their impact on the models. The project will be divided into 5 notebooks:

Exploration - Data Collection and Analysis
Preprocessing - Data Process for Modelling
Models Without Data Augmentation - Models Construction
Models Without Oversampling - Models Construction
Models With Data Augmentation & Oversampling - Models Construction

🔍 The Problem
* The group came across an interesting thread in Kaggle where the authors published Chest X-rays images so that Deep Learning and AI Enthusiasts can contribute to improving COVID-19 detection using just Chest X-rays, their objective was to "Help the medical and researcher community and encourage them to contribute extensively."

* COVID-19 and Viral Pneumonia have become a major public health concern since the emergence of the COVID-19 pandemic. In this case, the human can't detect visually the patterns that show if a patient is diseased or not In recent years, Deep Learning models have shown promising results in medical image analysis, especially in the field of radiology.

The project aims to tackle this problem by developing a COVID-19 and Viral Pneumonia detector using Deep Learning techniques. Specifically, the use of several convolutional neural networks (CNN) models such as VGG and ResNet, in a greedy optimization way to find the optimal hyperparameters for the model. The model will take Chest X-ray images as input and output a classification indicating whether the patient is infected with COVID-19 or viral pneumonia, or not infected at all.


### Final Model

* Learning rates and Momentums are defined as default

<pre>
Final_Model = base_cnn(act_1='relu',                                        
                        n_filt_1=6,                                         
                        n_filt_2=128,                                       
                        act_2='softmax',                                   
                        kernel_size=(3,3),                                   
                        pool_size=(2,2),                                    
                        batch_norm=0,                                      
                        model_name = 'Final_Model', 
                        optim=Adam(lr=0.001),                              
                        loss_lambda='sparse_categorical_crossentropy',      
                        metric='accuracy',
                        epoch=10,
                        schema=1,       
                        scores=1,       
                        results=1,      
                        data_augmentation=0,                               
                        seed=0)
</pre>

<img src="https://github.com/joaomalho/DL-Lungs-Viral-Detection-X-Ray/blob/main/lungs_score.png?raw=true" width="900"/>
