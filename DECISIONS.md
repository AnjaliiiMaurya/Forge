## My log

* `[11:20]` Suggested anchors were null in recommendations -> generated anchors from page titles and H1 values.
* `[12:05]` Cluster names were showing null values -> used top cluster keywords as fallback names.
* `[12:40]` Recommendation quality was poor due to archive pages -> filtered `/author/`, `/tag/`, and pagination URLs.
* `[13:10]` Weak recommendations were appearing -> added a minimum relatedness threshold.
* `[13:45]` Dashboard showed 0 entities -> used deterministic page keyword data as fallback when model entities were unavailable.
