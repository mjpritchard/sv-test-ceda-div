---
title: JASMIN Updates October 2025
date: 2025-10-21 15:00:00
tags: ['news', 'ceda', 'jasmin']
icon: fa-solid circle-info text-info
---

Please note the following updates for your attention:

- Reminder of scheduled maintenance day, Tuesday 4 November 2025
- New scratch volumes, retirement of old
- XFC service changes
- Storage migration progress

## Reminder of scheduled maintenance day, Tuesday 4 November

As previously announced via the status page, a regular maintenance day is scheduled for Tuesday 4th November. This potentially affects all JASMIN and CEDA services.

As usual, the LOTUS batch processing cluster will be unavailable for the duration of the work on the day, to avoid running jobs being adversely affected. A reservation will start at 05:00 until 23:59 on the day, but any job submitted before 04:00 with a running time that goes over the reservation period will not start until after the reservation has finished.

## New scratch volumes, retirement of old

New scratch volumes are now available, these are:

- `/work/scratch-pw4`
- `/work/scratch-pw5`

We plan to decommission the following old volumes in just over a month’s time, on Tuesday 4th December 2025:

- `/work/scratch-pw2`
- `/work/scratch-pw3`

Please begin using the new volumes now, and clear out any data from the old volumes before that date, when the volumes will initially be made read-only and then fully removed soon after (exact date TBC).

Please note that the scratch volumes are now accessible via our Globus data transfer service, to help make data transfers easier between GWS and scratch. Please remember to `chgrp` any data moved from scratch to a GWS, to appropriate `gws_<name>` group, to ensure correct ownership and permissions within the GWS.

Please also note that scratch data older than 28 days is automatically deleted, and the use of tools like `touch` to re-age the data is not permitted - users found to be abusing this will be sanctioned. Users are able to store up to a maximum of 100 TB.

## XFC service changes

We will shortly be reinstating the notifications system for the Transfer Cache (XFC) service. This means that users of the service will start receiving automatic email notifications from the system when their usage triggers alert criteria. We are doing this to help ensure that space is used efficiently for the intended purpose, i.e. very short-term cache space to support inward/outward data transfers.

As with scratch, high-performance data transfer tools like Globus are available to help move data efficiently, and the same rules apply to residence time and the use of `touch` or equivalent. This is to ensure fair usage between all users of the service.

## Storage migration progress

Hopefully you will be aware from previous notices, and via your GWS manager, of current work underway to migrate GWSs and the CEDA Archive from old to new storage hardware. Work is progressing well initially with GWSs but we soon plan to start migrating archive volumes too.

While changes to the archive will be transparent to users, changes to GWSs do mean a change in path, but you can check the path of your GWS in the accounts portal (on the same page where you would apply for access for it). GWS migrations also involve a "cutover" period for a final sync and check stage before the new volume is released for use, during which both old and new volumes are inaccessible to users, but we try to keep the length of this to a minimum. Please check with your GWS manager, with whom we will be communicating the timescale and progress of your particular workspace.

The task is large and challenging, but feedback from workspaces that have now migrated is very good, so we look forward to making further progress with this task over coming months. 

Thank you for your attention and apologies for any inconvenience caused by the work discussed.

JASMIN Team
