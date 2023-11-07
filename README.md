# LSTM Comment Flagger for [Blogzart](https://github.com/rakibulhaque9954/blog_remastered.git)
[日本語](https://github.com/rakibulhaque9954/Comment_Flag_LSTM_Model/blob/514ae75a47caf5d4d31aada24068fde0e3931556/%E6%97%A5%E6%9C%AC%E8%AA%9EREADME.md)

## Overview

The LSTM Comment Flagger is an advanced machine learning tool designed to automatically detect and flag inappropriate or toxic comments on digital platforms. Utilizing the Long Short-Term Memory (LSTM) architecture, this model has been meticulously trained on a comprehensive dataset to ensure high accuracy and performance.

## Features

- **High Accuracy**: Achieves 99% accuracy on the test dataset, ensuring reliable moderation.
- **Real-Time Analysis**: Capable of analyzing and flagging comments in real-time.
- **Scalability**: Designed to handle large volumes of data without performance degradation.
- **Ease of Integration**: Can be easily integrated with existing platforms via an API.

## Model Training

The LSTM Comment Flagger was trained from scratch on a dataset comprising 6,000 long datapoints. This dataset included a diverse range of comments to ensure the model's robustness across different scenarios.

## Usage

The model is deployed on Google Cloud Platform (GCP) and can be accessed via a RESTful API. This allows for seamless integration with web services and applications.

### API Endpoint

`https://lstm-flagger-ver-1-znzp2767aq-an.a.run.app`

### Request Format

To analyze a comment, send a GET request with the comment text as a query parameter:

```bash
curl -X GET "https://lstm-flagger-ver-1-znzp2767aq-an.a.run.app?text=your_comment_here"
```
### Response Format
The API returns a JSON object containing the classes of the comment and a flag indicating whether the comment is considered inappropriate.

```json
{
  "classes": ["toxic", "obscene"],
  "flag": true,
  "success": true
}
```
## Deployment

The LSTM Comment Flagger is currently deployed on GCP using Flask, allowing for high availability and scalability. The model's RESTful API communicates with the main blog platform hosted on Render to perform inference efficiently.

## Local Setup

For local testing and development, download the notebook itself:
```bash
https://github.com/rakibulhaque9954/Comment_Flag_LSTM_Model.git
```
## Conclusions

The LSTM Comment Flagger represents a significant step forward in automated content moderation. With its high accuracy and real-time performance, it serves as an essential tool for maintaining the quality of discourse on digital platforms. It showcases the potential of LSTM networks in understanding and moderating complex human language.

As the digital landscape evolves, we anticipate further enhancements to the model, such as incorporating more diverse datasets and exploring transfer learning to adapt to new forms of communication.
