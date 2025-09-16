---
title: "Prometheus"
ring: adopt
quadrant: platforms
tags: []
---

The tech-radar item "Prometheus" covers several things in Allegro: standard for describing metrics (largely compatible
with OpenMetrics) based on the use of names and labels requests_count{dc="dc4",scid="123",endpoint="/login"}) standard
for collecting metrics (scraping metrics from the service endpoint - usually /status/prometheus), or sending them (
so-called pushgateway) standard for querying metrics (promQL language) We use 5 applications in monitoring team, that
are compliant with this standard: prometheus (currently mainly as a scraper and a tool for generating recording_rules,
which are intermediary "metrics from metrics") vmagent (as a tool for controlling the flow of the metrics stream between
scrapers and storages - in the future also as a scraper) VictoriaMetrics (as our main metrics storage - a TSDB type
database, and as the main tool for responding to promQL queries) promxy (proxy of promQL queries, capable of merging
responses from multiple sources - e.g. clusters with different retention) cortex (as an alternative metrics storage -
currently in the testing phase at Allegro). 
