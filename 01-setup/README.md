# 🛠️ Lab Setup

How I built my Splunk home lab and loaded practice data. 

## Environment

- **Splunk:** Splunk Enterprise (free for 60 days)
- **Computer:** Windows 11 PC
- **Data:** Splunk's "Search Tutorial Dataset" (Uses the fictional company called "Buttercup Games")

## Steps

1. Downloaded and installed Splunk Enterprise. The process is easy and you just need to follow the installation wizard for the most part.
2. Opened Splunk in my browser at 'http://localhost:8000"
3. Created a new index named 'tutorial' (Settings ➡️ Indexes ➡️ New Index)
4. Uploaded 'tutorialdata.zip' (Settings ➡️ Add Data ➡️ Upload)
5. Set the host using **Regular expression on path** with '\\(.*)\/'
6. Sent the data to the 'tutorial" index


## Troubleshooting: the host problem
- **What happened:** The first upload labeled every event with the host '127.0.0.1' instead of the real server names.
- **Why:** On Windows, the "Segment in path" setting couldn't read the file path inside of the zip.
- **Fix:** I created a new index and re-uploaded using the "Regular expression on path," which pulled the correct names from the path.
- **Takeaway:** Check that your data's labels look right before you start analyzing.

## Results

- Searching 'index-tutorial' over ALL time shows all five hosts: www1, www2, www3, mailsv, and vendor_sales.
