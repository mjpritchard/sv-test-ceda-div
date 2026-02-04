---
title: Easter updates for CEDA and JASMIN users
date: 2025-04-14 16:00:00
tags: ['news', 'ceda', 'jasmin']
thumbnail: 
icon: fas egg text-success
---

Please note the following updates for your attention:

- **CEDA and JASMIN support over the Easter period**
- **Scheduled maintenance affecting SSD storage Tues 22 April**
- **JASMIN regular scheduled maintenance Tues 29 April**
- **Changes to scheduler policies for `standard` and `highres` partitions**

1. Over the Easter period, CEDA and JASMIN services will be running at risk. Due to public holidays, our helpdesks will be closed at the end of working hours on Thursday 17th April until the morning of Tuesday 22nd April. Staff leave during the school holiday period also affects our availability at this time.

2. Scheduled maintenance is planned for **Tuesday 22 April 2025** to apply software upgrades to solid-state storage (SSD) systems. SSD storage is at-risk for the afternoon with disruption possible though unlikely but would have wide-reaching impact, affecting user home directories `/work/scratch-nopw2` and GWS 'SMF' volumes with paths `/gws/smf/*`.

3. As previously announced, scheduled maintenance is also planned for **Tuesday 29 April 2025**, which will cause some disruption to all JASMIN and CEDA services. Systems will be at risk and may be unavailable for all or part of the day. Other system work is also scheduled for this date in order to minimise disruption.
The LOTUS2 batch processing clusters will be unavailable for the duration of work on the day. To avoid running jobs being adversely affected, a reservation will start at 05:00 on the day, so any job submitted before that with a run time that goes over the reservation period will not start until after the reservation has finished.

4. There will be changes to the scheduler policies for the `standard` and `highres` partitions on **Tuesday 29 April**.  Read below for advice on how to mitigate impacts
For high memory and high core jobs up to 1TB and 96 cores per job, respectively, please use the new `--qos=high` with the standard partition.  See the limits below:

- QoS: high
- mem-per-job-max: 1TB
- cpu-per-job-max: 96
- total-mem-per-user: 2.5 TB
- total-cpu-per-user: 288 cores
- maxtime: 48 hours

The `highres` partition will be closed - any job in pending or running state on the "highres" partition will progress until completion. 

Please continue to check the {{<link "ceda_status">}}status page{{</link>}} for details on particular issues.

Thank you for your attention and best wishes from the CEDA and JASMIN teams.
