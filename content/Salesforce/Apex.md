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

## Developing Code In The Cloud

Apex cannot be used to,

1. **Render Elements In The User Interface**: Other than error messages
2. **Change Standard Functionality**: Apex can only prevent the functionality from happening, or add additional functionality
3. Create temporary files
4. Spawn threads

You cannot render client side components with Apex. You need to use a standard of ES6 that Salesforce provides for building client side components.

## switch Statements In Apex

1. Apex provides a switch statement that tests whether an expression matches one of several values and branches acccordingly
2. The whne value can be a single value, multiple values, or sObject types
3. The swtich statement evaluates the expression and executes the code block
4. Apex switch statements expression can be f the following types,
   1. Integer
   2. Long
   3. sObject
   4. String
   5. Enum
5. There is no fall-through

## when and when else blocks

1. VAlues ca take one of the following forms,
   1. When literal {}
   2. When sObjectType identifier {}
   3. When enum_Value {}

## sObject

sObject -> {Account, Contract, MyCustomObject}

sObject a = [Select ID From Account];
sObject b = [Select ID From Contract];

## Apex Classes

1. As in Java, you can create classes in Apex
2. A class is a template or blueprint from which objects are created. An object is an instance of a class
3. All objects have state and behavior, that is, things that an oject knows about itself (class variables), and things that an object can do (class methods)
4. A class can contain **variables** and **methods**
5. **Variables** are used to specify the state of an object, such as the object's *Name* or *Type*. Since these variables are associated with a class and are members of it, they are commonly referred to as member variables
6. **Methods** are used to control behavior, such as deleteLineItem or copyLineItems
7. A class can contain other classes, called inner class
8. An interface is like a class in which none of the methods have been implemented - the method signatures are there, but the body of each method is empty. To use an interface, another class must implement it by providing ...

      ```apex
      public class myOuterClass {
         // Additional myOuterClass code here
         class myInnerClass {
            // myInnerClass code here
         }
      }
      ```

9. In Apx, you can define top-level classes (also called outer classes) as well as inner classes, that is, a class defined within another class. You can only have inner classes one level deep
10. Avoid using standard object names for class names
11. To define a class, specify the following,
    1. Access Modifiers,
       1. You must use one of the access modifiers (such as **public** or **global**) in the declaration of a top-level class
       2. You do ot have to use an access modifier in the declaration of an inner class
    2. Optional definition modifiers (such as virtual, abstract, and so on)
    3. Required: The keyword class followed by the name of the class
    4. Optional extensions and/or implementations

      ```apex
      private | public | global
      [virtual | abstract | with sharing | without sharing]
      class ClassName [implements InterfaceNameList] [extends ClassName]
      {
         // The body of the class
      }
      ```

12. To declare a variable, specify the following,
    1. Optional: Modifiers, such as public or final, as well as static
    2. Required: The data type of the variable, such as String or Boolean
    3. Required: the name of the variable
    4. Optional: The value of the variable
13. Use the following syntax when defining a variable,

      ```apex
      [public | private | protected | global] [final] [static] data_type variable_name [= value];
      ```

14. User-defined methods,
    1. Can be used anywhere that system methods are used
    2. Can be recursive
    3. Can refer to themselves or to methods defined later in the same class or anonymous block. Forward declarations are applicable
15. Passed Method Arguments,
    1. In Apex, all primitive data type arguments, such as **Integer** or **String**, are passed into methods by value. This fact means that any changes to the arguments exist only within the scope of the method. When the method returns, the changes to the arguments are lost

```apex
// PassPrimitiveTypeExample
// Primitive Data Type -> By Value
// Non-Primitive Data Type -> By Ref

public class PassPrimitiveTypeExample {
   public static void debugStatusMessage() {
      String msg = 'Original value';

      processString(msg);

      System.debug(msg);
   }

   public static void processString(String s) {
      s = 'Modified value';
   }
}
```

```apex
public class PassNonPrimitiveTypeExample {

   public static void createTemperatureHistory() {

   }

   public stat void reference(List<Integer> m) {
      m.add(70);
      m.add(68);
      m.add(75);
      m.add(80);
      m.add(82);
   }

   public static void referenceNew(List<Integer> m) {
      // Assign argument to a new list of five temperature values
      m = new List<Integer>{55, 59, 60, 62, 65};
   }
}
```

## Passing Method Arguments

1. In Apex, all primitive data type arguments, such as Integer or String, are passed into methods by value. This fact means that any changes to the arguments exist only within the scope of the method. When the method returns, the changes to the arguments are lost

## Data Modelling

- Order Header,
  - Ord #
  - Ord Date
- OrderLineItem,
  - OrderID
  - PrdID
  - Qty
  - UnitPrice

## Transactions

- An Apex transaction represents a set of operations that are executed as a single unit
- All DML operations in a transaction either completely successfully, or if an error occurs in one operation, the entire transaction is rolled back and no data is committed to the database
- The boundary of a transaction can be a trigger, a class method, an anonymous block of code, a Visualforce page, or a custom Web Service method
- An Apex transaction is sometimes referred to as an execution context. Both terms refer to the same thing

### How Are Transactions Useful

- Transactions are useful when several operations are related, and either all of none of the operations should be committed. This keeps the database in a consistent state
- There are meany business scenarios that benefit from transaction processing. For example, transferring funds from one ank account to another is a common scenario. It involves debiting the first account and crediting the second account with th amount to transfer. These two operations need to be committed together to thr database. But if the debit operation succeeds and the credit operation fails, the account balances will be inconsistent.
- Let's have a look at an example that shows how all DML insert operations in a method are rolled back when the last operation causes a validation rule failure

```apex
public class AccountsOperation {

   public static void createAccountAndContact(string accountName, string contactFirstName, string contactLastName) {
      Account acc = new Account (Name = accountName);

      insert acc;

      Contact con = new Contact(FirstName = contactFirstName,
                                 LastName = contactLastName,
                                 AccountId = acc.id);

      insert con;
   }
}
```

To call the above code,

```apex
AccountsOperation.createAccountAndContact("Hello World Corp", "Saif", "Ul Islam");
```

To make the above code fail,

```apex
AccountsOperation.createAccountAndContact("XYZ Corp", "Saif", "");
```

All statements will be rolled back wherever a mistake occurs.

## Asynchronous Apex

- Apex offers multiple ways for running our Apex code asynchronously. Here are different asynchronous Apex features and when to use each,
  - **Scheduled Apex**, (interfaces provided by Salesforce)
    - To schedule an Apex class to run on a specific schedule
  - **Batch Apex**, (interfaces provided by Salesforce)
    - For long-running jobs with large data volume that need to be performed in baches, such as database maintenance jobs
    - For jobs that need larger query results than regular transactions allow
  - **Future Methods**, (annotation must be used)
    - When you have a long-running method and need to prevent delaying an Apex transaction
    - When you make call-outs to external Web services
    - To segregate DML operations and bypass the mixed save DML error
  - **Queue-able Apex**, (interfaces provided by Salesforce)
    - To start a long-running operation and get an ID for it
    - To pass complex types to a job
    - To chain jobs

### Scheduled Apex

- To schedule an Apex class to run at regular intervals, first write an Apex class that implements the Salesforce-provided interface **Schedulable**
- You can specify the schedule using either the Schedule Apex page in the Salesforce setup user interface, or the System.schedule method
- Salesforce schedules the class for execution at the specified time. Actual execution can be delayed based on service availability
- The scheduler runs as system - all classes are executed, whether the user has permission to execute the class or not (WITHOUT SHARING)
- To monitor or stop the execution of a scheduled Apex job using the Salesforce user interface from Setup, enter Scheduled Jobs in the Quick Find box
- The **Schedulable** interface contains one method that must be implemented called **execute**, `global void execute (SchedulableContext sc) {}`
- The implemented `execute` method must be declared as global or public
- Use the `execute` method to instantiate the class you want to schedule

```apex
global class scheduledMerge implements Schedulable {
   global void execute(SchedulableContext sc) {
      mergeNumbers M = new mergeNumbers();
   }
}
```

- Though it's possible to do additional processing in the execute method, Salesforce recommend that all processing take place in a separate class

### Batch Apex

### Future Methods

- A future method runs in the background, asynchronously
- AYou can call a future method for executing long-running operations, such as call-outs to external Web services or any operation you'd like to run in its own thread, on its own time
- Each future method is queued and executes when system resources become available. That way, the execution of your code doesn't have to wait for the completion of a long-running operation
- A benefit of using future method is that some governor limits are higher for asynchronous apex, such as SQOL query limits and heap size limits
- The calling method cannot track if the future method started, stopped, when it stated, when it will end. You can only call with the calling method
- There are no such methods such as

### Queue-Able Apex
