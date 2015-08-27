# PEM Problems
## Overview

### What is PEM?

Post Event Messaging (PEM) in the context of NHS 111 is an electronic document, that is transmitted to GP practices at the end of an NHS 111 Call. There are essentially two types of PEM a GP can receive, one that is ‘for action’ meaning a GP has been referred back to their own GP with a timeframe associated with it. The other is a ‘for information’ message, which is for the GP to inspect and file against the patients record.

## Clinical

## Operational

### Do I get one at the end of every call?

GP’s shouldn’t be getting one at the end of every call. They should receive a message each time if the outcome was ‘for action’ this means the patient has been told to see their own GP.

When a patient is referred to OOH then 111 should not be sending a PEM to the GP, this is to avoid duplication and has resulted in a significant reduction in PEM’s to GP’s.

There is also a never send list, that 111 systems are told to check and suppress a message being generated at all. These are:

* DX 28 – Contact Pharmacist 
* DX 52 – Refer to Police 
* DX 60 – Contact Optician next routine appointment within 72 hours 
* DX 22 – To be seen by Dental Practice within 3 working days 
* DX 23 – Contact Orthodontist next working day 
* DX 45 – Provide Service Location Information 
* DX 46 – Refer to Health Information 
* DX 63 – Refer to Fluline

This list has the desired effect of reducing the volume of PEMs without creating clinical risk given the nature of these referrals. However, the proportion of calls contained within this list is small (1.9%), and hence the reduction is likewise low. This list is reviewed as part of each NHS Pathways version release by the Regional Clinical Leads. 

### Why can’t it just work the same as Out of Hours does?

The issue relates to the fact that NHS 111 is a nationally available number, although routing calls is very accurate it cannot be guaranteed that a GP’s patients will be handled by the local 111 service. This can be due to border issues, new mobile masts that haven't been assigned to the area they are in and other factors that cannot be controlled. Water can also carry mobile phone signals much further distances and make it possible for a mobile mast further away to be connected to a mobile handset.

### Why am I receiving Faxes?

### Why am I receiving different versions of PEM?




## Technical

## What is Kettering

Kettering is a standard message format that Out of Hours services use to report back to GP’s. The issue with the standard is that it wasn’t maintained and now there are many variants of that standard. This has developed by evolution over a long time and has become fragmented. This is a problem for NHS 111 providers as they are unable to determine what versions are being sent to where making it difficult to send an electronic PEM for patients that are out of area. This would force the 111 provider into faxing the report which has a wide range of quality, is difficult to manage and is more expensive on both parties.

## What is DTS?

DTS stands for Data Transport Service. It is a mechanism for moving data, typically kettering from one computer system to another. It works much the same way as email, where a sending system sends the message to a central server which stores it until it is retrieved by the receiving system, typically by 08:00 each day.

## What is ITK and what are the benefits?

ITK is the acronym for HSCIC’s Interoperability Toolkit. It’s a standard for how systems talk to each other and is an alternate transport mechanism to DTS. 111 uses a subset of the ITK standards for sending information. The benefit is that it is synchronous, meaning that the sender is notified that the delivery was successful and the recipient has acknowledged they have the data. DTS is not able to do this as their is an intermediary server involved.

## What is CDA?

CDA is short for Clinical Document Architecture. It is a set of standards applied to HL7 messages to provide structure and integrity to the messages that are transmitted from one computer system to another. The receiving system is able to inspect these and know exactly what information is contained where. They do need to be populated with quality content.

## What is Rendered PEM and What does it look like?

Rendered PEM is a CDA document that is converted from being machine readable to human readable. Rendering can be done prior to sending to allow for sending documents to people over NHS mail for example. Using rendered PEM is a good way of integrating services quickly and cheaply, it would mean manual work for receivers but offers a good interim solution while receiving software applications are building the functionality.

A version of the pre-rendered PEM can be found here:

Recipients are also able to apply custom renderers to the native CDA documents if they wish.

## How can I setup EMIS Web to Work with 111 ITK?

## How can I setup TPP to Work with 111 ITK?

## How can I setup Vision to Work with 111 ITK?

## How can I setup Microtest to Work with 111 ITK?