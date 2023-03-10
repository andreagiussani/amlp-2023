# Applied Machine Learning with Python - Academic Year 2022/23 - Bocconi University

## Instructor info
This course is held by Andrea Giussani, Academic Fellow in Computer Science.
You can reach him out either at [:email:](andrea.giussani@unibocconi.it) or on [Linkedin](https://it.linkedin.com/in/andrea-giussani).

## Repository Structure
 - `online_material`: in this folder, you will find external links that might help you in better understading the material.
 - `papers`: in this folder, you will find relevant papers on Machine Learning.
 - `class material`: in this folder, you will be available to investigate the class material.

## Setting Up the Google Colab Environment

The Google Colab is a product from Google Research which allows
> anybody to write and execute arbitrary python code through the browser, and is especially well suited to machine learning, data analysis and education. More technically, Colab is a hosted Jupyter notebook service that requires no setup to use, while providing free access to computing resources including GPUs.

For more information, please visit the following [link](https://research.google.com/colaboratory/faq.html).

Here, we provide a short tutorial on how to upload the data on that environemnt via Google drive, and then use the Google colab to run your analysis.
Please, note that we assume you have a google account to access to this Google product.

### 1. Open a Google Colab session

From your favourite browser, open a new colab notebook via the following [link](https://colab.research.google.com)

### 2. Mount your drive on colab

We assume you have placed the data into the `My Drive` folder. If so, connecting your drive to a google machine is pretty easy, using the python google library: just run the following code snippet

```python
from google.colab import drive
drive.mount('/content/drive')
```
After an authorisation check, you will be able to interact with your drive content either from the file browser side panel (easier) or using command-line utilities.

### 3. Clone the GitHub Repository on your Drive
I suggest to create a folder inside your drive. For example, call it `bocconi.amlp`. Then, in any colab notebook cell, type the following commands
```python
%cd '/content/drive/My Drive/bocconi.amlp'
```
and then clone the following repository:
```python
!git clone https://github.com/andreagiussani/Applied_Machine_Learning_with_Python.git
```
After this, the source library is available in your session. However, we need to perform two extra steps before working with it. <br>
First, we need to move to the `egeaML` folder using `%cd Applied_Machine_Learning_with_Python`, and then we need to install the `wget` library inside our session - this library is not preinstalled in Colab - with the pip manager. Just type in any cell `!pip install wget`.

### 4. Let's get our hands dirty
Now, you have to navigate inside the Google Drive folder where the repo has been cloned. Once there, you just need to type, say,
```python
from egeaML.egeaML import DataIngestion
raw_data = DataIngestion(df='/content/drive/MyDrive/bocconi.amlp/Applied_Machine_Learning_with_Python/data/data_intro.csv', col_target='male')
df = raw_data.load_data()
df.head()
```
inside your Google Colab session. And that's it! :smile:

Are you ready? Let us get started!
