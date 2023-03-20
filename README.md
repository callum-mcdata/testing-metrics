# 🥪 A Future of Testing

Welcome to this design session! Today we are going to walk through what it would be like to configure testing on top of metrics within your dbt project. For this session we are going to use the experimental spec that is being propsoed - all you need to know is that the actual `metric` contains less information than the past!

## The Excercise

You're an Analytics Engineer with the Jaffle Company. You've built out your Semantic Layer inside of dbt but a recent data quality issue led to your company mis-reporting on your key metrics. The CEO accepted responsibility but has asked you to research a way to make sure it doesn't happen again. 

You know that your `revenue` metric for January of 2023 had the following properties:
- The overall revenue was $10,000
- The revenue in the US was $6,729
- The revenue on Jan 4th was $800
- Revenue should always be greater than $100

With this information, we are going to be walking through 3 proposed designs for testing metrics. It is your responsibility to determine which of these feels the most dbtonic, which is the highest value, and to provide the team with any suggestions that you have!

### Design 1
Referencing the [first design in the Notion](https://www.notion.so/dbtlabs/DX-Collaboration-Testing-our-Metrics-2bd3b32ea6c54d46b873ca8575d8861b?pvs=4#0205f77ab44846e9b48f983a82d11120), please implement a test on the revenue metric inside of the [semantic graph file](models/semantics/semantic_graph.yml) for one (or more) of the three known properties.

A corresponding design document exists in the semantics folder for your convienence. 

### Design 2
Referencing the [second design in the Notion](https://www.notion.so/dbtlabs/DX-Collaboration-Testing-our-Metrics-2bd3b32ea6c54d46b873ca8575d8861b?pvs=4#707fc12eb66e4f8b96dc51754dd0a667), please implement a test on the revenue metric inside of the [semantic graph file](models/semantics/semantic_graph.yml) for one (or more) of the three known properties.

A corresponding design document exists in the semantics folder for your convienence. 

### Design 3
Referencing the [third design in the Notion](https://www.notion.so/dbtlabs/DX-Collaboration-Testing-our-Metrics-2bd3b32ea6c54d46b873ca8575d8861b?pvs=4#3e6d528962ce4d58a6c7a64e430c5e60), please implement a test on the revenue metric inside of the [semantic graph file](models/semantics/semantic_graph.yml) for one (or more) of the three known properties.

A corresponding design document exists in the semantics folder for your convienence. 