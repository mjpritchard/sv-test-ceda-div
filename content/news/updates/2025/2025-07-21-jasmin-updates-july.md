---
title: JASMIN updates for July 2025
date: 2025-07-21 10:00:00
tags: ['news', 'jasmin']
thumbnail: 
icon: fas cloud-sun text-info
---

Please note the following updates/reminders from the JASMIN team, for your attention:

- Scheduled maintenance Tuesday 29 July **- next week**
- New releases of JASPY and JASR
- Migration of group workspaces **- now underway**
- User Conference 1 & 2 October **- save the dates!**
- Recent storage issues **-how you can help**

## Scheduled maintenance Tuesday 29 July

REMINDER: Tuesday 29 July will be a scheduled maintenance day for JASMIN.  [Previous announcement](/status).

On a roughly quarterly basis, important updates are applied to systems within the JASMIN infrastructure (which also hosts the CEDA Archive and associated services) in order to keep them up to date and secure. Servers may need to be rebooted in order for these changes to take effect, so there may be an interruption to JASMIN and CEDA services on this date.

The LOTUS batch processing cluster will be unavailable for the duration of the work on the day, to avoid running jobs being adversely affected. A reservation will start at 05:00 on the day, and any job submitted before that with a running time that goes over the reservation period will not start until after the reservation has finished.

## New releases of JASPY and JASR

New releases of Jaspy and JasR are now available on the `sci` machines and LOTUS clusster, and can be loaded using `module load jaspy/3.12/v20250704` or `module load jasr/4.4/v20250704` as appropriate. [Previous announcement]({{% ref "2025-07-16-updates-to-software-environments" %}}).

Release notes for these are at:
https://github.com/cedadev/ceda-jaspy-envs/releases/tag/jaspy3.12_v20250704

On Tuesday, the 29th of  July, JASMIN maintenance day,  we will:

- make these the default versions that are obtained using module load jaspy and module load jasr.
- update the JASMIN Notebooks service to use the new Jaspy version
- remove the following old versions from the default module setup:
  - `jaspy/3.11/v20240815`
  - `jasr/4.3/v20240815`

## Migration of group workspaces

Work is now underway to migrate group workspaces to new storage. Please read our [previous announcement]({{% ref "2025-05-30-jasmin-storage-migration" %}}) for more detail on this and how it will affect you.

Group Workspace (GWS) managers are being contacted in batches to schedule (over the coming months) the migration of their particular workspace. Please look our for further contact from your GWS manager, and help where you can by:

- using relative paths or environment variables, so that when the path changes (i.e. when the migration cutover is complete) the change is minimally disruptive to you
- cleaning up, deleting any data that is no longer needed (noting that most GWSs will need to shrink by 1/3)
- trying out the new [Near-line data store (NLDS) service](https://help.jasmin.ac.uk/docs/short-term-project-storage/nlds/) so that you can move to near-line storage any data that needs to be kept but does not need to be on disk (but please consider carefully whether data needs to be kept at all).

GWS data will be moved for you in the migration, but will reappear at a new path on the cutover date to be agreed with the GWS manager.

## User Conference 1 & 2 October

A further reminder to save the dates for our upcoming **JASMIN User Conference on 1 & 2 October 2025**.

Further details will be posted on the [JASMIN Conference 2025 page]({{% ref "jasmin-conference-2025" %}}) as they become available.

We hope to open event registration shortly: please look out for further announcements.

## Recent storage issues

When reporting issues such as `Transport endpoint not connected` or machines "hanging", **please remember to include these 2 essential items** which help the team resolve the problem.

- the affected **host name** if it's a `sci` or other host, **or Job ID if it's a LOTUS job**
- the **full path to the data** you were trying to access

If you don't include these, the team will need to ask you for them before they can investigate, so it always helps to include them up-front in your report: sometimes the fix is then very quick.

Meanwhile, additional monitoring has now been put in place to help detect issues and prevent affected LOTUS nodes from receiving further jobs while the issue is resolved on that host. We hope that this should help improve the resilience of the system while we continue to work with the storage vendor to improve stability.

The migration mentioned above will also mean that group workspaces (and eventually CEDA Archive data) will then operate from alternative storage which should not suffer from these particular issues.



Thanks for your attention and we wish you an enjoyable and relaxing summer break!

JASMIN Team
