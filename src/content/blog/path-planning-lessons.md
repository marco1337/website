---
title: Lessons from Building a Warehouse Robot's Path Planner
description: What building navigation software for a fleet of autonomous robots taught me about defensive engineering.
date: 2025-11-02
---

The hardest bugs weren't in the planning algorithm — they were in the assumptions
about the world it ran in. Sensors drift, floors aren't perfectly flat, and two
robots can disagree about where they are at the exact same moment.

We ended up treating every sensor reading as provisional and building consensus
across redundant inputs rather than trusting a single source of truth. It made
the system slower to react by a few milliseconds, but far less likely to send a
robot into a wall.
