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

A version of the pre-rendered PEM can be found here: [NHS111CopyRecipientRendered.pdf](media/NHS111CopyRecipientRendered.pdf)

Recipients are also able to apply custom renderers to the native CDA documents if they wish.
