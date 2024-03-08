# Microsoft Fabric Hackathon Model

This repository contains the codebase for a model developed during the Microsoft Fabric Hackathon. The model facilitates the analysis of quantitative and qualitative data from the Immigration, Refugees and Citizenship Canada (IRCC) website to predicts scores for Canadian Permanent Resident draw scores, provide augmented and easy access to information through a RAG Chatbot and visualized data using Microsoft Fabric. Therefore helping thousands of immgrants achieve their dreams with ease and peace. 

## Microsoft Fabric Co-Pilot Extension

Enable individuals to build custom dashboard on Microsoft PowerBI by stating what dashboard they would prefer to see through the RAG Chatbot

This repo retrieved data from the Immigration, Refugees and Citizenship Canada (IRCC)
[https://www.canada.ca/en/immigration-refugees-citizenship](https://www.canada.ca/en/immigration-refugees-citizenship.html)

## Overview

The model performs the following tasks:

1. **Data Collection and Storage**:
    - Retrieves quantitative and qualitative data from the IRCC website.
    - Utilizes OpenAI GPT-4 to analyze the qualitative data
    - uploads these both quantitative and analysed qualitative data to a Fabric Lakehouse
    - Uses data pipeline to automate the process of updating qualitative and quantitative data from IRCC to Lakehouse weekly
      with new data.

2. **Prediction Model**:
    - Receives quantitative and qualitative evaluation data from the Fabric Lakehouse into a Synapse datascience prediction models.
    - Predicts scores for the PR draw across different classes.
    - Stores these predictions into the Fabric Lakehouse.

3. **RAG Chatbot Interface**:
    - Develops a retrieval augmented generative (RAG) model with OpenAI GPT-4.
    - Retrieves quantitative, qualitative data and prediction data from the Fabric Lakehouse.
    - Answers various queries through a chatbot interface.

4. **Data Visualization**:
    - Utilizes PowerBI to visualize qualitative data, quantitative data from IRCC, and predictions from the model.
  
![Model Architecture](https://github.com/Pelumioluwa/Microsoft-Fabric-Hackathon/blob/main/PR%20Quantitative%20Data%20PR%20Scores%20Table.jpg)

## Tools Utilized

To build the projectn the following tools were used:

1. Microsoft Fabric Synapse Data Science:
   - Ridge Regression model
   - LGBM Regressor
2. Microsoft AI Search
3. Microsoft Fabric Data Pipeline
4. Microsoft Fabric Data Lakehouse
5. Microsoft OpenAI GPT-4
6. Microsoft OpenAI ADA- embedding
7. Microsoft PowerBI
8. Microsoft Fabric Experimentation
9. Microsoft Copilot

## Repository Structure))
- **/data_pipeline**: Contains scripts and configurations for the automated data pipeline.
- **/prediction_model**: Includes code for the Synapse prediction model.
- **/rag_chatbot**: Contains code for the retrieval augmented generative model and the chatbot interface.
- **/visualization**: Holds files and scripts for data visualization using PowerBI.

## Contributing

I would appreciate any thoughts or contributions to improve the model and its functionalities. If you'd like to contribute, please kindly reach out to me via pelumi@yorku.ca


## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- Thanks to Microsoft Fabric for organizing the hackathon.
- Special thanks to the developers and contributors of OpenAI GPT-4 and Synapse for their incredible tools and technologies.

---

Feel free to expand this README with more details or instructions as needed. Happy hacking!
