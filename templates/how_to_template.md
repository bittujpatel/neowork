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
| **Project access** | You are a **member, admin, or guest** on the project you want to work in. Guests have the same track permissions as members on projects they can access.<br><br>**> Important:** Because guests inherit full member permissions, they can create, rename, and move tracks. Admins should ensure guests are aware of project workflows before granting access. |
| **Tracks enabled** | The project has a **Tracks** tab. If it does not, complete [Turn on Tracks for a project](#turn-on-tracks-for-a-project) first. |
| **Task access** | You have access to the specific task you want to start, move, or update across tracks. |
| **Admin rights** *(for deletion or turning off)* | Only an **Admin** can switch the Tracks capability off or permanently **delete a track**. All other tasks in this guide can be done by any team member with access. |

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

> **Note:** Two tracks in the same project cannot share the same name. Tracks are also project-scoped, so a track you create here does not appear in any other project.

---

## Rename a track

Update a track's label without affecting any task on it.

To rename a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Rename**.
3. Enter the new name and confirm.

---

## Move a track

Reorder the columns so the board matches the flow of your work.

To move a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Move track**.
3. Choose the position where you want the track to sit.

---

## Delete a track

Remove a track you no longer need. 

To delete a track:

1. On the **Tracks** tab, open the actions for the track's column header.
2. Select **Delete**.
3. Confirm the deletion.

> **Warning:** Only an **Admin** can delete a track. Deleting a track is permanent. It removes the track's statuses and task assignments everywhere – on open **and** closed tasks alike. There is no undo and no recovery window.

---

## Start a task on one or more tracks

Place an open task on the tracks where its work needs to happen so each discipline can see it in their own column.

To start a task on a track:

1. Open the task you want to start.
2. Select the **Tracks** pill.
3. For each track you want the task to appear on, select **Start**.

> **Note:** You can only start an **open** task. To start a closed task on a new track, reopen it first.

---

## Start several tasks across tracks at once

Move a batch of work to the next stage in a single action.

To start multiple tasks across tracks:

1. On the **Tracks** tab, go to the column that holds the tasks you want to move.
2. Select **Select** on each task you want to include.
3. Choose the other track or tracks to start the selected tasks on.
4. Confirm to start them.

> **Note:** If a selected task is already on a target track, it stays where it is and is not duplicated.

---

## Mark a task as Done on a track

Show that the work for one track is finished, without affecting the task's other tracks.

**From the board:**
1. Open the **Tracks** tab and find the task in the track's **In Progress** section.
2. Select **Mark Done**.

**From the task:**
1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Mark Done**.

> **Note:** A task already marked **Done** cannot be stopped. If you need to remove it from the track, first select **Mark Pending**, then **Stop**.

---

## Move a task back to In Progress

Reopen work on a track after it was marked Done.

**From the board:**
1. Open the **Tracks** tab and find the task in the track's **Done** section.
2. Select **Mark Pending**.

**From the task:**
1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Mark Pending**.

---

## Stop a task on a track

Remove a task from a track when it no longer belongs there.

**From the board:**
1. Open the **Tracks** tab and find the task in the track's **In Progress** section.
2. Select **Stop**.

**From the task:**
1. Open the task and select the **Tracks** pill.
2. Next to the track, select **Stop**.

The task leaves the track's column, and its status on that track returns to **Not started**. 

> **Note:** You can only stop a task that is **In Progress** on the track. If the task is Done, select **Mark Pending** first.

---

## Move a task to a different project

If you need to change the project a task belongs to, be aware of how it affects Tracks.

> **Warning:** Moving a task to a different project **permanently wipes** all its track assignments and history. Even if you immediately move the task back to the original project, it will land with no track started. 

---

## Check a task's status across all tracks

See every track a single task sits on, and where it stands on each, in one place.

To review a task from the Tracks pill:

1. Open the task from anywhere it appears (e.g., **My Work** or **Updates**).
2. Select the **Tracks** pill.

The pill lists every track in the project with the task's status inline — **Not started**, **In Progress**, or **Done**. 

---

## Turn off Tracks for a project

Hide the Tracks board and pill for a project when the team no longer needs them.

To turn off Tracks:

1. Open the project **Settings**.
2. Switch the **Tracks** capability off.

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
