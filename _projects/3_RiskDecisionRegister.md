---
layout: page
title: Governance Register
description: A local-first risk and decision management tool built for locked-down, restricted environments
img: assets/img/riskDecisionRegister.png
importance: 3
category: work
related_publications: false
---

## The Problem

Teams working in restricted or air-gapped environments — think SharePoint-only, no cloud tools, no networked backends — often have no good way to track risks and decisions in a governed, consistent way. Spreadsheets get stale, ownership gets fuzzy, and there's no easy way to link a risk to the decision that addressed it.

## The Solution

I built **Governance Register**, a local-first web app that gives teams a proper risk and decision workspace without requiring any infrastructure. It runs entirely in the browser from a static build — no server, no database, no setup required.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/riskDecisionRegister.png" title="Risk Register" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The risk register with scoring, ownership, and linked decisions.
</div>

Key features include:

- **Risk register** with probability/impact scoring, ownership, mitigation planning, linked decisions, and history tracking
- **Decision register** with rationale, linked risks, consequences, and status tracking
- **Snapshot import/export** — teams share a single JSON file via SharePoint or email; no sync service needed
- **Portable launchers** for Mac and Windows so end users can run it directly from the repo without any dev tooling
- **Bundled demo snapshot** for onboarding and training walkthroughs

## Why It's Built This Way

The portable, browser-based approach is intentional. Electron would add weight and distribution complexity; a lightweight static build opened from a `.command` or `.bat` file gets the job done with zero friction. The built app is checked into the repository so it works straight from a zip or clone.

The snapshot workflow is the key collaboration primitive — it turns a single file into a reviewable, versioned handoff between team members, which is exactly how restricted environments already work.

## Tech Stack

Built with TypeScript and React, bundled with Vite. Source lives under `app/`; the production build is committed directly to the repo for portable deployment.

[View on GitHub](https://github.com/DrDang/Risk-Decision-Register)
