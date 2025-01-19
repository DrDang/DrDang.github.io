---
layout: page
title: RCCA - Varying Recorded On Times
description: 
img: assets/img/fakeCockpit.jpg
importance: 4
category: work
related_publications: false
---

## The Challenge
A customer reported unusual data inconsistencies across newly produced systems, where some units displayed drastically higher operational metrics than expected. The issue raised concerns about quality and reliability, requiring immediate investigation.

## My Approach
I began by analyzing how these metrics were generated and stored, examining historical test data across multiple units. Using custom database queries, I identified distinct patterns in the data, revealing clusters of discrepancies. To gain further insights, I visualized these patterns over time, uncovering that the inconsistencies stemmed from varying baselines during production.

## The Solution
By collaborating with cross-functional teams, including software and production, we traced the root cause to differences in initialization processes during system testing. While a comprehensive overhaul of the source processes was impractical, I devised and implemented a targeted software solution that standardized the baseline across all units, ensuring consistency moving forward.