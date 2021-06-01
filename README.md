# Kibana Visualization Example

- In this repository example of **Bar Graph** create using kibana visualization is given.
- Kibana is part of the elastic-stack(ELK stack) that provides search and data visualization capabilities for data indexed in Elasticsearch.


### Steps To Create Bar Graph In Kibana :

- There is one index named 'jobs' already created and populated with some data in the elasticsearch.
- First of all, start the kibana service and open http://localhost:5601/ on your web browser, you will get a hone page of kibana.
- To create a chart first we have to create an index pattern that will consider the indices from elasticsearch.


#### 1. Create Index Pattern

- We are going to create an index pattern `job*` that will match all the elasticsearch indices that are starting with `job`.
- Kibana will perform visualization on all the data combine with all the indices of elasticsearch that match with the pattern we have created.


![create index pattern](/src/assets/home-page.png)

![create index pattern](/src/assets/inex-pattern.png)

![create index pattern](/src/assets/create-pattern.png)

#### 2. Create New Visualization Using That Index Pattern

- We are going to create a visualization using that index pattern.

![create visulization](/src/assets/visulize.png)

![create visulization](/src/assets/select-pattern.png)

![create visulization](/src/assets/create-visulization.png)

#### 3. Create Bar Graph 

- Select the bar graph from the visualization pop-up.

![create bar graph](/src/assets/select-bar-graph.png)

- By default Y-axis will show the count of doc that hits the criteria we have set on the X-axis.
- To set criteria for separation of docs select X-axis from Buckets.

![create bar graph](/src/assets/add-x-axis.png)

- Now we want separation of docs on the basis of Post date of the job, so we will use a date histogram for that.

![create bar graph](/src/assets/select-histogram.png)

- Select the field using you want to separate docs, In our case, we are using the **job post date** field.

![create bar graph](/src/assets/select-field.png)

- Select the interval for separation.

![create bar graph](/src/assets/interval.png)

- Run The Configuration.

![craete bar graph](/src/assets/bar-graph.png)
