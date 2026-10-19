# 🔍 Search Practice

My hands-on SPL practice using Splunk's Search Tutorial data. When conducting each search I wrote down the prediction **before** running it, then compared it to the actual generated results. 

## Search 1: Finding web errors

```spl
index=tutorial sourcetype=access_combined_wcookie status=404
```
  - **Prediction:** Only the web servers will appear, based on two clues: the sourcetype `access_combined_wcookie` is web server traffic, and `404` is a web status code, which the mail server's login records don't use.
    
- **Results:** I was correct. The results returned 690 events split among the 3 web servers: www1 (244), www3 (237), and www2 (209).
  
  ![Search 1 results showing 690 events](Status_404_search.png)
  
- **What I learned:** Combining a sourcetype field with a status code narrows the search and allows you to look for specific events. Based on the results, the even split suggests a load balancer is spreading traffic across the three web servers.  

  ![Host Field Results](status_404_host_field.png)
