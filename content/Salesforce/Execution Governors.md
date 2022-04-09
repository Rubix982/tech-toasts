---
title: "Execution Governors"
metaTitle: "Execution Governors"
metaDescription: "Execution Governors"
---

## Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Execution Governors And Limits](#execution-governors-and-limits)
- [Per Transaction Apex Limits](#per-transaction-apex-limits)
- [Static Apex Limits](#static-apex-limits)
- [Running Apex Within Governing Limits](#running-apex-within-governing-limits)
- [Best Practice For Writing Apex Code](#best-practice-for-writing-apex-code)
  - [**Bulkifying DML Calls**](#bulkifying-dml-calls)
  - [More Efficient SOQL Queries](#more-efficient-soql-queries)

## Execution Governors And Limits

- Because Apex runs in a multitenant environment, the Apex runtime engine strictly enforces limits so that runaway Apex code of processes don't monopolize shared resources
- If some Apex code exceeds a limit, the associated governor issues a runtime exception that can't be handled
- The Apex limits, or governors, track, and enforce the limits for the following categories,
  - Per-Transaction Apex Limits
  - ...

## Per Transaction Apex Limits

These limits count for each Apex transaction. For batch Apex, these limits are reset for each execution of a batch of records in this category,

1. Total number of SOQL queries issued: **100**
2. Total number of records retrieved by SOQL queries: **50,000**
3. Total number of DML statements issued: **150**
4. Total number of records processed as a result of DML statements: **10,000**
5. Total number of API call-outs in a transaction: **100**
6. Maximum cumulative timeout for all API call-outs in a transaction: **2 minutes**
7. Total heap size: **6 MB**
8. Maximum execution time for each Apex transaction: **10 minutes**

## Static Apex Limits

- Default Timeout for API call-outs in a transaction: **10 seconds**
- Maximum SOQL query run time: **2 minutes**
- Apex trigger batch size: **200 records**
- Maximum number of records returned for a Batch Apex query in Database.QueryLocator: **50 Million**

## Running Apex Within Governing Limits

- When you develop software in a multi-tenant cloud environment such as the Salesforce Lighting platform, you don't have to scale your code, because the Salesforce Lightning platform does it for you
- As discussed, because resources are shared in a multi-tenant platform, the Apex runtime engine enforces

## Best Practice For Writing Apex Code

The following are some best practics for writing code that doesn't exceed certain governor limits,

### **Bulkifying DML Calls**

Instead of,

```apex

```

We can do instead,

```apex
List<Line_Item__c> updateList = new List<Line_Item__c>();

for (Line_Item__c li : liList) {
    if (li.Units_Sold__c > 10) {
        li.Description__c = 'New description';
        updatedList.add(i);
    }
}

// Once the DML call for the entire list of line items update updatedList;
```

### More Efficient SOQL Queries

Placing SQOL queries inside for loop isn't a good practice because the SOQL query executes once for each iteration and may surpass the 100 SOQL queries limit per transaction. The following is an example that runs a SQOL query for every item in Trigger.new, which isn't efficient. An alternative example is given with a modified 

The following is a bad approach,

```apex
Trigger LimitExample on Invoice_Statement__C (before insert, before update) {
    for(Invoice_Statement__C inv : Trigger.new) {
        List<Line_Item>
        ...
    }
}
```

Recommended approach is,

```apex
trigger EnhancedLimitExample on Invoice_Statement__C (before insert, before update) {
    
}
```
