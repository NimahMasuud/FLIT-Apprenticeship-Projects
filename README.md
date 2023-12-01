# FLIT-Apprenticeship-Projects
Project1/Market Basket Analysis


 ### Overview

This project harnesses Market Basket Analysis techniques in Python to derive meaningful insights from transactional data. The primary objective is to comprehend customer buying behaviors, reveal connections between various products, and extract actionable intelligence to enhance targeted marketing strategies.

### Key Features

#### Feature Engineering

Utilizing Python, the dataset undergoes feature engineering, primarily involving the consolidation of items per customer per day into 'CustomerTransaction' baskets. 


#### Data Exploration

The exploration phase delves into understanding the dataset's structure and characteristics. Below is an example of exploring key columns:


Summary statistics for 'Member_Number', 'ItemDescription', and 'Date'


#### Apriori Algorithm

Application of the Apriori algorithm to unveil frequent itemsets that serve as the foundation for generating association rules:

from mlxtend.frequent_patterns import apriori, association_rules

# Generating frequent itemsets
frequent_itemsets = apriori(data, min_support=0.03, use_colnames=True)

# Generating association rules
rules = association_rules(frequent_itemsets, metric='lift', min_threshold=1)
 
