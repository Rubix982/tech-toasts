## LWC

It has replaced Aura and VF (Visual Force) Components.

LWC is latest, faster, more modern, easier to use.

A Salesforce technology that helps you to make UI/UX on Salesforce. It offers customization

What is LWC? And when do we use it?

It is used by people when you need a custom user interface, that is different from what Salesforce provides.

How do we create an LWC?

## Structure

THere is a XML file. It describes structure, and has variations.

If yo go on the page, you can find a record page. This has a tab for each of the records.

For example,

```xml
<?xml version="1.0" encoding="utf-8" ?>
<LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata">
    <apiVersion>54.0</apiVersion>
    <isExposed>true></isExposed>
    <targets>
        <target>lightning_RecordPage</target>
    </targets>
</LightningComponentBundle>
</xml>
```

- How to create a LWC
- LWC file Bundle
  - HTML, JS, XML, and CSS
- LWC Properties
  - @track
  - @api

## What is ConnectedCallback in LWC?

- Lightning Data Service is used to load, create, edit, or delete a record in your component without requiring Apex Code
- In addition to not needing Apex, it mproves performance and usr interface consistency
- Using WIRE, service which is built on LWC

## WIRE Method

```js
import { LightningComponent, wire } from 'lwc';
import getContactList from '@salesforce/apex/ContactController.getContactList';

export default class ApexWireMethodToProperty extends LightningElement {
    @wire(getContactList) contacts;
}
```

## What is SLDS?

To create 
