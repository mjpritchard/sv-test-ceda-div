---
title: "JASMIN updates: new cluster, scratch quotas, anaconda defaults removal"
date: 2025-01-28 15:00:00+00:00
tags: ['news', 'jasmin']
thumbnail: 
icon: fas triangle-exclamation text-warning
---


In this update:

- [New LOTUS2 cluster now available - please use it!](#new-lotus2-cluster-now-available---please-use-it)
- [Scratch quotas now in force - please clean up!](#scratch-quotas-now-in-force---please-clean-up)
- [Anaconda defaults removal - please check if this affects you!](#anaconda-defaults-removal---please-check-if-this-affects-you)
- [Reboots and changes to physical sci servers](#reboots-and-changes-to-physical-sci-servers)

Details:

## New LOTUS2 cluster now available - please use it!

A reminder that the new 55,000-core LOTUS2 cluster is now available for use. Please now move your processing to this cluster.

As hosts are retired from the old cluster, it is now **expected** that jobs will take longer to complete, so please do not report this as an issue in itself. The old cluster will be retired on 18 February 2025. Please see also [Reboots and changes to physical sci servers](#reboots-and-changes-to-physical-sci-servers), below.

{{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/rocky9-migration-2024/#new-lotus2-cluster-initial-submission-guide">}}Initial documentation{{</link>}} about how to submit jobs to the new cluster is provided, with more to follow in due course.

Please make sure you have read the [previous announcement](2025-01-15-jasmin-updates-new-cluster-and-maintenance-day) including the timetable for retirement of the old cluster.

## Scratch quotas now in force - please clean up!

In order to mitigate issues of scratch volumes filling up and impacting performance, quotas of **100TB per user** are now in place. `/work/scratch-pw3` is still very full so **ALL** users who have data there should take action to move data away before further writes are disabled, and before automated deletion tasks remove data for you.

Do not leave data in scratch volumes for extended time periods after your job(s) have finished: it is transient storage only.

## Anaconda defaults removal - please check if this affects you!

As per our [previous announcement](#), we no longer allow software from the Anaconda ‘defaults’ channel on JASMIN.
While we have removed this software from environments which we provide for you, in order to help you avoid any liability YOU may face for unlicensed use of this software, in environments you may have created for yourself, we have tried to detect these for you and provide instructions as to how to remove them. Where we have been able to detect environments which use the Anaconda defaults channel, we have placed a file in the each user's JASMIN home directory, named `README.anaconda_defaults_usage_<username>.txt`, containing a list of the affected files.

**If this file appears for you**, please (ASAP) {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/conda-removal/" >}}follow these instructions{{</link>}} to remove the files in the list.

## Reboots and changes to physical sci servers

A change to the timetable for switchover between clusters for the physical sci servers:

`sci-ph-02` will now be switched over for job submissions to the new cluster LOTUS2 straight after shutdown/reboot tomorrow Wednesday 29th January from 06:00 (downtime of 1-2 hours expected).

`sci-ph-01` will now be switched over for job submissions to the new cluster LOTUS2 straight after shutdown/reboot on Monday, 3rd February, from 06:00 (downtime of 1-2 hours expected).

Thank you for your attention and in advance for your cooperation.

With apologies for any inconvenience caused,

**JASMIN Team**
