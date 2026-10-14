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

- **"All time" vs. "All time (real-time)":** After loading my training data, I re-ran a search and my results disappeared. The data was still there, but the time picker was looking at the wrong time window. I first picked "All time (real-time)", which still showed nothing because it only watches for new incoming events. Switching to plain "All time" brought my results back, since my data had older timestamps. **Takeaway:** when a search comes back empty, check the time range first.

## About me

Technical trainer moving into SOC analyst work. CompTIA Security+ certified. 
See my [GitHub Profile](https://github.com/drodriguez09) for more. 
