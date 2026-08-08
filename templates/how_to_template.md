Tasket

# Tracks | **How-to guide**

**V 1.0 | 08.08.2026**

---

> **Note:** This guide is based on a working-draft specification of Tracks and will be updated once the specification is final.

---

## Before you begin

This guide gives you the exact steps for common jobs in **Tracks**, the Tasket capability that lets one task run across several parallel workstreams at once. Each task below is self-contained, so jump straight to the one you need.

> **Note:** In this guide, *In Progress*, *Done*, and *Not started* refer to a task's status **on a single track**. They are separate from the task's own status (Open, Completed, or Discarded).

## Prerequisites

Before you begin any task in this guide, make sure the following are in place:

| Requirement | Details |
|---|---|
| **Project access** | You are a **member, admin, or guest** on the project you want to work in. Guests have the same track permissions as members on projects they can access. |
| **Tracks enabled** | The project has a **Tracks** tab. If it does not, complete [Turn on Tracks for a project](#turn-on-tracks-for-a-project) first. |
| **Task access** | You have access to the specific task you want to start, move, or update across tracks. |
| **Admin rights** *(for turning Tracks off)* | Only an **Admin** can switch the Tracks capability off. All other tasks in this guide can be done by any team member with access. |
| **Network connection** *(for setup actions)* | Switching the capability on or off and creating, renaming, moving, or deleting tracks are **online only**. Start, Mark Done, and Mark Pending also work offline. |

---

## Turn on Tracks for a project

Switch the capability on to add the **Tracks** tab and start organizing work into lanes.

To turn on Tracks:

1. Open the project you want to use Tracks in.
2. Open the project **Settings**.
3. Switch the **Tracks** capability on.

The project gains a **Tracks** tab alongside its **Open**, **Closed**, and **Settings** tabs. Any team member can turn Tracks on.

---

## Create a track

Add a track for each workstream your task moves through, such as *Spec*, *Design*, or *QA*.

To create a track:

1. Open the **Tracks** tab.
2. Select **Add track**. This option appears at the end of the board and between any two existing tracks.
3. Enter a name for the track.
4. Confirm to add the track to the board.

The new track appears as a column, split into an **In Progress** section and a **Done** section.

> **Note:** Two tracks in the same project cannot share the same name. Tracks are also project-scoped, so a track you create here does not appear in any other project.

---

## Rename a track

Update a track's label without affecting any task on it.

To rename a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Rename**.
3. Enter the new name and confirm.

The label updates on the board column and in the Tracks pill. Every status and task assignment on the track stays exactly as it was.

---

## Move a track

Reorder the columns so the board matches the flow of your work.

To move a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Move track**.
3. Choose the position where you want the track to sit.

The column moves to its new position. Nothing else changes — no task or status is affected.

---

## Delete a track

Remove a track you no longer need.

To delete a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Delete**.
3. Confirm the deletion.

> **Warning:** Deleting a track is permanent. It removes the track's statuses and task assignments everywhere – on open **and** closed tasks alike. There is no undo and no recovery window. Delete only when you are certain the track is no longer needed.

---

## Start a task on one or more tracks

Place an open task on the tracks where its work needs to happen so each discipline can see it in their own column.

To start a task on a track:

1. Open the task you want to start.
2. Select the **Tracks** pill.
3. For each track you want the task to appear on, select **Start**.

The task moves to **In Progress** on each selected track and appears in the matching board columns.

> **Note:** Keep these limits in mind:
> - You can only start an **open** task. To start a closed task on a new track, reopen it first.
> - Starting a task on a track it is already on simply highlights its existing placement.

---

## Start several tasks across tracks at once

Move a batch of work to the next stage in a single action — for example, sending everything that finished *Design* into *Engineering*.

To start multiple tasks across tracks:

1. On the **Tracks** tab, go to the column that holds the tasks you want to move.
2. Select **Select** on each task you want to include.
3. Choose the other track or tracks to start the selected tasks on.
4. Confirm to start them.

Each selected task starts on the chosen tracks and appears in those columns.

> **Note:** If a selected task is already on a target track, it stays where it is and is not duplicated.

---

## Mark a task as Done on a track

Show that the work for one track is finished, without affecting the task's other tracks.

You can do this from the board or from the task.

**From the board:**

1. Open the **Tracks** tab and find the task in the track's **In Progress** section.
2. Select **Mark Done**.

**From the task:**

1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Mark Done**.

The task moves to the track's **Done** section, and the column counter updates. Marking a task Done on one track has no effect on any other track.

> **Note:** A task already marked **Done** cannot be stopped. If you need to remove it from the track, first select **Mark Pending**, then **Stop**.

---

## Move a task back to In Progress

Reopen work on a track after it was marked Done.

You can do this from the board or from the task.

**From the board:**

1. Open the **Tracks** tab and find the task in the track's **Done** section.
2. Select **Mark Pending**.

**From the task:**

1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Mark Pending**.

The task returns to the track's **In Progress** section, and the column counter updates.

---

## Stop a task on a track

Remove a task from a track when it no longer belongs there.

You can do this from the board or from the task.

**From the board:**

1. Open the **Tracks** tab and find the task in the track's **In Progress** section.
2. Select **Stop**.

**From the task:**

1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Stop**.

The task leaves the track's column, and its status on that track returns to **Not started**. Its status on every other track is unchanged.

> **Note:** You can only stop a task that is **In Progress** on the track. If the task is Done, select **Mark Pending** first.

---

## Check a task's status across all tracks

See every track a single task sits on, and where it stands on each, in one place.

To review a task from the Tracks pill:

1. Open the task from anywhere it appears – for example, the **My Work** tab or the **Updates** tab.
2. Select the **Tracks** pill.

The pill lists every track in the project with the task's status inline — **Not started**, **In Progress**, or **Done** — and shows how many tracks are Done out of all available tracks. From here you can also **Start**, **Mark Done**, **Stop**, or **Mark Pending** on any track directly.

> **Note:** The pill is the only place you can see a task's full track picture in a single view. If Tracks is switched off for the project, the pill does not appear.

---

## Read the board at a glance

Use the board when you want to see one project's whole flow rather than a single task.

Keep these points in mind as you read a column:

- **One column per track.** A task started on three tracks appears in three columns at once.
- **Two sections per column.** Each column has an **In Progress** section and a **Done** section.
- **Open tasks only.** Completed or discarded tasks do not appear on the board. Reopen a task to bring it back into its columns exactly as it was.
- **The header counter.** Each column header shows **X out of Y** — the number of tasks marked **Done** (X) out of all the open tasks on that track (Y) — so you can gauge progress at a glance.

To inspect a task, select it in any column to open a view where you can check its assignees, watchers, comments, and any attached Studio documents or Friday chats.

---

## Work with Tracks offline

Keep moving work forward in no-network zones. Some Tracks actions are available offline and sync when you reconnect.

**Available offline:**

- **Start** a task on a track.
- **Mark Done** a task on a track.
- **Mark Pending** a task on a track.

Your changes are queued locally and reconciled automatically when you reconnect.

**Requires a connection (online only):**

- Switching the Tracks capability on or off.
- Creating, renaming, moving, or deleting tracks.

> **Note:** If two people change the same task on the same track while offline, the change that syncs **last** is the one that is kept once everyone reconnects. If a track was deleted online while you were offline, any queued change for that track is dropped on sync and the track is not recreated.

---

## Turn off Tracks for a project

Hide the Tracks board and pill for a project when the team no longer needs them, without losing any data.

To turn off Tracks:

1. Open the project **Settings**.
2. Switch the **Tracks** capability off.

The **Tracks** tab and the pill are hidden across the project.

> **Important:** Only an **Admin** can turn Tracks off. Switching Tracks off is a hide, not a delete – every track, task assignment, and per-track status is preserved. Switch Tracks back on and the board returns exactly as it was.

---

## Related resources

- **Tracks feature guide** – a first-time overview of what Tracks is and why teams use it.
- **Tracks release note** – a summary of what changed in the latest update.

---

## Revision history

**Owner: Technical Writer**
**Review cadence: Quarterly**

| Version | Date | Updates | Responsible party |
|---|---|---|---|
| 1.0 | 08.08.2026 | Published (initial release) | Chandra Prakash J Patel |

---

© 2026 Neo Work OS. Confidential and Proprietary.

---
