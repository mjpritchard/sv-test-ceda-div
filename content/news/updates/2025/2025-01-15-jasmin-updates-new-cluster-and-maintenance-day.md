---
title: "JASMIN updates: new cluster and maintenance day"
date: 2025-01-15 17:00:00+00:00
tags: ['news', 'jasmin']
thumbnail: 
icon: fas server text-info
---

{{<alert alert-type="danger">}}
Important updates regarding LOTUS cluster and upcoming maintenance on JASMIN
{{</alert>}}

In this update:

- [LOTUS2, JASMIN's new compute cluster: now available for testing](#new-cluster-and-new-slurm-scheduler-available-for-testing)
- [Updates regarding retirement of old LOTUS Cluster](#closure-of-lotus-standard-partitions)
- [Changes to usage policy on `pw` scratch disks](#changes-to-usage-policy-on-pw-scratch-disks)
- [Upcoming maintenance day](#quarterly-scheduled-maintenance-day)

Details:

## New cluster and new Slurm scheduler available for testing

The new batch cluster **LOTUS2**, with a new version of the Slurm workload manager, is available for testing via the job submission sci host `sci-ph-03.jasmin.ac.uk`. There is a new job accounting hierarchy for this Slurm cluster, with a **new set of partitions** and **qualities of service (QoS)** that have attributes of run-length time limits and resources.  Please consult the {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/rocky9-migration-2024/#new-lotus2-cluster-initial-submission-guide">}}initial guide{{</link>}} on how to submit a job to LOTUS2. The full documentation will be updated in due course.

## Closure of par-multi and long-serial partitions

The old LOTUS partitions `par-multi` and `long-serial` will be closed on Friday 31st January at 16:00. The equivalent resources on LOTUS2 are accessible via:

- new partition `highres` and QoS `highres`
- new partition `standard` and QoS `long`

## Switchover of physical `sci` machines to new cluster

Job submission hosts can only be connected with one Slurm cluster, so as part of the introduction of the new cluster, the `sci` machines need to be switched over to use the new cluster, starting with the **physical** `sci` machines.

~This will happen on **Thursday 30th January**. Access to `sci-ph-0[1,2].jasmin.ac.uk` will be disabled from 09:00 while the switchover takes place: a downtime of 2 hours is expected. When these machines come back up, they will only be able to submit to the **new** (LOTUS2) cluster.~

Updated 28 Jan:

- `sci-ph-02` will now be switched over for job submissions to the new cluster LOTUS2 straight after shutdown/reboot on Wednesday 29th January from 06:00 (downtime of 1-2 hours expected).
- `sci-ph-01` will now be switched over for job submissions to the new cluster LOTUS2 straight after shutdown/reboot on Monday, 3rd February, from 06:00 (downtime of 1-2 hours expected).

A further switchover of the **virtual** sci machines will be announced in due course.

## Closure of LOTUS standard partitions

All LOTUS standard partitions (queues) will be closed on **Tuesday 18th February at 16:00**: job submissions to these will be rejected but any pending or running jobs will proceed until completion. The equivalent resources on LOTUS2 are as follows:

- for "short-serial-4hr" jobs, use partition `standard` and QoS `short`
- for "short-serial" jobs, use the partition `standard` and QoS `standard`
- for "high-mem", "par-single" and "par-single" jobs, use the partition `highres` and QoS `highres`
- for "test" jobs, use the partition `debug` and QoS `debug`

## Arrangements for special LOTUS partitions and migration of ORCHID GPU partition

To be announced in due course.

## Retirement of Intel nodes

Intel nodes in the old LOTUS cluster will gradually be decommissioned starting from the upcoming [scheduled maintenance day](#quarterly-scheduled-maintenance-day) on 21 Jan 2025. No Intel hardware features in the new cluster.
If you have codes in C or Fortran compiled specifically for Intel CPU architecture, these will fail to run on LOTUS2.

## Changes to usage policy on `pw` scratch disks

A per-user limit of **100TB** will be introduced on `/work/scratch-pw[2,3]` storage volumes. Please manage your disk space to avoid batch jobs from failing. Please remember to clear up after your work to free up space for other users of the platform.

## Quarterly scheduled maintenance day

As previously announced via the [status page](/status), a regular maintenance day is scheduled for
Tuesday 21st January. This potentially affects all JASMIN and CEDA Services.

The LOTUS and LOTUS2 batch processing cluster will be unavailable for the duration of the work on the day, to avoid running jobs being adversely affected. A reservation will start at 05:00 until 23:59 on the day, but any job submitted before 04:00 with a running time that goes over the reservation period will not start until after the reservation has finished.

Thank you for your attention and in advance for your cooperation.

With apologies for any inconvenience caused,

**JASMIN Team**

See also:

{{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/rocky9-migration-2024/#notes" >}}Rocky 9 migration{{</link>}}