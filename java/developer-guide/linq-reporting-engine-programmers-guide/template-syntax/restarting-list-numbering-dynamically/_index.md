---
title: Restarting List Numbering Dynamically
type: docs
weight: 110
url: /java/restarting-list-numbering-dynamically/
---

You can restart list numbering within your documents dynamically using restartNum tags. In particular, this feature is useful when working with a nested numbered list within a data band as shown in the following example.

Assume that you have the Order and Service classes defined in your application as follows.

**public class Order
{
`    `public String  REF getClientName getClientName()  REF getterBody { ... }
`    `public String  REF getClientAddress getClientAddress()  REF getterBody { ... }
`    `public  REF enumeration Iterable<Service>  REF getServices getServices()  REF getterBody { ... }**

`    `**...
}**

**public class Service
{
`    `public String  REF getName getName()  REF getterBody { ... }**

`    `**...
}**

Given that orders is an enumeration of Order instances, you could try to use the following template to output information on several orders in one document.

**<<foreach [order in orders]>><<[order. REF getClientName getClientName()]>> (<<[order. REF getClientAddress getClientAddress()]>>)**

1. **<<foreach [service in order. REF getServices getServices()]>><<[service. REF getName getName()]>>**

**<</foreach>><</foreach>>**

But then, a result document would look as follows.

**Jane Doe (445 Mount Eden Road Mount Eden Auckland 1024)**

1. **Regular Cleaning**
1. **Oven Cleaning**

**John Smith (43 Vogel Street Roslyn Palmerston North 4414)**

3. **Regular Cleaning**
3. **Oven Cleaning**
3. **Carpet Cleaning**

That is, there would be a single numbered list across all orders, which is not applicable for this scenario. However, you can make list numbering to restart for every order by putting a restartNum tag into your template before a corresponding foreach tag as follows.

**<<foreach [order in orders]>><<[order. REF getClientName getClientName()]>> (<<[order. REF getClientAddress getClientAddress()]>>)**

1. **<<restartNum>><<foreach [service in order. REF getServices getServices()]>><<[service. REF getName getName()]>>**

**<</foreach>><</foreach>>**

` `REF note **Note –** When using with a data band, it is required to put a restartNum tag before a corresponding foreach tag in the same numbered paragraph.

Then, a result document looks as follows.

**Jane Doe (445 Mount Eden Road Mount Eden Auckland 1024)**

1. **Regular Cleaning**
1. **Oven Cleaning**

**John Smith (43 Vogel Street Roslyn Palmerston North 4414)**

1. **Regular Cleaning**
1. **Oven Cleaning**
1. **Carpet Cleaning**

` `REF note **Note –** You can use a restartNum tag without a data band to dynamically restart list numbering for a containing paragraph, if needed; for example, the tag can be used to restart list numbering for a document inserted dynamically (see “ REF insertDoc Inserting Documents Dynamically” for more information).
