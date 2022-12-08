# FYP-Smart-City-Research-Project

This repository contains project artefacts that are produced as part of the Final Year Project (FYP) in Singapore Management University(SMU) completed by myself and a fellow undergraduate, with the guidance from a project sponsor and supervision from a project supervisor. 

*Note:Permission have been obtained by the project supervisor and sponsor on sharing the details of some portion of the project. (Due to prior confidentiality agreement signed, raw data collected from survey done in this project will not be shared)*

The project sponsor is an assistant professor at the School of Computing and Information Systems, Singapore Management University (SMU-SCIS) with an interest in Computational Social Science. She has kindly provided us with a Computational Social Science research project that is inspired by the the research paper “Aesthetic Capital: What makes London looks Beautiful, Quiet and Happy?” published by Yahoo Labs in 2014.

## Project Overview: 

Research Question: **Leveraging Image Analysis and crowdsourcing to understand public perceptions on “What makes the area surrounding MRT stations in Singapore look Beautiful, Safe, and Welcome?”**

<img src="https://user-images.githubusercontent.com/43470271/206454596-d93ee30a-badc-4fed-ba44-2feefb97ff40.png">

The project artefacts in this repository includes:
- Jupyter Notebook containing codes of image analyses (Color, Bag of Visual Words, Object Detection). Note that the codes were run on the Google Colab Platform but downloaded as Jupyter Notebook (.ipynb file extension)
- Presentation slide that has a high level description and explanation of our research project.

Note: Any references used in the project has been both in the last slide of the presentation and at respective code cells in the Jupyter Notebook.

### Project Insights from analyses done:
*Note:For more details on the analysis methods, please refer to the presentation slide*

<img src="https://user-images.githubusercontent.com/43470271/206454873-55f579a7-d350-41e3-97f0-f8ffad7158df.png">

**Descriptive Statistics**
Here are the results based on the image ratings derived from the survey responses:

<table>
  <tr>
    <th>Beautiful Metric</th>
    <th>Safe Metric</th>
    <th>Welcome Metric</th>
  </tr>
  <td>
    <img src="https://user-images.githubusercontent.com/43470271/206456426-3607f760-562f-4e6b-a635-fd0bd2e41da2.png">
  </td>
  <td>
    <img src="https://user-images.githubusercontent.com/43470271/206457155-7e3c42d7-30d0-45f0-98b4-239429148752.png">
  </td>
    <td>
      <img src="https://user-images.githubusercontent.com/43470271/206457260-c8f8b6ff-476f-46a3-b779-3246a55d7299.png">
      <img src="https://user-images.githubusercontent.com/43470271/206457474-e7790da9-be3f-42bf-a077-7fe10be23cc6.png">
  </td>
  </table>
  
**Image Analysis(Colours)**
For colours analysis, we used the skimage image processing python package to extract the RGB colours from each MRT image. Then, linear regression was applied on the colors extracted from each image to find out the effects of colors on image perception ratings for each of the 3 metrics (Beautiful,Safe, Welcome). Finally correlation analysis was done to select the colors that have a strong linear relationship with image perception ratings for each of the 3 image metrics. The results shown the the table below are statistically significant at 5% significance level. However, the r-square values of the linear regression models are low at 0.163, 0.098 and 0.123 respectively (for the qualities of "Beautiful", "Safe" and "Welcome”) which signifies that these colors alone are insufficient in explaining the changes in image ratings.

<table>
  <tr>
    <th>Beautiful Metric</th>
    <th>Safe Metric</th>
    <th>Welcome Metric</th>
  </tr>
  <td>
    <img src="https://user-images.githubusercontent.com/43470271/206465605-a8bb4861-6c92-458a-b89f-bd64ad5241db.png">
    <img src="https://user-images.githubusercontent.com/43470271/206465257-1c59201d-8a40-449b-ae9d-6d61ba45f306.png">
  </td>
  <td>
    <img src="https://user-images.githubusercontent.com/43470271/206465686-5e12387c-cfc6-4e92-868d-3a63e284996f.png">
  </td>
    <td>
      <img src="https://user-images.githubusercontent.com/43470271/206465855-9b58345c-818d-4d02-96cb-ddf267c21581.png">
  </td>
  </table>
  
**Image Analysis(Object Detection)**
 For object detection, we used a pre-trained deep learning object detection model from the opencv image processing python package to detect unique objects from all the MRT images and used correlation analysis to find the association between the unique objects detected in images and the image perception ratings for each of the 3 metrics (Beautiful,Safe, Welcome).
 
The results shown in the "Summary of Insights" table under the Project Overview for object detection are statistically significant at 5%
significance level. Image below is a snippet of objects detected by the object detection model.
  <img src="https://user-images.githubusercontent.com/43470271/206466860-2d008886-7502-4e4a-a9ab-575af81a45fd.png">

**Image Analysis(Bag of Visual Words)**
For Bag of visual words, we used an image feature detector from the skimage image processing python package to extract key features from all MRT images. Take an image of a person as shown below, a human would identify the person’s key features as the nose, eyes and mouth. Hence, the image feature extractor aims to do the same. 
<img src="https://user-images.githubusercontent.com/43470271/206468917-fd752a7e-d40b-43ef-8f26-2af6f1ecc166.png">

K-means clustering was used thereafter to group and differentiate the most distinct and comprehensive features across all the MRT images(visual words). Finally, correlation analysis was performed to select the visual words that have a strong linear relationship with image perception ratings for each of the 3 image metrics.The following picture is an example of strongly correlated visual words identified in the MRT images 
<img src="https://user-images.githubusercontent.com/43470271/206468732-62bf475d-0ec8-475b-bb5b-c15b1b421060.png">
