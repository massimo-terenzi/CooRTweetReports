# CooRTweetReports

**CooRTweetReports** is a browser-based tool to analyze coordinated social media activity using OpenAI’s GPT models.  
It works in combination with two R packages:

- [`CooRTweet`](https://github.com/nicolarighetti/CooRTweet) — for detecting coordinated behavior across platforms.  
- [`coortweetpost`](https://github.com/massimo-terenzi/coortweetpost) — for post-processing network outputs into summary tables.

👉 **Try it directly in your browser (no installation needed):**  
[https://massimo-terenzi.github.io/CooRTweetReports/](https://massimo-terenzi.github.io/CooRTweetReports/)

---

## 🔍 What it does

This tool takes in:

- `coordinated_communities.csv`  
- `coordinated_objects_by_community.csv`

…and allows you to:

1. Filter the most relevant communities by number of unique objects and vertices.  
2. Sample and preview the shared texts (`object_id`) per community.  
3. Generate a structured narrative analysis using OpenAI’s GPT (via your API key).  
4. Export a complete **Word (.doc)** report with an optional **Executive Summary**.  
5. View results interactively in the browser, with progress indicators and stop controls.

---

## 🧪 Example workflow

1. Run your coordination detection pipeline with `CooRTweet`.  
2. Post-process the results with [`coortweetpost`](https://github.com/massimo-terenzi/coortweetpost) in R:

   ```r
   export_all_results(coordinated_groups, network_graph)
