---
layout: page
title: RCCA Helper
description: A local-first Root Cause and Corrective Action workspace with interactive fault tree analysis, action tracking, and report generation
img: assets/img/rccaHelper.svg
importance: 4
category: work
related_publications: false
---

## Why This Exists

Most RCA tools are either too generic, too heavyweight, or too dependent on cloud infrastructure for teams working in restricted or offline environments. During investigation sessions, you need something that stays focused on the actual investigation — not on IT approvals or network connectivity.

RCCA Helper is a local-first browser app built to match how investigations actually run&#58; map causes visually, capture evidence in context, track actions against the right cause, and generate a report without ever moving data into another tool.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rccaHelper.svg" title="RCCA fault tree workspace" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Interactive D3 fault tree with status-aware nodes, action markers, and corrective-action indicators.
</div>

## Core Capabilities

- **Interactive fault tree** built with D3 — pan, zoom, recenter, and PNG export
- **Node-level investigation workflow** with Pending, Active, Ruled Out, and Confirmed statuses
- **Root-cause marking** so confirmed causes roll directly into resolution planning
- **Evidence capture** — notes and rationale attached directly to investigation nodes
- **RAIL-style action tracking** with assignees, due dates, and progress
- **Corrective action tracking** linked back to identified root causes
- **HTML report generation** for single investigations or bulk output
- **Multi-project organization** with a dashboard summary across investigations
- **JSON import/export** for project bundles and individual investigations
- **Local persistence** with optional auto-backup — no backend required
- **Light/dark theme** support

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rccaHelper_dash.svg" title="RCCA dashboard overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Dashboard view showing active investigations, status mix, root-cause coverage, and reporting progress.
</div>

## Investigation Workflow

1. Create or import a project
2. Build the fault tree during the investigation session
3. Mark causes as ruled out, active, confirmed, or explicit root causes as evidence develops
4. Attach investigation actions and corrective actions to relevant causes
5. Export JSON bundles, PNG tree views, or generated HTML reports for circulation and recordkeeping

## Running It

The built app is checked into the repository. No Node.js or npm required to run it&#58;

- **Mac** — double-click `Run RCCA Helper.command`
- **Windows** — double-click `Run RCCA Helper.bat`

These launchers start a lightweight local server for the checked-in `dist/` folder and open the app in the browser.

## Tech Stack

Built with React 19, TypeScript, Vite, D3, and Tailwind CSS 4. Runs entirely offline. Exports are plain JSON — no backend, no sync service, no cloud dependency.

[View on GitHub](https://github.com/DrDang/RCCA-Helper)
