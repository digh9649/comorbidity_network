This project is exploring comorbidity within the veteran community. Comorbidity, which is the co-occurrence of multiple health conditions, is a major concern for Veterans, impacting their well-being. The existing literature about comorbidities found in Veterans has established a strong relationship between mental health and chronic health conditions. Some areas explored include the correlation between PTSD and chronic pain. This project aims to find correlations between conditions by predicting missing links with a meta-learner and checking that they align with correlations established in existing literature. 
 
The research questions guiding this project: 
How well do the predicted missing links align with established knowledge about comorbidity associations?
Do specific network properties correlate with disease severity or impact on patients?

Initial Anticipated Findings: 
I would anticipate the meta-learner's predictions to align with existing observations about relationships between psychiatric conditions like PTSD, neurological conditions, chronic pain, and mortality. 
I would also anticipate that network properties like clustering coefficient and path lengths would give insights into disease severity that align with existing treatment plans/severity scores of these diseases. For example, a shorter average path length within the network may indicate a greater potential for disease interaction. This could suggest a higher likelihood of one disease triggering another or influencing its severity.

For this project, I will use the Human Disease Comorbidity network from the Index of Complex Networks. This network represents significant comorbidity associations of human disease conditions. It is a complete, weighted and directed network. The data was extracted from medical records of around 100,000 US Veterans between 2001 and 2017. The nodes represent disease conditions, specifically level 2 conditions under the classification scheme of the US Agency for Healthcare Research and Quality. The edges represent significant comorbidity associations between conditions. Each edge is weighted by the log odds increase of condition i given condition j. 

To predict missing links in this network, I used multiple topological predictors: Jaccard Coeff., degree product and shortest path. Using those predictors, I then built a meta-learner on top of them to predict the missing links. 

The individual predictors python notebook contains just the code for the three predictors. The meta-learner notebook contains the code for the individual predictors and builds the meta-learner. 

