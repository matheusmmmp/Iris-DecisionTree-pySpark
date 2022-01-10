<h1 align="center">
   :evergreen_tree: <a href="#"> Decision Tree in PySpark </a>
</h1>

<h3 align="center">
    A study about the use of a decision tree to predict the iris species of a flower
</h3>

<h4 align="center"> 
	 Status: Finished🚀
</h4>

<p align="center">
 <a href="#about">About</a> •
 <a href="#features">Features</a> •
 <a href="#how-it-works">How it works</a> • 
 <a href="#tech-stack">Tech Stack</a> • 
 <a href="#user-content-license">License</a>
</p>


## About

The decision tree is one of the oldest and most widely used methods in machine learning, and it can be used to classify an element by analyzing the relationships between its variables. These algorithms progressively subdivide the data into smaller and more specific sets, in terms of their attributes, until they reach a size simplified enough to be labeled. To do so, it is necessary to train the model with previously labeled data in order to apply it to new data.

The objective of this exercise is, through the use of pySpark in the Google Collab environment, to predict the iris species of a flower by the given characteristics. We will predict the species through the dataset of 3 iris species where 50 samples were collected for each species, considering the species as the output variable and the other variables of petal and sepal sizes as the input.

---

## Features

- [x] Using PySpark in Google Colab
- [x] Decision Tree Application
- [x] Random Forest Application
- [x] Use of the Algorithm Classifier
---

## How it works

This project was developed in Google Colab and uses the following dataset:

-   **[Iris Species Dataset](https://www.kaggle.com/uciml/iris)**


### Pre-requisites

To run spark in Colab, we need to first install all dependencies in Colab environment, i.e. Apache Spark 2.4.4 with hadoop 2.7, Java 8 and Findspark to find spark in the system. Follow the steps to install the dependencies:

#### Install Dependencies in your Colab environment

```bash

!sudo apt update
!sudo apt-get install openjdk-8-jdk-headless -qq > /dev/null
!wget -q https://archive.apache.org/dist/spark/spark-2.4.4/spark-2.4.4-bin-hadoop2.7.tgz
!tar xf spark-2.4.4-bin-hadoop2.7.tgz
!pip install -q findspark
import os
os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
os.environ["SPARK_HOME"] = "/content/spark-2.4.4-bin-hadoop2.7"
import findspark
findspark.init('spark-2.4.4-bin-hadoop2.7')

```


#### Importing Spark libraries

```bash

from pyspark.sql import SparkSession 
spark = SparkSession.builder \
    .master("local[*]") \
    .appName("ArvoreDecisao") \
    .getOrCreate()
import pyspark.sql.functions as f
import pyspark.sql.types as t
from pyspark.sql.types import *
from pyspark.sql.functions import *

```

---

## Tech Stack

The following tools were used in the construction of the project:

-   **[Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb?hl=pt_BR)**
-   **[Apache Spark](https://spark.apache.org/)**
-   **[Python](https://www.python.org/)**

#### **PySpark Libraries** 

-   **Vectors**
-   **VectorAssembler**
-   **StringIndexer**
-   **DecisionTreeClassifier**
-   **MulticlassClassificationEvaluator**
-   **RandomForestClassifier**
-   **Spark SQL**


---

## License

This project is under the license [MIT](./LICENSE).

Made with love by Matheus Pereira 👋🏽 [Get in Touch!](www.linkedin.com/in/matheus-de-medeiros-pereira-52b245140)
