---
title: "Apex"
metaTitle: "Apex"
metaDescription: "Apex"
---

## Apex Programming

- Apex is a programming language that uses Java-like syntax and acts like database stored procedures. Apex enables developers to add business logic to system vents, such as button clicks, updates of related records, and custom pages. Apex is:
  - **Hosted**: Apex is saved, compiled, and executed on the server - the Lighting Platform
  - **Object Oriented**: Apex supports classes, interfaces, and inheritance
  - **Strongly typed**: Apex validates references to objects
  - **Multi-tenant Aware**: Because Apex runs in a multi-tenant platform, it guards closely against runaway code by enforcing limits, which prevent code from monopolizing shared resources
  - **Integrated With The Database**: It is straightforward to access and manipulate records. Apx provides direct access to records and their fields, and provides statement and query languages to manipulate those records
  - **Data Focused**
  - **Easy To Use**
  - **Easy To Test**
  - **Versioned**: Salesforce has 3 major releases everywhere, Summer, Winter, Spring. Adds new features. This can be thought of as an API (interface), that you can use
  - **Case-Insensitive Language**

## How Does Apex Work?

1. Developer User
   1. -> Un-compiled Apex Class Or Trigger
   2. <- Compiler Errors
   3. <-> Internet
2. Internet,
   1. Application Server
      1. <-> Apex Compiler
      2. <-> Apex Runtime
      3. -> Compiled Apex
      4. <-> Compiled Apex
   2. Data Storage,
      1. Apex Class
3. End User,
   1. -> Request
   2. <- Response

## Understanding Apex Core Concepts

- Version Settings
- Variables & Expressions
- All statements end with a semi-colon
- Primitive data type arguments are passed into methods by value
- Non-primitive data type arguments are passed into methods by reference

## Using Statements

A statement is any coded instruction that performs an action. In Apex, statements can be one of the following types.

## Data Types

- **Primitive**: such as Integer, Double, Long, Date, Datetime, String, ID, Boolean, among others
- **sObject**: either as a generic sObject or as a specific sObject, such as an Account, Contact, or MyCustomObject__c
- **Collection**,
  - List (or array)
  - Set
  - Map
- **Typed List Of Values**
- **User-Defined Apex Classes**
- **System-Supplied Apex Classes**
- **Blob**: Binary data in form of a string
- **Boolean**: A value that can only be assigned true, false, or null. For example, "Boolean isWinner = true"
- **Date**: A value that indicates a particular day. Unlike datetime values, Date values contain no information about time
- **Datetime**: A value that indicates a particular day and time, such as a timestamp
- **Decimal**: A number that includes a decimal point. A decimal is an arbitrary precision number. Currency fields are automatically assigned the type Decimal in Apex
- **Double**: A 64-bit number that includes a decimal point
- ID: Any valid 18-character Lightning Platform record identifier
- **Integer**:
- **Long**:
- **String**:
- **Time**:

## Apex Primitive Data Types

**Object**: Data types (such as integer), user-defined custom classes, the sObject generic type, or an sObject specific type (such as Account). All Apex data types inherit from Object.

Object -> Primitive, sObject, user-defined types, and built-in Apex types

In programming, a collection represents a set of similar data type items as s single unit. These units are used for grouping and managing related objects

Collections are designed to group certain objects with a logical connection. For example, a StudentCollection object may be used to maintain university student details

## When Should You Use Apex?

Use Apex if you want to,

- Create Web Services
- Create Email Services
- Perform complex validation over multiple objects
- Create complex business processes that are not supported by point and click automation
- Create custom transactional logic (logic that occurs over the entire transaction, not just wit a single record or object)
- Attach custom logic to another operation, such as saving a record, so that it occurs whenever the operation is executed, regardless of whether it originates in the user interface, a Visualforce page, or from SOAP API
