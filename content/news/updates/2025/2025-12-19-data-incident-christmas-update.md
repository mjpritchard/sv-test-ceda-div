---
title: Data Incident Christmas Update
date: 2025-12-19 10:30:00
tags: ['news', 'ceda', 'data-incident-nov25']
icon: fa-solid fa-gifts text-info

---

This is an update on the Archive data incident that occurred on 18th November 2025 - {{< link href="/tags/data-incident-nov25/" >}} see previous updates here. {{< /link >}}

We are making good progress with recovering data back into the Archive and have made significant progress. Over 1.6 Petabytes of data have been recovered to a holding area - 1.3 Petabytes of this has now been moved to its correct location in the Archive. Most of this should now be available to users - we are doing some final checks for data permissions.

## High data transfer speeds with Globus

We identified over 790TB of CMIP6 data to be available via our ongoing collaboration through the Earth System Grid Federation. We worked with the USA's {{< link href = "https://www.ornl.gov/" >}} Oak Ridge National Laboratory {{< /link >}} to transfer the data {{< link href="https://help.jasmin.ac.uk/docs/data-transfer/globus-transfers-with-jasmin/" >}} using Globus {{< /link >}} - an online data transfer service designed specifically for moving large datasets between research institutions.

Using Globus, we achieved an astonishing transfer rate of 8.1 GB per second, sustained over the 27 hours to bring over the 1.4 million files. In old-money, that's equivalent to watching an entire blue ray DVD per second!

These incredibly fast speeds were achieved by using JASMIN's Globus data transfer service which uses 5 high-performance data transfer nodes located in a special "Data Transfer Zone" of the network to optimise throughput. The specialist system architecture at each institution, enables highly parallel, "friction-free" transfers.

The transfer of this data into a holding location then allowed for checks to be computed locally on JASMIN and compared to the data catalogue records. The final movement of data to user-accessible archive locations is still in progress.

{{< image src="../../../img/news/2025/2025-12-19-incident-xmas-update/incident-globus-transfer.png" caption="The central section of this graph shows the network traffic into the five data transfer notes during the period of the CMIP6 data transfer from Oak Ridge National Laboratory to JASMIN, compared to their normal, background levels of user data transfers." >}}

A further 100+ TB of CMIP6 data has been transferred from European sites. This was available via HTTP, with an overall transfer rate of approximately 0.5 GB per second - showing a stark difference between the Globus transfer rates.

## Remaining data transfers will resume in early January

Remaining missing data is being retrieved from CEDA's own tape backups. This is an ongoing process.
Our data retrieval will also be reduced over the festive period. We will be able to share a more detailed update in the new year.

Finally, a reminder that {{< link "/2025-12-10-support-over-christmas-period.md" >}} JASMIN and CEDA support will close for the Christmas period {{< /link >}} at 16:30 on Friday 19th December 2025 and reopen on 5th January 2026. Thank you for your understanding during this time.

The CEDA and JASMIN team would like to take this opportunity to wish all our users a very Merry Christmas and a Happy New Year!
