# UST - User Story Tutor

A onn-line tool to help teams that use agile practices to building better user stories.

## Description

The User Story Tutor (aka UST) receives as input a User Story text in English and presents personalized recommendations for improving it, with the support of a large language model (LLM). The tool also presents a prediction in Story Points, generated by a machine learning algorithm trained with data from other projects. The user is also presented with the User Story’s readability indexes, as they can be used to represent an indicator of text clarity.

UST supports agile teams during the construction of User Stories and assists the development process during the User Story preparation phase and in estimating task effort. UST consists of a web application that can be accessed using a browser on mobile devices, PCs, and notebooks. UST uses an LLM provided by OpenIA to recommend improvements and present readability indexes. 

The application was designed around 3 modules with well-defined functions. The Recommender module responds to User Story recommender requests. It is responsible for maintaining the prompt and combining it with the text of the new User Story, query-
ing OpenAI via API, and preparing the return for presentation to the user. The module that performs User Story estimates in Story Points uses a predictive model, already trained with historical data to assist developers in their estimates, acting as a reference for
the team responsible for estimating effort. Readability indexes are extracted from text with basic natural language processing techniques. 

## User Story NeoDataSet

This dataset includes User Story (or Issue) text descriptions, User Story titles, and Story Points from 33 software development projects, comprising a total of 20,479 User Stories (or issues) extracted from GitLab repositories, amounting to 12,262.7 Story Points. The mining process focused on GitLab’s top open-source projects that use agile software development methodologies and record task sizes in Story Points. Only tasks with the **State** attribute set to **Closed** and with the **Weight** attribute filled in were collected. The **Weight** field in GitLab is used to record the effort in Story Points. The data was mined between January 2023 and April 2023. The projects in the dataset have diverse characteristics, covering different programming languages, business domains, and geographic locations of the teams.

The paper below shortly this dataset in **section 4.1 Dataset**  

## Citation Suggestion
Neo, G. S.; Moura, J.; Almeida, H.; Neo, A. and Freitas Júnior, O. (2024). User Story Tutor (UST) to Support Agile Software Developers. In Proceedings of the 16th International Conference on Computer Supported Education - Volume 2: CSEDU; ISBN 978-989-758-697-2; ISSN 2184-5026, SciTePress, pages 51-62. DOI: 10.5220/0012619200003693 

## Demo on-line

[demo online](https://userstoryteach.streamlit.app/)

## Code details

For coding, we used StreamLit, a library for building open-source applications for machine learning and data science. The Recommender Module performs a query to OpenAI. The scikit-learn libraries were also used.

