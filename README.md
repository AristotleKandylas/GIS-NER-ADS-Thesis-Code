<h1 align="center"> GIS-NER-ADS-Thesis-Code </h1>
<p align="center">
    <a href="/LICENSE">
        <img alt="GitHub" src="https://img.shields.io/badge/License-GPLv3-blue.svg">
    </a>
</p>

<div align="center">
    <a href="/LOGO">
        <img src="https://onekeyresources.milwaukeetool.com/hs-fs/hubfs/GIS-Blog-Header.jpg?width=2309&name=GIS-Blog-Header.jpg" alt="Devicon Logo" height="300" />
    </a>
</div>

## Table
* [About the Project](#About-the-Project)
* [License](#License)


## :memo: About the Project
This is the official repository of my master thesis in Applied Data Science at Utrecht University.

My research project presents two deep learning-based NER systems to extract geographic phenomena from geo-analytical questions and classify them into core concepts of spatial information that conceptually model and distinguish spatial information. The NER systems are trained by BERT and Bi-LSTM models on 278 geo-analytical questions and tested on 31 validation questions, from a corpus that contains 309 questions in total. The evaluation and comparison results showed that the BERT model had higher accuracy, precision, recall and F1-score on recognizing core concepts in geo-analytical questions, compared to Bi-LSTM.

The project's code is available for everyone interesting but also for those who want to develop NLP solutions in the Geosciences scientific domain.

## :microscope: Demostration
For example, in a geo-analytical question answering system, the core concepts of a geo-analytical question can be recognized and annotated in the following way:
<p align="center">
<img src="https://user-images.githubusercontent.com/107751800/206797017-61eefa35-82f0-4050-be21-f0c0e852f49f.png" alt="example1"/>
</p>
<h5 align="center"> Annotation of core concepts in a geo-analytical question </h5>

The answer to this geo-analytical question can be visualized in a GIS software via a analytic GIS workflow as shown in the following figure :
<p align="center">
<img src="https://user-images.githubusercontent.com/107751800/206797615-51b13583-72be-4a87-9316-0b0dc0d33b85.png" alt="example1"/>
</p>
<h5 align="center"> Shortest network-based paths to a police station for specific PC4 areas </h5>

As this research has proved, the BERT outperfoms the Bi-LSTM model in core concept recognition tasks. In order to evaluate the BERT model's performance we selected three random geoanalytical questions from an another geo-analytical question corpus proposed by Xu, et al. (2022). As shown in the first figure (left side), fire stations and school are correctly recognized as objects. Also in the second figure (middle), the model correctly captures the vegetation areas as field nominal. Finally, as it is presented in the third figure, the model recognizes accurately in the third question, the number as content amount count and the traffic accidents as events.

<p align="center">
<img src="https://user-images.githubusercontent.com/107751800/206800620-cdbcbfbd-7538-480b-8f5b-a4c04fb3e4e0.png" alt="example1" height="300" />
</p>


## :floppy_disk: This repository
This repository contains the documentation and  the code written about the master thesis.


<ins>Specifically:<ins>

- **The preprocessing code** can be found in the <a href="https://github.com/AristotleKandylas/GIS-NER-ADS-Thesis-Code/blob/main/PRE_PROCESSING" target = "_blank"> PRE_PROCESSING folder</a> of this repository. This code reads the neccessary files (i.e. geoanalytical question corpus and core concepts dictionary) and creates the unified tags (e.g. object quality --> OBJQ) for the core concept recognition from the two Deep Learning models.

- **The tokenization code** can be found in the <a href="https://github.com/AristotleKandylas/GIS-NER-ADS-Thesis-Code/blob/main/TOKENIZATION" target = "_blank"> TOKENIZATION folder</a> of this repository. Contains all the code for the tokenization and the POS (Part Of Speech) tags creation of each geoanalytical question. In addition with this code, each token from each question is matched automatically to the corresponding unified tag which was generated in the <a href="https://github.com/AristotleKandylas/GIS-NER-ADS-Thesis-Code/blob/main/PRE_PROCESSING" target = "_blank"> **preprocessing code** </a>. The final output of this code is the generation of a .csv file which contains each geoanalytical question with the corresponding tokens, pos and and tags. 

- **The two developed Deep Learning Models'** can be found in the <a href="https://github.com/AristotleKandylas/GIS-NER-ADS-Thesis-Code/blob/main/DEEP_LEARNING_MODELS" target = "_blank"> DEEP_LEARNING_MODELS folder</a> of this repository. Contains all the developed code for the two Deep Learning models, including evalution metrics and visualizations.


## :clipboard: **Dataset**

As the **dataset** used in this research, was provided by the <a href="https://github.com/quangis" target = "_blank"> QuAnGIS research group</a>, and no consent was obtained to share it publicly, I am unable to share the dataset with the geoanalytical questions, in this repository.



## :envelope_with_arrow: Contact and contribution

For questions about this repository, please contact the author <a href = "https://github.com/AristotleKandylas" target = "_blank">Aristoteles Kandylas</a>, or open an Issue or Pull request in this repository.



## :balance_scale: License

This repository is licensed under a GNU General Public License v3.0. You can view the <a href= "https://github.com/AristotleKandylas/GIS-NER-ADS-Thesis-Code/blob/main/LICENSE" target = "_blank"> LICENSE here</a>.


