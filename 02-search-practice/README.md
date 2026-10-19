# 🔍 Search Practice

My hands-on SPL practice using Splunk's Search Tutorial data. When conducting each search I wrote down the prediction **before** running it, then compared it to the actual generated results. 

## Search 1: Finding web errors

```spl
index=tutorial sourcetype=access_combined_wcookie status=404
```
- **Prediction:** With this search, only the webservers will appear since we are searching for a status code of 404. This code is generally associated with web traffic.
- **Results:** I was correct. The results returned 690 events split among the 3 webservers: www1 (244), www3 (237), and www2 (209).
  
  ![Search Results:](Status_404_search.png)
  
- **What I learned:** Combining a sourcetype field with a status code narrows the search and allows you to look for specific events. Based on the results, I can also see that the load balancer for the webservers is working correctly since the traffic is split pretty evenly among the 3 webservers. 
