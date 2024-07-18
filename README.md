

# Attribute Value Extraction
<a name="readme-top"></a>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href>Introduction</a></li>
    <li>
        <a href>Solution Architecture</a>
    </li>
    <li><a href>Models</a></li>
    <li><a href>Example</a></li>
    <li><a href >End to End pipeline</a></li>
    <!-- <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li> -->
  </ol>
</details>

# Introduction
Attribute extraction from image is a task that involves using visual concepts to map the probabilities of commonly used word.Automatically extracting attributes from the image is an epoch-making task because it needs to precisely predict not just the objects but also their attributes and activities are involved in making the scene. It can be used in many areas, for example applied in the context of e-commerce where product attribute values are extracted from product offers.
Automated extraction of product attributes from images enhances product cataloging by providing detailed and accurate descriptions. Traditionally a manual process, AI now automates this, analyzing images and extracting relevant attributes, such as color, material, and logos and more.This technology saves time and resources while ensuring high-quality, consistent product information across platforms.


Using AI for attribute extraction allows companies to produce detailed and accurate product listings that better connect with consumers. By transforming plain product images into detailed descriptions, businesses can improve engagement and convey value more effectively, driving higher conversion rates and providing a competitive edge in the digital marketplace.

## What we have?
We have an end to end framework which could be utilized to automatically extract attributes from images using a predefined configuration.The available code is developed to  allows users to upload an image of a product and select the attributes they want to extract based on some particular categories, but similar approach could be followed to extract attributes for different products. 






# Solution Architecture

### Solution Diagram
An overview of the proposed framework:

![overview image](https://github.com/Kunilata09/Rough/blob/main/ARC_DIA.png)


##  Data
The image data for this work is collected from the GAP webpage , which is publicly avaialable .



### Architecture Overview

The goal of this project is to automate the extraction of various attributes from product images using a Vision Question Answering model. Given an image and a set of predefined questions, the BLIP VQA model analyzes the image and provides answers, facilitating the understanding and cataloging of product attributes.The complete process follows the below steps


- Collect Input Images :
   Gather all images that we need to extract attributes automatically.
- Category Selection :  Manually assign a category to each image based on visual inspection. This step requires domain knowledge to accurately categorize the images.
- Load Configuration :Use a configuration file (e.g., JSON or YAML) that maps categories to attributes and corresponding questions. This configuration should be thoroughly tested and validated against ground truth data to ensure accuracy. Hence under each category we are having set of attributes and all attribute correspondense to a relevent question. 

      For example-
      Quantities: How many products are there?
      Colour: What are the colors present in the image?

- Model :Initialize and configure the BLIP Processor and BLIPForQuestionAnswering model to prepare for processing images and answering questions.


<div id="top"></div>
<h3 align="left">Example</h3>



![](https://github.com/Kunilata09/Rough/blob/main/Screenshot%202024-07-16%20163827.png)






## End to End pipeline:
We have successfully implemented the above approaches and have created an end to end pipeline. to make process very simple. you just need use [this](https://github.com/tpjesudhas/cv_component/blob/main/usecases/ImageTrendAnalysis/App.py) code and below instructions to run them.
### Prerequisites

- Python 3.8 or higher
### Install Dependencies

Install all the requirements to run the code

        $ pip install -r requirements.txt
        
Based on your product ,make a config file for attributes and the corresponding questions. 

### Run the app
 
        $ python app.py
        


Note:- This was our *version 1 release*. We, are continuosly working to improve the accuracy of the model.




Features

BLIP VQA Model: Utilizes the BLIP (Bootstrapping Language-Image Pre-training) VQA model for answering questions based on image content.
Versatile Application: Can be applied to various product categories for attribute extraction.
