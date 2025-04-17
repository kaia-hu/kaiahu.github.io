### Evaluating Commodity-Driven Deforestation
##### Author: Kaia Hu & Gargi Shekhar Mahajan
##### Prepared for Data Science & Big Data Course; Instructor: Raja Sooriamurthi
#### Description:
The DeDuCE dataset provides global estimates of deforestation and carbon emissions driven by agriculture and forestry from 2001–2022, covering over 180 commodities. It includes key indicators for assessing deforestation rates, risks, and mitigation strategies, aiming to support sustainable forest management and policy development

#### Motivation
Our team’s motivation to work on pressing environmental issues comes from a sense of urgency and responsibility. The LA wildfires have been a wake-up call for all of us, sparking our interest in delving deep into what’s fueling such events. One major reason is deforestation. What really draws us to this project is the chance to uncover the smaller, hidden factors behind such a massive problem. From the everyday products people consume to the hidden connections between global supply chains and deforestation, we want to understand how individual choices tie into this issue. Our aim isn’t just to analyze the data but to create solutions that are actionable by everyone : governments, companies, and individuals alike. The significance of this project lies in its potential to bridge the gap between global environmental challenges and individual responsibility. What are people eating, buying, or doing daily that contributes to such large-scale problems?


#### Related Work
We came across an article on the BBC that highlighted the connection between consumerism and climate change. It discusses how our everyday purchasing decisions, ranging from food to clothing are driving environmental degradation, especially through industries like agriculture and manufacturing. This led us to the DeDuCE article, which takes a closer look at deforestation driven by commodity consumption. Building on the insights from DeDuCE, we aim to create meaningful visuals and analysis that expand beyond their study, making this complex issue more accessible and actionable for everyone.
https://www.bbc.com/news/science-environment-56566377
https://trase.earth/insights/deduce-new-data-to-inform-action-against-commodity-driven-deforestation


#### Data
The dataset is huge, incorporating over 200k rows and 13 rows. The 13 rows are: Continent/Country group; ISO; Producer country; Year; Commodity group; Commodity; Deforestation attribution, unamortized (ha); Deforestation risk, amortized (ha); Deforestation emissions excl. peat drainage, unamortized (MtCO2); Deforestation emissions excl. peat drainage, amortized (MtCO2); Peatland drainage emissions (MtCO2); Deforestation emissions incl. peat drainage, amortized (MtCO2); Quality Index: Flagging deforestation estimates. Each row represents the deforestation attribution, risk, and emissions associated with one commodity (example: almonds) in a certain country and a given year. This data was built on the previous Pendrill et al. 2022 dataset. It is derived using a land-balance model to attribute deforestation across 135 countries in the tropics to expansion of cropland, pastures and forest plantation and the commodities produced on this land, and tracing these commodities to consumption using a two different trade models: a physical trade model and a multi-regional input-output model.


#### Questions

*How does commodity deforestation vary across different continents and countries?* <br>
Value proposition: to inform about future directions on conservation efforts to target key vulnerable regions. Another value for the audience is informing us (consumers of food products) on how to identify less impactful products.
Workflow: High-level visualizations on the patterns of deforestation attribution across different continents and countries.<br>
*What are some commodities that are really bad for the environment?* <br>
Value proposition: inform consumers about the environmental impact of their food choices and urge them to make better decisions through data. <br>
Workflow: Explore visual tools to demonstrate the high-deforestation-impact commodities and provide a "grocery guide" for consumers. Map the deforestation attribution of specific commodity with their global production to see if different sources of the same commodity could differ significantly in their environmental impacts. <br>
*How is the deforestation risk of agricultural and forestry commodities varying throughout time? What are some interesting patterns and trends with time that could be explained by political or economic situations.* <br>
Value proposition: Have a better understand the data and potentially draw correlation between social events and policies with deforestation attribution. <br>
Workflow: slicing the data into different years and comparing year-to-year changes in deforestation attribution and risk across different commodities and countries. <br>

#### Possible Findings/Implications

Overall commodities in developing countries are likely to have higher deforestation attributions and risks, especially in those countries near the equator (Indonesia, Brazil..)
Rice, coffee beans, and certain tropical fruits that are really popular in Western countries (example: avocado) have really high deforestation attributions. And they are more massively produced in vulnerable regions.
