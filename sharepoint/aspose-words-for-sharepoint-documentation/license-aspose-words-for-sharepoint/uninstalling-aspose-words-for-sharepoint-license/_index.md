---
title: Uninstalling Aspose.Words for SharePoint License
type: docs
weight: 30
url: /sharepoint/uninstalling-aspose-words-for-sharepoint-license/
---

To uninstall the license, please use the steps below from the server console.

1. Retract the license solution from the farm:

{{< highlight java >}}

 stsadm.exe -o retractsolution -name Aspose.Words.SharePoint.License.wsp -immediate 

{{< /highlight >}}

1. Execute administrative timer jobs to complete the retraction immediately:

{{< highlight java >}}

 stsadm.exe -o execadmsvcjobs 

{{< /highlight >}}

1. Wait for the retraction to complete. You can use Central Administration to check if the retraction completed under **Central Administration**, then **Operations** and **Solution Management**.
1. Remove the solution from the SharePoint solution store:

{{< highlight java >}}

 stsadm.exe -o deletesolution -name Aspose.Words.SharePoint.License.wsp  

{{< /highlight >}}
