# Cloud Services

Main goal is to give students a sense of why they might need cloud services and, when they do, what their options are.

## Prerequisites

This lecture asks the instructor to demonstrate:

- uploading notebooks to databricks and to colab
- a flask app
- connecting to an AWS S3 bucket

Ideally, instructor will have the relevant accounts set up and a demonstrable flask app!
 
## Learning Goals

- Explain the general concept of "the cloud"
- Understand the cases where hardware acceleration is useful
- Understand the cases where cloud storage is useful
- Explain the difference between a "cloud database" and a "storage bucket"
- Explain the purpose of deploying a machine learning model
- Understand the basics of some popular deployment techniques
- Describe the utility of full-stack web application

## Lecture Materials

[Jupyter Notebook: Cloud Services](cloud_services.ipynb)

## Lesson Plan

Provide a breakdown of the lecture activities using the structure below. 

### Introduction (5 Mins)

What the cloud is (just someone else's computer!) and why you might want to use cloud services (three main reasons: hardware acceleration, large-file storage, model serving).

### Hardware Acceleration (10 Mins)

Make the contrast between using packages like NumPy (software acceleration) and uploading your whole notebook to Google Colab (hardware acceleration).

Demo importing notebooks into other platforms. (Should be a familiar concept from the big data lectures.)

### Cloud Storage (10 Mins)

As usual, AWS is a leading player here. S3 buckets are very popular with FI students (and cheap).

### Flask (10 Mins)

INSTRUCTOR-SPECIFIC FOR NOW

### Pickling (10 Mins)

This may or may not be a review for students. But even if it is, good refresher on using `pickle` to save and to load objects, especially including fitted models.

### AWS S3 Demo (10 Mins)

Demonstrating how to connect to S3 buckets from a local Jupyter notebook. Key packages here are `boto3` and `s3fs`.

### Conclusion (5 Mins)

Let students know that it will be possible to get support for flask for future projects (esp. including capstone). "Thanks, everyone!"
