---
title: "Object"
metaTitle: "Object"
metaDescription: "Object"
---

## What Are Objects?

## What Are Fields?

- Fields in Salesforce represents what he columns represent in relational databases. It can store data values which are required for a particular object in a record
- Every standard and custom object has fields in it. Each field has a specific data type
- Types of fields,
  - "**Standard Fields**": There are four standard fields in every custom object that are "Created By", "Last Modified", "Owner", and the "Name" (Can have repetition) field. These fields cannot be deleted. For standard objects, the fields which are present by default in them and cannot be deleted from standard objects are standard fields
  - "**Custom Fields**": The Custom fields are those field which are added by the Salesforce admin to meet the business requirements of any organization. They can be created on any standard or custom object

## Get To Know Fields

## Field Data Types

- "**Auto Number**"
- "**Formula**"
- "**Roll-Up Summary**"
- "**Lookup Relationship**"
- "**Master-Detail Relationship**"
- "**External Lookup Relationship**"
- "**Checkbox**"
- "**Currency**"
- "**Date**"
- "**Date/Time**"
- "**Email**"
- "**Geolocation**"
- "**Number**"
- "**Percent**"
- "**Phone**"
- "**Picklist**"
- "**Picklist (Multi-Select)**"
- "**Text**"
- "**Text Area**"
- "**Text Area (Rich)**"
- "**Text (Encrypted)**"
- "**Time**"
- "**URL**"

## Methodologies

There are two important points to Salesforce,

1. Sharing
2. Visibility

Not everyone can see everything.

## Lookup vs Master-Detail

1. In master-detail, detail record cannot exist without a master record
2. You create master-detail relationship when,
   1. The relation record is required on all detail records
   2. The ownership and sharing of a detail record are to be determined by the mater record
   3. When a user deletes the mater record, all detail records are to be deleted
   4. You want to create rollup summary fields on the master record to summarize the detail records
3. Typically, you use lookup relationship when objects are only related in some cases. Sometimes a contact is associated with a specific account, but sometimes it's just a contact. Objects in lookup relationship usually work as stand-alone objects

## Trigger

Apex is written for Trigger.

Salesforce Object Search Language (SOSL), Salesforce Object Query Language (SOQL).

You can select fields and on which to enable Field History Tracking.

## Flow Builder User Interface

1. **Canvas**: Just like an artist, the canvas is where you design and visualize your flow. There are two layouts available: freeform or auto-layout
   1. **Freeform** provides more flexibility on the canvas
   2. **Auto-layout** provides a more structured experience which is recommended for beginners
2. **Elements**: Under the Toolbox, you'll find Elements. These are the building blocks to create each step of your flow on the canvas. Be aware that the flow type determines which elements are available in your Toolbox. There are three main types.
3. **Manager**: Under the Toolbox, you'll also find the Manager tab. This consists of all the elements and resources found in your flow. By clicking on each resource, you can also see the relationship between them and the flow
4. **Button Bar**: Here shows all the important information

## Salesforce Flow (Hands-On)


