# Microsoft Fabric Hackathon Model

This repository contains the codebase for a model developed during the Microsoft Fabric Hackathon. The model facilitates the analysis of quantitative and qualitative data from the Immigration, Refugees and Citizenship Canada (IRCC) website, predicts scores for Canadian Permanent Resident draw scores, leverages on RAG architecture via a chatbot interface, and visualizes the data using PowerBI. 

This repo retrieved data from the Immigration, Refugees and Citizenship Canada (IRCC)
[https://www.canada.ca/en/immigration-refugees-citizenship](https://www.canada.ca/en/immigration-refugees-citizenship.html)

## Overview

The model performs the following tasks:

1. **Data Collection and Storage**:
    - Retrieves quantitative and qualitative data from the IRCC website.
    - Utilizes OpenAI GPT-4 to analyze the qualitative data.
    - uploads these both quantitative and analysed qualitative data to a Fabric Lakehouse
    - Automates the process through a data pipeline and updates the lakehouse weekly with new data.

2. **Prediction Model**:
    - Feeds quantitative and qualitative evaluation data from the Fabric Lakehouse into a Synapse prediction model.
    - Predicts scores for the PR draw across different classes.
    - Stores these predictions into the Fabric Lakehouse.

3. **Chatbot Interface**:
    - Develops a retrieval augmented generative model with OpenAI GPT-4.
    - Retrieves quantitative and qualitative data from the Fabric Lakehouse.
    - Answers various queries through a chatbot interface.

4. **Data Visualization**:
    - Utilizes PowerBI to visualize qualitative data, quantitative data from IRCC, and predictions from the model.
  
![Model Architecture](https://github.com/Pelumioluwa/Microsoft-Fabric-Hackathon/blob/main/PR%20Quantitative%20Data%20PR%20Scores%20Table.jpg)

## Repository Structure

- **/data_pipeline**: Contains scripts and configurations for the automated data pipeline.
- **/prediction_model**: Includes code for the Synapse prediction model.
- **/rag_chatbot**: Contains code for the retrieval augmented generative model and the chatbot interface.
- **/visualization**: Holds files and scripts for data visualization using PowerBI.

## Getting Started

To get started with the model, follow these steps:

1. Clone this repository to your local machine.
2. Set up the necessary dependencies for each component of the model.
3. Configure access to the Fabric Lakehouse for data storage and retrieval.
4. Download codebase and run on local machine.


## Contributing

I would appreciate any thoughts or contributions to improve the model and its functionalities. If you'd like to contribute, please kindly reach out to me via pelumi@yorku.ca


## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- Thanks to Microsoft Fabric for organizing the hackathon.
- Special thanks to the developers and contributors of OpenAI GPT-4 and Synapse for their incredible tools and technologies.

---

Feel free to expand this README with more details or instructions as needed. Happy hacking!
