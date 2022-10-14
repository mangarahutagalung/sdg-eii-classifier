# sdg-eii-classifier
A text classifier project with the Environment Innovation Initiative of the University of Pennsylvania. The goal of this project is to build a web scraper that can classify UPenn faculty members' SDG goals and research interests from their online biography.

Objective: The University of Pennsylvania is building a dashboard that shows each faculty member's research interest in relation to the UN's SDG goals. To do this, we need to classify each faculty member to any of the SDG goals from their biography that are available online. It will take a significant amount of time to manually analyze and classify 3,000+ faculty members. Therefore, we are building a web scraper that can automatically classify someone's research interest from their online biography.

Method: We have manually analyzed and classified around 2,000 faculty members' research interests in relation to the 16 SDG goals. We then built a web scraper and a classifier algorithm that utilizes these 2,000 data as our training and validation data. 

Steps (refer to the file names):
1. scraper: We first extracted around 2,000 faculty members' online biography from a list of websites provided by the university. After we analyze the data distribution, we realized that the data is extremely imbalanced for the positive connections. We then decided to augment new data based on the available positive data for each SDG goal.
2. data_augmentation: Here, we augmented new texts based on each SDG goal positive connection.
3. model_development: Finally, we experimented with different classifiers for each of the goals. We also experimented with different decision thresholds, to get the best combination of precision and recall.
4. saved-model (folder): We then saved the best model and parameters for each SDG goal in this folder. The models that are available in this folder are ready to be used to predict whether a given text or biography has a positive connection with each SDG goal.

I will create a more in-depth walkthrough regarding the logic and the script of this project soon. In the meantime, if you have any questions regarding this project, feel free to shoot me an email at mangara@sas.upenn.edu.

N.B.: the data provided in this repo is only showing a glimpse of the actual data. However, the websites and the connections are real. The purpose of sharing the data example is to allow people to try and run the script and experiment with them.
