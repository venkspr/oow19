**# Lab3**



**# Introduction**



In this lab we will be adding some charts to the reports page and learn about the visualization capabilities of Visual Builder. We will be consuming data from a remote rest endpoint. 



**# Add a bar chart visualizing annual sales**



**##### Step 1 : Create a service connection to remote rest endpoint**



https://apex.oracle.com/pls/apex/venks/reports/yearlysales



![img](assets/image2019-8-25_15-22-13.png)



![img](assets/image2019-8-25_15-22-50.png)



**##### Step 2: Make sure that you hit the test tab and copy the response body before clicking create.**



![img](assets/image2019-8-25_15-24-19.png)



**##### Step 3: Drag and Drop a bar chart to the reports page**



![img](assets/image2019-8-25_15-26-4.png)



**##### Step 4: Click on add data and choose the service connection we just defined in step 1**



![img](assets/image2019-8-25_15-27-45.png)



Ensure that you choose all the fields. Map the Value(Y Axis) to total field, Label(X axis) to year 



![img](assets/image2019-8-25_15-29-15.png)



**##### Step 5: Now you should have a bar chart on the reports page**



![img](assets/image2019-8-25_15-30-39.png)



**##### Step 6: Set the width to 100%, so the chart takes the full width of the container**



![img](assets/image2019-8-25_16-24-41.png)





**# Add a pie chart to display total sales by category**



**##### Step 1: Drag and drop a pie chart from the components to the page**



![img](assets/image2019-8-25_16-28-32.png)



**##### Step 2: Now we will reference the service connection defined before as source of data for the pie chart**



![img](assets/image2019-8-25_16-30-16.png)



![img](assets/image2019-8-25_16-31-38.png)



**##### Step 3: Check the rendered Pie Chart**



Next we want to ensure both the chart are same width and take up 6 columns in a 12 grid layout



**##### Step 4: Change the class for both the chart to oj-md-6**



Now both the charts should be of the same width and properly aligned on the screen



![img](assets/image2019-8-25_16-37-14.png)



**# Chart options**



There are several configuration options available for the charts. You can declaratively set some of those via property palette.



Refer to the image below to see how they change the rendering of the chart.



![img](assets/chart-options.gif)



Congratulations, you have completed lab 3. [Click here to goto Lab 4](lab4)lab4)