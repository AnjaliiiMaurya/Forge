## My log

* `[11:00]` Dashboard at localhost:7700 died immediately after run.py completed -> HTTP server runs in a daemon thread and is killed when the Python process exits -> added a blocking `while True: time.sleep(3600)` loop in `run.py main()` so the dashboard stays alive until Ctrl-C.
* `[11:20]` Suggested anchors were null in recommendations -> generated anchors from page titles and H1 values; strip brand suffixes after separator characters first.
* `[12:05]` Cluster names were showing null values -> used top 2 cluster keywords as fallback names.
* `[12:40]` Recommendation quality was poor due to archive pages -> filtered `/author/`, `/tag/`, `/page/`, and `/category/` URLs by path segment.
* `[13:10]` Weak recommendations were appearing -> added a minimum relatedness threshold of 0.10.
* `[13:45]` Dashboard showed 0 entities -> used `clusters["page_keywords"]` count as fallback in `li_entities()` when model entities are unavailable.
