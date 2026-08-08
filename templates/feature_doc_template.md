Tasket

# Tracks | **Feature guide**

**V 1.0 | 08.08.2026**

---

## Key contact information

| Role | Owner | Contact |
|------|-------|---------|
| **Capability owner** | Product Manager, Tracks | product@neo.work |
| **Document owner** | Technical Writer | docs@neo.work |

---

## Contents

- [About this guide](#about-this-guide)
  - [Purpose](#purpose)
  - [Audience](#audience)
  - [Conventions](#conventions)
- [Introduction](#introduction)
- [What is Tracks?](#what-is-tracks)
  - [Why teams use Tracks](#why-teams-use-tracks)
- [Key terms](#key-terms)
  - [The three track statuses](#the-three-track-statuses)
- [Turning Tracks on for a project](#turning-tracks-on-for-a-project)
- [Finding your way around the Tracks board](#finding-your-way-around-the-tracks-board)
  - [What you can do from a column](#what-you-can-do-from-a-column)
- [Tracks pill](#tracks-pill)
- [What to expect as you work](#what-to-expect-as-you-work)
  - [Using Tracks offline](#using-tracks-offline)
- [Who can do what](#who-can-do-what)

---

## About this guide

### Purpose

The purpose of this document is to introduce **Tracks**, the Tasket capability that lets a single task run across several parallel workstreams at the same time. It explains what Tracks is, why it exists, and how to find your way around it, so that a first-time user can build an accurate mental model of the feature before putting it to work.

### Audience

This document is intended for **anyone using Tracks for the first time** or anyone who wants to understand how a task can move through several workstreams at once inside Tasket.

### Conventions

The following callouts and formatting are used in this document to highlight specific types of information.

**Table 1: Callout conventions**

| Convention | Meaning |
|------------|---------|
| **Note** | A note provides helpful user information or a reference to related material. |
| **Important** | An important statement provides information essential to completing a task or understanding a concept. |
| **Warning** | A warning provides information to help you avoid irreversible loss of data or other significant impact. |

**Table 2: Text conventions**

| Convention | Meaning |
|------------|---------|
| **Bold** | Tab, button, field, and action names in text (for example, the **Tracks** tab, the **Mark Done** action). |
| *Italic* | Terms being introduced or emphasized. |

---

## Introduction

In Tasket, a **task** is a single unit of work that belongs to exactly one project. Most real work, though, does not happen in a single step. A task usually passes through more than one workstream before it is finished.

Take a sign-in redesign. It needs a spec, then design, then engineering, then QA, and finally documentation. Each of those is a separate stage, often owned by a different person, and the task moves through all of them.

Traditionally, a task can only carry one status at a time, which forces these parallel stages into a single line. **Tracks** removes that limit. It lets one task sit in several lanes at once, with each lane keeping its own status for that task, so every discipline can see and update its own part of the work independently.

> **Important:** This guide is based a working-draft specification of Tracks, and this document will be updated once the specifications are final.

---

## What is Tracks?

Tracks lets one task sit in several **track** lanes at once, and each lane keeps its own status for that task. So the same sign-in task can be in *spec* and in *design* at the same time, with each discipline seeing it in their own lane.

> **Note:** A track is a workstream, shown as a lane. A single task can live on many tracks at once, and it holds a separate status on each track it is on.

> **Important:** Finishing the task itself — marking it Completed or Discarded is independent of what is happening on any of its tracks.

### Why teams use Tracks

- **One task, many disciplines.** Instead of forcing a task through one linear status, each discipline sees the task in its own lane and updates only its part.
- **Parallel progress.** A single task can be In Progress in engineering while already Done in design, so nothing gets blocked waiting on a single shared status.
- **Shared visibility.** One glance at the board tells you how far a task has moved across every workstream.

---

## Key terms

Before you open Tracks, it helps to know four terms. They appear throughout the feature.

| Term | What it means |
|------|---------------|
| **Track** | A workstream, shown as a lane (a column) on the Tracks board. Tracks belong to a single project. |
| **Track status** | Where a task stands on one particular track. It is always one of: Not started, In Progress, or Done. |
| **The board** | The **Tracks** tab. It shows one column per track, so you can see the whole project's flow at a glance. |
| **The Tracks pill** | A control on a task that shows, in one place, every track the task is on and its status on each. |

### The three track statuses

On any given track, a task is always in exactly one of these states:

- **Not started** – The task has not been placed on this track yet.
- **In Progress** – The task has been started on this track and work is happening.
- **Done** – The work for this track is finished. You can always move it back to In Progress with **Mark Pending**.

> **Note:** Because each track carries its own status, marking a task **Done** on one track has no effect on any other track it is on.

---

## Turning Tracks on for a project

Tracks is a capability you switch on per project. Until it is enabled, the project does not show a Tracks tab.

1. **Go to your project.** Open the project you want to use Tracks in.
2. **Enable Tracks.** Any team member can switch the Tracks capability on for a project.
3. **Find the new tab.** Once enabled, the project gains a new **Tracks** tab alongside its **Open**, **Closed**, and **Settings** tabs.

> **Note:** Any team member can turn Tracks on, but only an **Admin** can turn it off.

> **Important:** Switching Tracks off is a hide, not a delete. The Tracks tab and the pill are hidden, but no data is lost. Switching Tracks back on restores every track, every assignment, and every per-track status exactly as they were before.

---

## Finding your way around the Tracks board

Open the **Tracks** tab and you will see the board. Here is how to read it.

- **One column per track.** The board shows one column for each track in the project. A task started on three tracks appears in three columns at once.
- **Two sections per column.** Every column is split into an **In Progress** section and a **Done** section, so you can see what is active and what is finished on that track.
- **Only open tasks.** Columns show open tasks only. A task that has been Completed or Discarded is not shown on the board.
- **A counter on each header.** Each column header shows a counter in the form *"X out of Y"* — the number of tasks marked Done (X) out of all the open tasks on that track (Y), giving you a quick sense of progress.

If you open a task from a column, you get a view of that task where you can check its details — assignees, watchers, comments, and any attached Studio documents or Friday chats.

### What you can do from a column

Each task in a column offers a small set of actions, depending on where the task sits.

| Where the task is | Actions available |
|-------------------|-------------------|
| In the **In Progress** section | **Mark Done**, **Stop**, and **Select**. |
| In the **Done** section | **Mark Pending** (to move it back to In Progress) and **Select**. |

Here is what each action does:

- **Mark Done** – Moves the task to the Done section of that track.
- **Stop** – Removes the task from that track. Its status on that track returns to Not started, and it leaves the column. Other tracks are unaffected.
- **Mark Pending** – Moves a Done task back into the In Progress section of that track.
- **Select** – A multi-select. It lets you pick several tasks in a track and start them across other tracks in one action — handy when a batch of work moves to the next stage together.

---

## Tracks pill

The board is great for viewing one project's flow. But when you are looking at a single task, the **Tracks pill** is where its full story lives.

Track pill lets you see the whole picture at once place.

- **It travels with the task.** The pill appears on the task detail view wherever you open the task from — for example the **My Work** tab or the **Updates** tab.
- **Every track, in one list.** Opening the pill lists every track in the project with the task's status inline: Not started, In Progress, or Done.
- **A Done count.** It also shows how many tracks are Done out of all the tracks available to the task.

From the pill you can act on any track directly:

- **Start** on any track the task is Not started on.
- **Mark Done** or **Stop** on any track the task is In Progress on.
- **Mark Pending** on any track the task is Done on.

> **Important:** The pill is the only place a task's full track picture is visible in one view. The board shows one project's lanes; the pill shows one task across all of them.

---

## What to expect as you work

As you start using Tracks, these behaviours are worth knowing so nothing surprises you.

- **Closing a task keeps its tracks.** When you Complete or Discard a task, it drops out of the board columns (which only show open tasks), but its track statuses are kept. Reopen the task and it returns to its columns exactly as it was.
- **Renaming and moving are safe.** Renaming a track only changes its label on the board and in the pill; statuses and assignments stay put. Moving a track only changes the column's position; nothing else changes.
- **Guests can join in.** Guests (members from another organisation) have the same track permissions as members on projects they have access to.

> **Warning:** Deleting a track is a hard, irreversible removal of that track's statuses and assignments everywhere including – on open and closed tasks alike. There is no undo and no recovery window, so delete with care.

### Using Tracks offline

Tasket works in no-network zones, and some Tracks actions come along for the ride.

- **Works offline:** **Start**, **Mark Done**, and **Mark Pending**. Your changes are queued locally and reconciled when you reconnect.
- **Needs a connection:** Switching the capability on or off, and creating, renaming, moving, or deleting tracks. These are infrequent, project-wide changes.

> **Note:** If two people change the same task on the same track while offline, the change that syncs last is the one that is kept when everyone reconnects.

---

## Who can do what

For quick reference, here is who is allowed to perform each Tracks action.

| Action | Who can perform it |
|--------|--------------------|
| Switch the Tracks capability on | Any team member |
| Switch the Tracks capability off | Admin only |
| Create a track | Any team member |
| Rename a track | Any team member |
| Move a track | Any team member |
| Delete a track | Any team member |
| Start a task on a track | Any member with access to the task |
| Mark Done, Stop, and Mark Pending | Any member with access to the task |
| Select and start across tracks | Any member with access to the tasks selected |
| View the Tracks board | Any member with access to the project |

---

## Revision history

**Owner: Technical Writer**
**Review cadence: Quarterly**

| Version | Date | Updates | Responsible party |
|---------|------|---------|-------------------|
| 1.0 | 08.08.2026 | Published (initial release) | Chandra Prakash J Patel |

---

© 2026 Neo Work | Confidential and Proprietary.

---
