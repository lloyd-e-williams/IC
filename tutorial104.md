---
layout: post
title:  "Tutorial 104: Monitoring"
date:   2018-02-04 19:34:21 -0500
categories: oic tutorial 
typora-copy-images-to: /images/tutorial104
---
This tutorial shows you how to monitor integrations.

From the left-side menu, choose **Monitoring**:

![Screen Shot 2018-03-05 at 11.10.47 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.10.47 PM.png)

Click on **Dashboards** to view statistics on the health of the system. 

![Screen Shot 2018-03-05 at 11.53.07 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.53.07 PM.png)

Notice that you have the option to change a drop-down menu to view the System Health and the Design-Time metrics. Go ahead and take a look at these dashboards. 

![Screen Shot 2018-03-05 at 11.55.13 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.55.13 PM.png)

![Screen Shot 2018-03-05 at 11.53.07 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.53.07 PM-0312164.png)

Click on the **Agents** to monitor the connectivity agents.

Expand the triangle next to Agent Group name (e.g. Lloyds Macbookpro Agent) to see the status of the individual agents that were previously configured.

![Screen Shot 2018-03-05 at 11.29.54 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.29.54 PM.png)

Next click on Integrations in the left-hand side menu. Find the integration that you created containing your initials. 

*Notice that you can change the time period if you are interested in viewing the status of the integrations that executed over a longer period of time.*

![Screen Shot 2018-03-05 at 11.33.07 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.33.07 PM.png)

You can click on the # for each of the status items (e.g. Received, Processed, Success, Errors). Click on the number of **Recieved**,

You will see the tracking page with a list of all the instances. 

![Screen Shot 2018-03-05 at 11.37.12 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.37.12 PM.png) 

Notice that the Person Id is shown since this was your tracking field. It is a link that will take you a picture of the integration that is high-lighted in green to show the path that the execution took at run-time.

![Screen Shot 2018-03-05 at 11.38.49 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.38.49 PM.png)

There is a menu in the top right corner which contains options for viewing all the business identifiers, errors, the audit trail and the activity stream. 

![Screen Shot 2018-03-05 at 11.41.03 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.41.03 PM.png)

Click on **View Audit Trail**. A box will appear showing you the basic activities which took place related to this integration. 

![Screen Shot 2018-03-05 at 11.42.42 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.42.42 PM.png)

Click the **Close** button. 

Click on the menu at the top again, but this time choose **View Activity Stream**. This time a different box appears that also contains triangles which can be expanded to view the payload formats.

![Screen Shot 2018-03-05 at 11.46.39 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.46.39 PM.png)

This is very useful for debugging. 

Click the menu again and choose **Business Identifiers**. You should see the values that you provided when you ran the integration, since they were both set-up as tracking fields.

![Screen Shot 2018-03-05 at 11.47.31 PM](images/tutorial104/Screen Shot 2018-03-05 at 11.47.31 PM.png)

This completes this monitoring tutorial. When you do the more complex **Orchestration** integrations, you will see the value of knowing which path each individual execution of an integration took since you will be able to supply branching logic based on the values that are being processed at run-time.