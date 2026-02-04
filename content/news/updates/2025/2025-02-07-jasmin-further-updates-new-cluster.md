---
title: "JASMIN: further updates about new cluster and notebooks service"
date: 2025-02-07 14:00:00+00:00
tags: ['news', 'jasmin']
thumbnail: 
icon: fas server text-info
---


In this update:

- [Further news and important dates regarding migration to the new cluster, LOTUS2](#lotus2-migration)
- [NEW: JASMIN notebooks service now supports GPUs](#using-gpus-with-the-jasmin-notebooks-service)

Please note the following updates as part of our {{<link "https://help.jasmin.ac.uk/docs/software-on-jasmin/rocky9-migration-2024/">}}current migration{{</link>}}, which includes the retirement of the old CentOS7 cluster, LOTUS, with the new Rocky 9 cluster, LOTUS2:

## LOTUS2 migration

1. All physical sci machines `sci-ph-NN` now submit jobs to the new cluster, LOTUS2.
2. The cron server, `cron-01` will be switched over to submit to LOTUS2 on **Thursday 13th Feb at 08:00**. A downtime between 08:00-10:00 is planned to allow users to update/adapt their batch job scripts to the new Slurm scheduler on LOTUS2.
3. The new cylc server, `cylc2`  (Rocky9, running cylc v8) is ready to use with LOTUS2.  The old server `cylc1` will be retired soon. Further notes on JULES/CYCL2 cylc8 version will be added to the document linked above.
4. All virtual sci machines `sci-vm-NN` will switch over to LOTUS2 on Tuesday 18th February.
5. All standard partitions on the old cluster, LOTUS, will close on Tuesday 18th February.
6. The `long-serial` and `high-mem` partitions are already closed.
7. All Intel nodes are now retired (no Intel hardware features in LOTUS2).
8. The updated usage policy with max 100TB per user on the `scratch-pw*` disks, is now in place.
9. Measures to monitor and prevent excessive resource usage on the sci machines are now in place, to improve system stability.
10. ORCHID users should look out for further information which will be sent to them directly.

## Using GPUs with the JASMIN Notebooks service

It's now possible to se GPUs with the the JASMIN Notebooks service: {{<link "https://help.jasmin.ac.uk/docs/interactive-computing/jasmin-notebooks-service-with-gpus/" >}}find out more here{{</link>}}.

Thanks in advance for your cooperation,

**JASMIN Team**
