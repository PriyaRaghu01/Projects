                                                                           
Under the Guidance of 
Prof.T.Suguna M.Tech 
DEPARTMENT OF COMPUTER SCIENCE AND 
ENGINEERING 
GOVERNMENT COLLEGE OF TECHNOLOGY 
(An Autonomous Institution affiliated to Anna University 
Coimbatore) 
COIMBATORE - 641 013 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
MINI 
PROJECT
 WORK 
 
 
 
 
 
 
 
     2022 
 
BREAST CANCER CLASSIFICATION 
FROM HISTOPATHOLOGICAL IMAGES 
USING CONVOLUTIONAL NEURAL 
NETWORK IN DEEP LEARNING 
 
PROJECT SUBMITTED IN PARTIAL 
FULFILLMENT OF THE 
REQUIREMENTS FOR THE AWARD OF 
THE DEGREE OF BACHELOR OF 
TECHNOLOGY IN INFORMATION 
TECHNOLOGY 
OF THE ANNA UNIVERSITY 
 
Submitted by 
 
                                                             BARANITHARASI M (1818106) 
                                                         MATHUMITHA S (1818137) 
                                                            PRIYADHARASINI R (1818144) 
                                                           
Under the Guidance of  
Prof. T. SUGUNA, M.TECH., 
AP/IT 
 
DEPARTMENT OF INFORMATION TECHNOLOGY 
GOVERNMENT COLLEGE OF TECHNOLOGY 
 (An Autonomous Institution Affiliated to Anna University)  
COIMBATORE - 641 013 
                                                                       i  
DEPARTMENT OF INFORMATION TECHNOLOGY 
GOVERNMENT COLLEGE OF TECHNOLOGY 
(An Autonomous Institution affiliated to Anna University) 
COIMBATORE - 641 013 
 
MINI PROJECT WORK 
 
JANUARY 202 
 
This is to certify that this project work entitled 
 
 BREAST CANCER CLASSIFICATION FROM 
HISTOPATHOLOGICAL IMAGES USING 
CONVOLUTIONAL NEURAL NETWORK IN DEEP 
LEARNING 
is the bonafide record of project work done by 
 
BARANITHARASI M                        1818106 
                                MATHUMITHA S  1818137 
  PRIYADHARASINI R     1818144 
 
 
of B.TECH. (Information Technology) during the year 2021 - 2022 
 
 
 
Project Guide Head of the Department 
Prof. T. Suguna, M.TECH., AP/IT                            Dr. S. Rathi, M.E, Ph.D., 
 
 
Submitted for the Project Viva-Voce examination held on    
 
 
 
  
 
Internal Examiner External Examiner 
ACKNOWLEDGEMENT 
Great achievements are not possible without standing on the shoulders of giants. 
Without the active involvement of the following experts this project would not have been 
a reality. 
We express our sincere gratitude to Dr.P.Thamarai M.E, Ph.D., Principal, 
Government College of Technology, Coimbatore for providing us all facilities that we 
needed for the completion of this project. 
We whole-heartedly express our thankfulness and gratitude to Dr.S.Rathi M.E., 
Ph.D., Professor and Head of the Department of Information Technology, Government 
College of Technology, for helping us to successfully carry out this project. 
Our thankfulness and gratitude to our respectable project guide Prof.T.Suguna 
M.Tech., Assistant Professor, who has been immense help through the various phases 
of the project. With her potent ideas and excellent guidance, we were able to comprehend 
the essential aspects involved. 
We would like to thank our faculty advisor Dr.M.Blessy Queen Mary M.E.,Ph.D., 
Assistant Professor for her continuous support and encouragement throughout this 
project. 
We extend our sincere thanks to the faculty members of Information Technology 
department, Prof.R.Devi, M.Tech., Assistant Professor, Prof.C.Aswini, M.Tech., 
Assistant 
Professor, 
Prof.S.GladsonOliver, 
M.Tech., 
Assistant 
Professor, 
Prof.M.Jeyanthi, M.Tech., Assistant Professor, Prof.R.Malavika, M.Tech., Assistant 
Professor, Prof.M.Gowri Shankar, M.E, Assistant Professor, for rendering their help for 
the completion of this project. We also thank Non-Teaching Staffs and all our friends for 
their cooperation and suggestions towards the successful completion of this project. 
ii 
SYNOPSIS 
Deep learning (known as Convolutional neural networks) is an artificial intelligence (AI) function 
that imitates the workings of the human brain in processing data and creating patterns for use 
in decision making. Several deep learning algorithms have been recently introduced to 
scientific communities and are applied in various application domains. In this project, 
Convolutional Neural Network [CNN] is used for image classification. There are mainly three 
things in CNN: i) local receptive field, ii) shared weight and biases, iii) activation and pooling. 
In CNN, first the neural networks are trained using a heavy set of data so that the CNN can 
extract the feature of given input. When the input is given, first image preprocessing is done 
then the feature extraction occurs on the basis of set of data stored and then the classification 
of data is done and output is shown as the result. 
The main aim of our project is to detect and classify the histopathological images as cancerous 
or non-cancerous using convolutional neural networks.  
iii 
iv  
CONTENTS 
 
 
CHAPTER NO                            TITLE PAGE NO 
   
 BONAFIDE CERTIFICATE i 
 ACKNOWLEDGEMENT                      ii 
 SYNOPSIS                      iii 
 TABLE OF CONTENTS iv 
 LIST OF FIGURES                      ix 
 LIST OF ABBREVATIONS                    x 
 
       1 
 
INTRODUCTION 
 
1-3 
 
 1.1 DESCRIPTION                        1               
 1.2 EXISTING SYSTEM                        1 
 1.3 PROBLEM DEFINITION                        2              
 1.4 PROPOSED SYSTEM                        2 
 1.5 ORGANIZATION OF PROJECT                       3                                
 
          2 
 
LITERATURE SURVEY 
 
                    4-10 
 
2.1  A SUPPORT VECTOR MACHINE BASED                    4 
ENSEMBLE ALGORITHM FOR BREAST  
CANCER DIAGONSIS 
2.1.1 DESCRIPTION                                                   
2.1.2 MERIT                                                                
2.1.3 DEMERIT                                                           
2.2 
2.3 
2.4 
2.5   
IMPROVED MAMMOGRAPHIC CAD                            
PERFORMANCE USING MULTI-VIEW  
INFORMATION: A BAYESIAN NETWORK  
FRAMEWORK  
2.2.1 DESCRIPTION                                                   
2.2.2 MERIT                                                                
2.2.3 DEMERIT                                                       
X-RAY SCATTERING IMAGE CLASSIFICATION         
USING DEEP LEARNING 
2.3.1 DESCRIPTION                                                   
2.3.2 MERIT 
2.3.3 DEMERIT 
BREAST CANCER DIAGNOSIS BASED ON  
ENHANCED PARETO OPTIMAL AND MULTI-              
LAYER PERCEPTRON NEURAL NETWORK                           
2.4.1 DESCRIPTION 
2.4.2 MERIT 
2.4.3 DEMERIT 
MULTI-VIEW DEEP LEARNING  
ARCHITECTURE FOR CLASSIFICATION OF               
BREAST MICROCALCIFICATIONS  
2.5.1 DESCRIPTION 
2.5.2 MERIT 
5 
6 
7 
8  
v 
2.5.3 DEMERIT 
2.6   
BATIK CLASSIFICATION USING DEEP  
CONVOLUTIONAL NETWORK TRANSFER                  
LEARNING  
2.6.1 DESCRIPTION 
2.6.2 MERIT 
2.6.3 DEMERIT 
2.7 A KNOWLEDGE BASED SYSTEM FOR BREAST           
CANCER CLASSIFICATION FUZZY LOGIC  
METHOD  
2.7.1 DESCRIPTION 
2.7.2 MERIT 
2.7.3 DEMERIT 
3                      
SYSTEM SPECIFICATION 
3.1      
3.2      
SYSTEM REQUIREMENTS 
3.1.1  SOFTWARE REQUIREMENT 
3.1.2  COLAB SPECIFICATION     
SOFTWARE DESCRIPTION 
3.2.1 ABOUT GOOGLE COLAB 
3.2.2 ABOUT PYTHON 
3.2.3 CHARACTERISTICS OF PYTHON   
9       
10 
11-12 
11 
11 
11 
12 
12 
12 
12 
vi 
vii  
 
                4                      PROJECT DESIGN     13-20 
 
 4.1       OBJECTIVE                                                                      13 
 4.2       FLOW CHART                                                                  13 
                                       4.3        MODULE DESCRIPTION OF THE MODEL                    14 
                                                     4.3.1  PRE-PROCESSING                                              14 
                                                     4.3.2  TRAINING THE MODEL                                       15 
                                                     4.3.3  TESTING THE MODEL                                          19 
                                       4.4        DATA AUGMENTATION TECHNIQUE                            20 
   
         5 IMPLEMENTATION AND RESULT 21-30 
   
 5.1 IMPLEMENTATION                     21 
 5.1.1 IMPORT LIBRARIES                                          21 
 5.1.2 DATA PROCESSING 23 
 5.1.3 TRAINING AND EVALUATION 
SPLIT                                                                            
                    23 
 5.1.4 DATA GENERATOR 24 
 5.1.5 MODEL DEFINITION 25 
 5.1.6 TRAINING DATASET  26 
 5.1.7 PLOTTING THE GRAPH    27 
5.1.8  IMAGE PREDICTION    27 
5.2 SAMPLE OUTPUT                                                            28 
5.2.1 ACCURACY AND LOSS GRAPH 28 
5.2.2 PREDICTION 
29 
5.2.2.1 CANCEROUS PATCH                               
5.2.2.2 NON-CANCEROUS PATCH                      
6                       
7                       
CONCLUSION 
REFERENCES                                                                            
29 
30 
31 
32
 viii 
ix  
LIST OF FIGURES 
 
 
 
 
 
FIGURE NO. 
 
 
    4.1 
                                            TITLE 
 
 
    WORKFLOW OF THE PROCESS 
PAGE NO 
 
 
                      13 
    4.2 
    4.3 
    4.4 
    CNN ARCHITECTURE 
    WORKING EXAMPLE OF CNN ARCHITECTURE 
    REPRESENTATION OF TRAINING AND  
    TESTING THE MODEL                                                                
                            14 
                            17 
                             
                            19                                          
    5.1     EXISTING SYSTEM – ACCURACY GRAPH                             28 
    5.2     EXISTING SYSTEM – LOSS GRAPH                      28 
    5.3     INPUT IMAGE FOR CANCEROUS                      29 
    5.4     OUTPUT PREDICTION FOR CANCEROUS                       29 
    5.5     INPUT IMAGE FOR NON-CANCEROUS                                                                   30 
    5.6     OUTPUT PREDICTION FOR NON-CANCEROUS                      30 
LIST OF ABBREVATIONS 
ANN 
CAD 
CC 
CNN 
EX-DBC 
GMMs 
GPU 
KNN 
MLO 
MLP 
OPEN CV 
PCA 
RAM 
RF 
SVM 
WAUCE 
ARTIFICIAL NEURAL NETWORK 
COMPUTER AIDED DESIGN 
CRANI CAUDAL VIEW 
CONVOLUTIONAL NEURAL NETWORK 
EXPERT SYSTEM DUCTAL BREAST CANCER 
GAUSSIAN MIXTURE MODELS 
GRAPHICS PROCESSING UNIT 
K NEAREST NEIGHBOUR 
MEDIO LATERAL OBLIQUE VIEW 
MULTI LAYER PERCEPTRON 
OPEN SOURCE COMPUTER VISION 
PRINCIPLE COMPONENT ANALYSIS 
RANDOM ACCESS MEMORY 
RANDOM FOREST 
SUPPORT VECTOR MACHINE 
WEIGHTED AREA UNDER THE RECEIVER OPERATING 
CHARACTERISTICS CURVE ENSEMBLE 
x 
CHAPTER 1  
INTRODUCTION 
1.1 DESCRIPTION 
Breast cancer can originate from any cell, tissue, or gland of the breast. 
Sometimes it starts from the ducts that produce milk and sometimes it originates 
from the lobules which are glandular tissues. If not diagnosed at an early stage 
there is a possibility of spreading the cancer cells toward different parts of the body 
and cause damage there too. Breast tumor has two most common types: benign 
and malignant where the benign lesion is not cancerous, it is some kind of 
abnormalities in the cell and they are unable to become a cause of breast cancer 
and malignant is cancerous lesions. Malignant cells spread at a very fast rate by 
start divisions swiftly because both cells (benign and malignant) have irregular 
appearance and structure, it is a very difficult task to manually analyze the 
microscopic image. To overcome this issue and making this process completely 
automatic deep learning has been introduced. CNN has been used in many types 
of researches in medical image processing but used very rarely in breast cancer 
classification. In this study, application of deep learning has been exploit using the 
CNN model for the classification of breast cancer using histopathology images.  
1.2 EXISTING SYSTEM 
Several methods can be used to diagnose Breast Cancer, including breast biopsy, 
ultrasound, mammography, thermography, and fine needle aspiration cytology 
which requires the availability of pathologist for diagnosis which might reduce the 
accuracy rate. In order to improve breast cancer outcomes and survival, early 
detection is critical. Since detection of cancer is key to effective treatment of breast 
cancer we use various machine learning algorithms to predict if a tumor is benign 
1 
or malignant, based on the features provided by the data.The limitation of most of 
the machine learning study is the lack of experimental data because of which the 
cost of the experiment increases. More accuracy could be achieved by the better 
labeling of the input images and by using high-quality data. 
1.3 PROBLEM DEFINITION 
According to the world health organization (WHO) Breast cancer is the most 
frequent cancer among women, impacting 2.1 million women each year, and also 
causes the greatest number of cancer-related deaths among women. In 2018, it is 
estimated that 627,000 women died from breast cancer-that is approximately 15% 
of all cancer deaths among women. While breast cancer rates are higher among 
women in more developed regions, rates are increasing in nearly every region 
globally. Accurate detection and classification of breast cancer is a critical task in 
medical imaging due to the complexity of breast tissues. Due to automatic feature 
extraction ability, deep learning methods have been successfully applied in 
different areas, especially in the field of medical imaging. In this study, a novel deep 
learning using Convolutional Neural Network model for the Breast Cancer 
Classification with histopathological images is proposed. Features are extracted 
through an unsupervised pre-training and supervised fine-tuning phase. The 
network automatically extracts features from image patches. Logistic regression is 
used to classify the patches from histopathology images. 
1.4 PROPOSED SYSTEM 
The proposed model is working in an unsupervised fashion for the extraction of 
features from the input histopathology image patches in the form of feature vectors. 
The extracted features matrix is then transferred to the backpropagation neural 
network which is a supervised learning phase and it comprises of the conjugate 
gradient. A model is formed by the feature matrix of images in the training phase 
and the final stage is the classification stage which discriminate between cancerous 
and non-cancerous regions.  
2 
1.5 ORGANIZATION OF THE PROJECT 
➢ Literature reviews of already existing proposals are discussed in chapter2. 
➢ Chapter 3 has system specification which tells about the software requirements. 
➢ Chapter 4 discusses the overall project and design which tells the brief 
description of each of the modules in this project. 
➢ Chapter5 has the implementation and experimental result of the project. 
➢ Chapter 6 deals with the conclusion and future work. 
➢ Finally chapter 7 deals with the references. 
3 
CHAPTER 2 
LITERATURE REVIEW 
2.1 
A SUPPORT VECTOR MACHINE BASED ENSEMBLE ALGORITHM 
FOR BREAST CANCER DIAGNOSIS 
2.1.1   DESCRIPTION 
This research studies a support vector machine (SVM)-based ensemble learning 
algorithm for breast cancer diagnosis. Illness diagnosis plays a critical role in 
designating treatment strategies, which are highly related to patient safety. 
Nowadays, numerous classification models in data mining domains are adapted to 
breast cancer diagnosis based on patients’ historical medical records. However, 
the performance of each algorithm depends on various model configurations, such 
as input feature types and model parameters. To tackle the limitation of individual 
model performance, this research focused on breast cancer diagnosis that uses 
an SVM-based ensemble learning algorithm to reduce the diagnosis variance and 
increase diagnosis accuracy. Twelve different SVMs, based on the proposed 
Weighted Area Under the Receiver Operating Characteristic Curve Ensemble 
(WAUCE) approach, are hybridized. To evaluate the performance of the proposed 
model, Wisconsin Breast Cancer, Wisconsin Diagnostic Breast Cancer, and the 
U.S. National Cancer Institute’s Surveillance, Epidemiology, and End Results 
(SEER) program breast cancer datasets have been studied. The proposed 
WAUCE model reduces the variance by 97.89% and increases accuracy by 
33.34%, compared to the best single SVM model on the SEER dataset. 
2.1.2   MERIT 
The experimental results show that the WAUCE model achieves a higher accuracy 
with a significantly lower variance for breast cancer diagnosis compared to five 
other ensemble mechanisms and two common ensemble models, i.e., adaptive 
boosting and bagging classification tree. 
4 
2.1.3  DEMERIT 
One limitation of this study is that it requires a large amount of time and cost. This 
method is quite expensive.  
2.2    IMPROVED MAMMOGRAPHIC CAD PERFORMANCE USING MULTI
VIEW INFORMATION: A BAYESIAN NETWORK FRAMEWORK 
2.2.1   DESCRIPTION 
Mammographic reading by radiologists requires the comparison of at least two 
breast projections (views) for the detection and the diagnosis of breast 
abnormalities. Despite their reported potential to support radiologists, most 
mammographic computer-aided detection (CAD) systems have a major limitation, 
as opposed to the radiologist’s practice. To tackle this problem, a Bayesian network 
framework for multi-view mammographic analysis, with main focus on breast 
cancer detection at a patient level. The causal-independence models and context 
modeling over the whole breast represented as links between the regions detected 
by a single-view CAD system in the two breast projections. The proposed approach 
is implemented and tested with screening mammograms for 1063 cases of whom 
385 had breast cancer. The single-view CAD system is used as a benchmark 
method for comparison. The results show that our multi-view modeling leads to 
significantly better performance in discriminating between normal and cancerous 
patients. It also demonstrate the potential of our multi-view system for selecting the 
most suspicious cases.  
2.2.2  MERIT 
A rule-based system is very beneficial because it contains specific and 
unambiguous information. The rules can be altered and updated easily whenever 
the need arises. 
5 
2.2.3  DEMERIT 
On statistical properties, the use of rules-based has the strain and adversity that 
there is a possibility of deriving the similar statistical properties for some patterns 
of different classes, due to which there may occur a problem of incorrect 
recognition. 
2.3   X-RAY SCATTERING IMAGE CLASSIFICATION USING DEEP 
LEARNING 
2.3.1  DESCRIPTION 
A model is proposed for feature extraction and classification of breast cancer 
using deep-learning and machine-learning models. Inception-v3 and Xception 
were used for feature extraction because of their benefits. Classification was 
performed using softmax, SVM, RF, KNN and ensemble. The Inception-v3 model 
with softmax was combined with other models such as Inception-v3-SVM, 
Inception-v3-RF, Inception-v3- KNN, and ensemble for the purpose of using 
machine learning for clinical applications related to breast cancer. Similarly, the 
Xception model and its combination with other models such as Xception-SVM, 
Xception-RF, Xception-KNN, and the Ensemble method were explored. The 
performance of the proposed models was addressed and compared with the 
existing models in breast cancer classification. The models based on the ensemble 
method produce highest testing accuracy and outperformed the existing models. 
This work could be important for the clinical applications of breast cancer analysis.. 
2.3.2  MERIT 
The proposed system delivered 90.67% accuracy with augmented data and 87.38% 
without augmented data which is high compared to the previous methods which existed 
at that time. 
6 
2.3.3  DEMERIT 
Though the sample provided atmost accuracy, it tend to fail in certain cases as 
Ensemble cannot help unknown differences between sample and population. 
2.4 BREAST CANCER DIAGNOSIS BASED ON ENHANCED PARETO 
OPTIMAL AND MULTILAYER PERCEPTRON NEURAL NETWORK 
[2018] 
2.4.1  DESCRIPTION 
This proposed technique is used for breast cancer in which the classification is 
done using a Multilayer perceptron neural network. A non-dominated sorting 
genetic algorithm is used for the network assembly but local minimum is a problem 
of MLP. This model extract the features from the mammographic images with two 
views MLO and CC, ANNs are used and then focused the features of resultant 
mammographic images from ANNs for classification of two types of cells that are 
benign and malignant. 
2.4.2  MERIT 
This proposed model work can work for different views just as in multi view 
technology and as it is multi layered perceptron the accuracy is high as each layer 
is identified and is noted upon. 
2.4.3  DEMERIT 
This model cannot extract features with a well-built particular performance.  
7 
2.5 A MULTI-VIEW DEEP LEARNING ARCHITECTURE FOR CLASSIFICATION 
OF BREAST MICROCALCIFICATIONS [2016] 
2.5.1  DESCRIPTION 
The problem of differentiating between malignant and benign tumors based on 
their appearance in the CC and MLO mammography views are given. 
Classification of clustered breast microcalcifications into benign and malignant 
categories is an extremely challenging task for computerized algorithms and expert 
radiologists. We describe a deep-learning classification method that is based on 
two view-level decisions, implemented by two neural networks, followed by a 
single-neuron layer that combines the view level decisions into a global decision 
that mimics the biopsy results. Our method is evaluated on a large multi-view 
dataset extracted from the standardized digital database for screening 
mammography (DDSM). Experimental results show that our network structure 
significantly improves on previously suggested methods. 
2.5.2 MERIT 
This model uses a small amount of data and achieves better accuracy. The 
accuracy become better by using a large amount of data. 
2.5.3  DEMERIT 
This model requires a high cost of implementation and as the model uses small 
amount of data when large data is used accuracy rate is reduced. 
2.6 BATIK CLASSIFICATION USING DEEP CONVOLUTIONAL NETWORK 
TRANSFER LEARNING 
2.6.1 DESCRIPTION  
Batik fabric is one of the most profound cultural heritage in Indonesia. Hence, 
8 
continuous research on understanding it is necessary to preserve it. Despite of being 
one of the most common research task, Batik’s pattern automatic classification still 
requires some improvement especially in regards to invariance dilemma. 
Convolutional neural network (ConvNet) is one of deep learning architecture which 
is able to learn data representation by combining local receptive inputs, weight 
sharing and convolutions in order to solve invariance dilemma in image classification. 
Using dataset of 2,092 Batik patches (5 classes), the experiments show that the 
proposed model, which used deep ConvNet VGG16 as feature extractor (transfer 
learning), achieves slightly better average of 89 ± 7% accuracy than SIFT and SURF
based that achieve 88 ± 10% and 88 ± 8% respectively. Despite of that, SIFT reaches 
around 5% better accuracy in rotated and scaled dataset. 
2.6.2 MERIT 
Since VGG16 extractor does not require training, it is more efficient than SIFT/SURF 
BoW extractor. On top of that, neural network models such as VGG16 are known to 
run parallelly in GPU [16] to make it even more efficient. 
2.6.3 DEMERIT 
Certain images in dataset often overlap each other. This condition often confuses 
classifier during training and causes less accurate generalization. Due to the various 
sources of data, the quality (resolution, noise, watermarks etc) of the data are also 
various. Removing low quality data and preprocessing high quality ones may 
produce homogeneous data and improve classifier accuracy. 
9 
2.7 A KNOWLEDGE BASED SYSTEM FOR BREAST CANCER 
CLASSIFICATION FUZZY LOGIC METHOD [2017] 
2.7.1  DESCRIPTION 
A knowledge-based system is proposed for breast cancer disease 
classification. The knowledge-based system uses EM, PCA, CART and fuzzy rule
based methods. WDBC and Mammographic mass datasets are used for the 
method evaluation. The accuracies obtained by the method are respectively 0.932 
and 0.941 for WDBC and Mammographic mass datasets. Breast cancer has 
become a common disease around the world. Expert systems are valuable tools 
that have been successful for the disease diagnosis. The development of a new 
knowledge-based system for classification of breast cancer disease using 
clustering, noise removal, and classification techniques is produced. Expectation 
Maximization (EM) is used as a clustering method to cluster the data in similar 
groups. Classification and Regression Trees (CART)  is used to generate the fuzzy 
rules to be used for the classification of breast cancer disease in the knowledge
based system of fuzzy rule-based reasoning method. To overcome the multi
collinearity issue, Principal Component Analysis (PCA) is incorporated in the 
proposed knowledge-based system. Experimental results on Wisconsin Diagnostic 
Breast Cancer and Mammographic mass datasets show that proposed methods 
remarkably improves the prediction accuracy of breast cancer. The knowledge
based system can be used as a clinical decision support system to assist medical 
practitioners in the healthcare practice. 
2.7.2  MERIT  
This model provides a promising accuracy in the classification task. 
2.7.3  DEMERIT 
This model is a hybrid intelligent system and a non-incremental which is quite 
expensive for implementation. 
10 
CHAPTER 3 
SYSTEM SPECIFICATION 
3.1 SYSTEM REQUIREMENTS 
3.1.1   SOFTWARE REQUIREMENTS 
Operating system : 
Coding Language : 
Tool 
: 
Windows 7 
PYTHON 
Google Colab / MATLAB 
3.1.2  COLAB’S SPECIFICATION 
System 
Hard Disk 
RAM 
: 
: 
: 
Google Colab 
128 GB 
4 GB 
3.2 SOFTWARE DESCRIPTION 
3.2.1  ABOUT GOOGLE COLAB  
Colab is a free Jupyter notebook environment that runs entirely in the cloud. 
Most importantly, it does not require a setup and the notebooks that you create can 
be simultaneously edited by your team members - just the way you edit documents 
in Google Docs. Colab supports many popular machine learning libraries which 
can be easily loaded in your notebook. Typical uses include: 
➢ Write and execute code in Python 
➢ Import/Save notebooks from/to Google Drive 
11 
➢ Import/Publish notebooks from GitHub 
➢ Import external datasets from Kaggle 
➢ Integrate PyTorch, TensorFlow, Keras,OpenCV 
➢ Free Cloud service with free GPU 
3.2.2  ABOUT PYTHON 
Python is an interpreted, high-level and general-purpose programming language. 
Python's design philosophy emphasizes code readability with its notable use of 
significant indentation. Its language constructs and object-oriented approach aim 
to help programmers write clear, logical code for small and large-scale projects 
python is dynamically-typed and garbage-collected. It supports multiple 
programming, including structured (particularly, procedural), object oriented and 
functional programming. Python is often described as a "batteries included" 
language due to its comprehensive standard library. 
3.2.3  CHARACTERISTICS OF PYTHON 
➢ Easy to code 
➢ High Level language 
➢ Free and Open Source 
➢ Integrated easily with other languages such as C, C++  
➢ Portable language as it can be run on any platform such as Windows, Linux, 
Unix. 
➢ Large standard library which provides a rich set of module and functions. 
➢ Graphical User interfaces can be made using a module such as PyQt5, PyQt4, 
wx Python, or Tk in python. 
12 
 
13  
CHAPTER 4 
    PROJECT DESIGN 
 
 4.1   OBJECTIVE 
The main objective is to classify the histopathological images of breast cancer as 
positive or negative. A model is proposed for the classification of breast cancer on 
the histopathological images by using a novel deep learning method known as 
“Convolutional Neural Network”. 
 
  
 4.2   FLOW CHART 
         
  Labels                                                                                     Loss functions 
   
 
 
          Training                   Pre -                           Feature                Convolution                Prediction 
          Image set                 Processing                 Extraction         Neural network model 
                                                                                                
 
  
             
               Test                      Pre -                            Feature            Convolution               Classified  
          Image set                 Processing                 Extraction          Neural Network                result 
                                                                                             
Figure 4.1 WORKFLOW OF THE PROCESS 
 
4.3    
MODULE DESCRIPTION OF THE MODEL 
In deep learning, a convolutional neural network (CNN) is a type of deep neural 
networks, which deals with the set of data to extract information about that data. In 
CNN, the neural networks are trained using a heavy set of data so that the CNN 
can extract the feature of given input. When the input is given, first image 
preprocessing is done then the feature extraction occurs on the basis of set of data 
stored. The classification of data is done and output is shown as the result. There 
are three modules used: i) Pre-Processing, ii) Training the model and iii) Testing 
the model. 
CI features          
Input           
maps                
SI feature          
maps                
C2 feature        
maps                 
S2 feature  
maps 
Output 
Convolutions                               
Subsampling     Convolutions    Subsampling    Convolutions 
Figure 4.2 CNN ARCHITECTURE 
4.3.1  PRE-PROCESSING 
The pre-processing steps were conducted with resizing, patch, and augmentation. 
The first pre-processing step normalizes the size of the input images. Almost all 
the radiographs were rectangles of different heights and too large (median value 
of matrix size ≥1,800). Accordingly, we resized all images to a standardized 32×32 
pixel square, through a combination of preserving their aspect ratios and using 
zero-padding. The investigation of deep learning efficiency depends on the input 
14 
data. Therefore, in the second processing step is where input images are pre
processed by using a patch (a cropped part of each image). A patch was extracted 
using a bounding box so that it contains sufficient maxillary sinus segmentation for 
analysis. Finally, data augmentation was conducted for just the training dataset, 
using mirror images that were reversed left to right and rotated −30, −10, 10, and 
30 degrees.   
4.3.2   TRAINING THE MODEL 
After the pre-processing stage the data were sent to the training phase where the 
dataset is first divided into two classes namely cancerous and non-cancerous. The 
number of cancerous images should be equal to number of non-cancerous images 
to maintain a balanced dataset. The model training includes classification report 
that will save the model. After saving the model, it will be trained with 5 epoch (an 
epoch is the date and time relative to which a computer's clock and timestamp 
values are determined). 
A CNN usually takes an order 3 tensor as its input. Higher order tensor inputs, 
however, can handle by CNN in similar fashion.  The input then sequentially goes 
through a series of processing. One processing step is usually called a layer, which 
could be a convolutional layer, pooling layer, normalization layer, fully connected 
layer, loss layer etc..,. Here we have used CNN with the following layers: 
Input layer: In this layer, an image is given as an input and produces output which 
is used to feed the Convolutional layers. In our example, input is of (32 X 32) is 
taken into consideration and the number of channel of image is 3 for RGB. x  
Convolutional layers: In this layer, input image is convolved with a set of learnable 
filters, which produces a feature map corresponding to each image in the output 
image. In our model, there are six Convolutional layers. For first three layers size 
of the kernels is of 5 X 5 and padding is set to zero and the stride is set to two and 
for next three layers, we have kept the size of kernel to be 3 X 3. 
15 
Fully Connected Layer or inner product layer: In this layer neurons are fully 
connected to each other and producing the result. Here input is simply treated as 
a vector and produce an output in the form of a single vector. Two inner product 
layers. The last layer is a fully connected layer where a softmax layer is used to 
classify the input image. Total number of classes used in our case is two, one for 
benign and other for malignant. 
Pooling Layer: Convolutional layers bring out the features of images with precise 
positions. If the positions change, even a small amount for any reason, the feature 
maps will be different. To overcome this problem, the down sampling process must 
be done at the output of every convolutional layer. With convolutional layers, down 
sampling can be done by changing the convolution’s phase across the image. A 
more acceptable and common method is to use a pooling layer. Using this process, 
outputs will be more accurate. 
The abstract description of the CNN structure: 
�
�𝟏 →𝒘𝟏 →𝒙𝟐 →  .  .  .  →𝒙𝑳−𝟏 → 𝒘𝑳−𝟏 →𝒙𝑳 → 𝒘𝑳 →𝒛  
The above equation illustrates how CNN runs layer by layer in a forward pass. The 
input is 𝒙𝟏, usually an image (order 3 tensor). It goes through the processing in the 
first layer, which is the first box. We denote the parameters involved in the first 
layer’s processing collectively as tensor 𝒘𝟏. The output of the first layer 𝒙𝟐, which 
also act as the input to the second layer processing. The process proceeds till all 
the layers in the CNN has been finished which outputs 𝒙𝑳. One additional layer, 
however, is added for backward error propagation in CNN. Commonly used 
strategy is to output 𝒙𝑳 as a C dimensional vector, whose i th entry encodes the 
prediction. In general, 𝒙𝑳 may have other forms of interpretation. The last layer will 
be a loss layer if t is the corresponding target value for the input 𝒙𝟏 ,then the cost 
or loss function can be predicted as,  
�
� = 𝟏
 𝟐
 ||(𝒕 − 𝒙𝑳)(𝒕 − 𝒙𝑳)||   
16 
 
17  
The CNN structure for the Breast cancer classification is given below 
 
32             7                        32 
      
     32                  7                                7                                 
 
 
 
 
 
                 32                 1920                         1920                                  1920           1920             2 
 
                 Input          DenseNet              Global Average                     Dropout   Normalization   Dense     
                 Image                                      Pooling  
 
 
                                               Convolutional Layers                                        Fully Connected Layer 
 
 
Figure 4.3 WORKING EXAMPLE OF CNN ARCHITECTURE  
 
 
 
 
 
 
 
 
 
 
 
 
Total params: 18,333,506 
Trainable params: 18,100,610 
Non-trainable params: 232,896 
Layer (type) Output Shape Param 
densenet201 (Functional) (None, 7, 7,1920) 18321984 
 
global_average_pooling2d (None,1920) 0 
dropout (Dropout) (None, 1920) 0 
batch_normalization (None, 1920) 0 
dense (Dense) (None, 2) 3842 
 
18  
The model output will give the accuracy in the range of 92-95%.   
 
                              TP +TN 
Accuracy =     
                        TP + FN + FP + TN 
 
                                                  TP  
Precision =     
                           TP + FN  
 
                                TP 
Recall      =     
                           TP + FN 
 
 
                         2 x Precision x Recall 
F1            =     
                          Precision + Recall 
 
          TP-TRUE POSITIVE 
           TN-TRUE NEGATIVE  
           FP-FALSE POSITIVE 
           FN-FALSE NEGATIVE 
 
 
 
4.3.3   TESTING THE MODEL 
For the testing stage, same preprocessing steps are applied on the testing data 
which were used in training. Image patches are created in the same fashion as in 
the training and these patches are then passed to the trained model. The patches 
from the histopathology images used in the testing stage are completely unseen 
for the model. The model classified the patches as either a positive sample (cancer) 
or as a negative sample (background). 
ENTER INPUT IMAGE NAME : non-Cancerous.png 
[1.3755745e-07, 0.918] 
Normal 
Figure 4.4 REPRSENTATION OF TRAINING AND TESTING THE MODEL 
19 
4.4  DATA AUGMENTATION TECHNIQUE 
Data augmentation is an effective and widely used tool to avoid the overfitting 
problem by creating additional data. More complex systems using deep neural 
network have low bias but generate high variance. It means that these systems 
overfit the training data and will demonstrate bad performance on test data or on 
data that had not seen before. It would result in greater errors in prediction. 
Therefore, the increased diversity from data augmentation decreases the model’s 
variance by improving it at generalizing. The proposed system uses Gaussian 
Mixture Models (GMMs) for modeling and classification. Gaussian Mixture Models 
(GMMs) assume that there are a certain number of Gaussian distributions, and 
each of these distributions represent a cluster. Hence, a Gaussian Mixture Model 
tends to group the data points belonging to a single distribution together. Gaussian 
Mixture Models use the soft clustering technique for assigning data points to 
Gaussian distributions.
 20 
CHAPTER 5 
IMPLEMENTATION AND RESULTS 
5.1 IMPLEMENTATION 
Implementation is the most crucial stage in achieving a successful system 
and giving the users confidence that new system is effective and workable. 
Implementation of this project refers to the installation of the packages in its real 
environment to the full satisfaction of the users and operations of the system. 
Testing is done individually at the time of development using the data and 
verification is done the way specified in the program specification. In short, 
implementation constitutes all activities that are required to put an already tested 
and completed package into operation. The success of any information system lies 
in its successful implementation. System implementation is the stage in the project 
where the theoretical design is turned into a working system. The most critical stage 
is achieving a successful system and in giving confidence on the new system for 
the user that it will work efficiently and effectively. The existing system was long 
time process. 
5.1.1   IMPORT LIBRARIES 
import json 
import math 
import os 
import cv2 
from PIL import Image 
import numpy as np 
from keras import layers 
from tensorflow.keras.applications import ResNet50,MobileNet, DenseNet201, In
 ceptionV3, NASNetLarge, InceptionResNetV2, NASNetMobile 
21 
 
22  
from keras.callbacks import Callback, ModelCheckpoint, ReduceLROnPlateau, T
 ensorBoard 
from keras.preprocessing.image import ImageDataGenerator 
from keras.utils.np_utils import to_categorical 
from keras.models import Sequential 
from tensorflow.keras.optimizers import Adam 
import matplotlib.pyplot as plt 
import pandas as pd 
from sklearn.model_selection import train_test_split 
from sklearn.metrics import cohen_kappa_score, accuracy_score 
import scipy 
from tqdm import tqdm 
import tensorflow as tf 
from keras import backend as K 
import gc 
from functools import partial 
from sklearn import metrics 
from collections import Counter 
import json 
import itertools 
%matplotlib inline 
 
          5.1.2   DATA PROCESSING 
 
def Dataset_loader(DIR, RESIZE, sigmaX=10): 
IMG = [] 
read = lambda imname: np.asarray(Image.open(imname).convert("RGB")) 
for IMAGE_NAME in tqdm(os.listdir(DIR)): 
PATH = os.path.join(DIR,IMAGE_NAME) 
_, ftype = os.path.splitext(PATH) 
if ftype == ".png": 
img = read(PATH) 
img = cv2.resize(img, (RESIZE,RESIZE)) 
IMG.append(np.array(img)) 
return IMG 
benign_train = np.array(Dataset_loader('data/train/benign',224)) 
malign_train = np.array(Dataset_loader('data/train/malignant',224)) 
benign_test = np.array(Dataset_loader('data/validation/benign',224)) 
malign_test = np.array(Dataset_loader('data/validation/malignant',224) 
5.1.3   TRAINING AND EVALUATION SPLIT 
X_train = np.concatenate((benign_train, malign_train), axis = 0) 
Y_train = np.concatenate((benign_train_label, malign_train_label), axis = 0) 
X_test = np.concatenate((benign_test, malign_test), axis = 0) 
Y_test = np.concatenate((benign_test_label, malign_test_label), axis = 0) 
s = np.arange(X_train.shape[0]) 
np.random.shuffle(s) 
X_train = X_train[s] 
Y_train = Y_train[s] 
s = np.arange(X_test.shape[0]) 
23 
 
24  
np.random.shuffle(s) 
X_test = X_test[s] 
Y_test = Y_test[s] 
Y_train = to_categorical(Y_train, num_classes= 2) 
Y_test = to_categorical(Y_test, num_classes= 2) 
x_train, x_val, y_train, y_val = train_test_split( 
    X_train, Y_train,  
    test_size=0.2,  
    random_state=11 
) 
   
  5.1.4    DATA GENERATOR 
 
w=60 
h=40 
fig=plt.figure(figsize=(15, 15)) 
columns = 4 
rows = 3 
 
for i in range(1, columns*rows +1): 
    ax = fig.add_subplot(rows, columns, i) 
    if np.argmax(Y_train[i]) == 0: 
        ax.title.set_text('Benign') 
    else: 
        ax.title.set_text('Malignant') 
    plt.imshow(x_train[i], interpolation='nearest') 
plt.show() 
BATCH_SIZE = 1 
train_generator = ImageDataGenerator( 
zoom_range=2,   
rotation_range = 90, 
horizontal_flip=True,   
vertical_flip=True, 
) 
5.1.5    MODEL DEFINITION 
def build_model(backbone, lr=1e-4): 
model = Sequential() 
model.add(backbone) 
model.add(layers.GlobalAveragePooling2D()) 
model.add(layers.Dropout(0.5)) 
model.add(layers.BatchNormalization()) 
model.add(layers.Dense(2, activation='softmax')) 
model.compile( 
loss='binary_crossentropy', 
optimizer=Adam(lr=lr), 
metrics=['accuracy'] 
) 
return model 
K.clear_session() 
gc.collect() 
resnet = DenseNet201( 
weights='imagenet', 
include_top=False, 
25 
input_shape=(224,224,3) 
) 
model = build_model(resnet ,lr = 1e-4) 
model.summary() 
5.1.6   TRAINING DATASET 
history = model.fit_generator( 
train_generator.flow(x_train, y_train, batch_size=BATCH_SIZE), 
steps_per_epoch=x_train.shape[0] / BATCH_SIZE, 
epochs=20, 
validation_data=(x_val, y_val), 
callbacks=[learn_control, checkpoint] 
) 
5.1.7   PLOTTING THE GRAPH 
with open('history.json', 'w') as f: 
json.dump(str(history.history), f) 
history_df = pd.DataFrame(history.history) 
history_df[['acc', 'val_acc']].plot() 
history_df = pd.DataFrame(history.history) 
history_df[['loss', 'val_loss']].plot() 
26 
 
27  
          5.1.8    IMAGE PREDICTION 
 
CATEGORIES = ["Normal","Cancer"] 
image =input("ENTER INPUT IMAGE NAME: ") 
from google.colab.patches import cv2_imshow 
x=cv2.imread(image,1) 
cv2_imshow(x) 
IMG = [] 
read = lambda imname: np.asarray(Image.open(imname).convert("RGB")) 
img = read(image)            
img = cv2.resize(img, (224,224)) 
IMG.append(np.array(img)) 
prediction = model.predict(np.array(IMG)) 
prediction = list(prediction[0]) 
print(prediction) 
print(CATEGORIES[prediction.index(max(prediction))]) 
 
 
 
 
 
 
 
 
5.2  SAMPLE OUTPUT 
5.2.1    ACCURACY AND LOSS GRAPH 
Figure 5.1   ACCURACY GRAPH 
Figure 5.2    LOSS GRAPH 
28 
 
29  
          5.2.2  PREDICTION 
 
 5.2.2.1    CANCEROUS PATCH 
 
 
                                              FIGURE 5.3 INPUT IMAGE 
 
 
 
                               ENTER INPUT IMAGE NAME: 2.png 
 
 
   [1.3744735e-06, 0.957] 
   Cancer 
 
                             FIGURE 5.4 OUTPUT 
 
 
 
30  
  5.2.2.1    NON - CANCEROUS PATCH 
 
 
 
 
 
                                              FIGURE 5.5 INPUT IMAGE 
 
 
                                  ENTER INPUT IMAGE NAME: 3.png 
 
 
    
 
 
 
             [1.3755745e-07, 0.918] 
         Normal 
 
                                   FIGURE 5.6 OUTPUT 
 
 
 
 
31  
CHAPTER 6 
                                                  CONCLUSION 
 
The goal of our work was to detect and classify the cancerous and non-cancerous 
histopathological images using Deep learning. A novel method of deep learning technique 
known as Convolutional Neural Network was proposed. The proposed method includes three 
phases namely, Pre-processing phase, Testing phase and training phase. The 
histopathological images used in the process is in the form of RGB. The Region of interest 
(ROI) was cropped from the images and is sent to convolutional layers in the Pre-processing 
phase. In the Training phase, the images are trained with equal number of both cancerous and 
non-cancerous patches of histopathological images. The training is done with a duration of 5 
epoch which is more efficient than the already existing systems. The testing is done after the 
training phase by giving an input image and the model will classify it as either cancerous or 
non-cancerous along with the display of the image. This method produced an average of 92% 
testing accuracy on testing samples and achieved the highest performance in the classification 
of Breast Cancer. 
 In future, we will explore and apply our work on pre-trained models trained with a larger 
number of layers and may also explore patch-based models with data augmentation 
techniques to classify Breast Cancer using histopathological images. 
 
 
 
 
 
32  
 
                                           CHAPTER  7  
                                                       REFERENCES 
 
[1] M. Velikova, M. Samulski, P. J. F. Lucas, and N. Karssemeijer, “Improved mammographic 
CAD performance using multi-view information: A Bayesian network framework'', Phys. 
Med. Biol., vol. 54, no. 5, pp. 1131_1147, Mar. 2009 
[2] A. J. Bekker, H. Greenspan, and J. Goldberger, “A multi-view deep learning architecture 
for classification of breast microcalcifications'' ], Jun. 2016 
[3] T. Araujo, G. Aresta, E. Castro, J. Rouco, P. Aguiar, C. Eloy, A. Polónia, and A. Campilho, 
“Classification of breast cancer histology images using convolutional neural networks” 
, IEEE  2017 
[4] M. Nilashi, O. Ibrahim, H. Ahmadi, and L. Shahmoradi, “A knowledge based system for 
breast cancer classification using fuzzy logic method '', Telematics Informat., Jul. 2017 
[5] M. S. Ashraf, O. I. and Siti, “Intelligent breast cancer diagnosis based on enhanced 
Pareto optimal and multilayer perceptron neural network'', Int. J. Comput. Aided Eng. 
Technol.,2018. 
[6] H.Wang, B. Zheng, S.W. Yoon, and H. S. Ko, “A support vector machine based 
ensemble algorithm for breast cancer diagnosis,'' Eur. J. Oper. Res.,vol. 267, no. 2, pp. 
687_699, Jun. 2018 
[7] Irum Hirra, Mubashir Ahmad , Ayaz Hussain, M. Usman Ashraf, Iftikhar Ahmed Saeed, 
Syed Furqan Qadri , Ahmed M. Alghamdi, and Ahmed S. Alfakeed “Breast Cancer 
Classification From Histopathological Images Using Patch-Based Deep Learning 
Modelling” , IEEE Access 2021 
 
 
  
