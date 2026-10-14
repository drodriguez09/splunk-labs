# Splunk labs

Hands-on practice with Splunk as I prepare for the **Splunk Core Certified User** exam, while building out my SOC analyst skills. Everything here was built in my home lab!

**Status:** In progress

## What's in this repo

- `01-setup/` - How I installed Splunk and loaded it with training data
- `02-search-practice/` - SPL searches which includes: what I predicted, what actually happened, and what I learned
- `03-investigation/` - *Coming soon:* a security investigation write-up

## Skills I'm practicing

- Writing SPL (Search Processing Language) searches to analyze log data
- Using fields like `host`, `source`, `sourcetype`, and `status` to narrow down search results
- Using **Transforming** commands: `stats`, `top`, `rare`
- Building reports, dashboards, and alerts

## Lessons learned

- **"All time" vs. "All time (real-time)": ** After I loaded my training data, I was exploring Splunk and re-clicked the search button. This cleared out my data that had populated. To get it back I had to tell Splunk to look at the "All time" option so that it could look at historical data since the data I was working had an older timestamp. One mishap that occurred was that I had first chosen the "All time (real-time)" option which did not populate anything since that only shows new incoming events. 

## About me

Technical trainer moving into SOC analyst work. ComptTIA Security+ certified. 
See my [GitHub Profile](https://github.com/drodriguez09) for more. 
