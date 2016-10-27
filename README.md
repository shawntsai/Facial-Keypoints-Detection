
Code to setup AWS GPU instance to run Daniel Nouri's Facial Keypoints competition convoluted neural network code

To use this script, first run this to fit your first model:
    python kfkd.py fit
Then train a bunch of specialists that intiliaze their weights from
your first model:
    python kfkd.py fit_specialists net.pickle
Plot their error curves:
    python kfkd.py plot_learning_curves net-specialists.pickle
And finally make predictions to submit to Kaggle:
    python kfkd.py predict net-specialists.pickle


1. start a AWS GPU instance
 - I used Ubuntu Server 14.04 LTS (HVM), SSD Volume Type
 - Search "community AMI's" for AMI ID ``` theano-tensorflow-cuda7.0-cudnn4 (ami-2f8c7b42)```
 - And for GPU instance I used GPU instances g2.2xlarge
2. ssh into the server
3. ```git clone https://github.com/wendykan/AWSGPU_DeepLearning.git```
4. ```chmod 777 -R AWSGPU_DeepLearning/```
5. ```vi cookies.txt```
  - Then copy-paste kaggle cookie into this file
6. ```./setup.sh ```
