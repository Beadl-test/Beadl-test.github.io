---
layout: default
title: BEADL XML
nav_order: 3
has_children: true
---
# BEADL XML
{: .no_toc}
In its current version, BEADL defines a rigid, yet extensible framework by using XML (eXtensible Markup Language) to describe behavioral tasks. This way, the main concept of the task logic can be precisely defined as well as the requirements of the different bevaioral control environments can be met. In addition to that, using an XML Schema Definition (XSD) ensures the formal verification of the content of a XML-based BEADL definition.
<hr>
# BEADL XML Element Overview
{: .no_toc}
Since BEADL is implemented using XML, there should only be a single root element `<BEADL>` in the structure of a well-formed BEADL file. Under this root element two different child elements are currently designated, describing the trial-based protocol implementation `<BeadlTrialProtocol>` and properties for the graphical editor `<BeadlEditor>`.
Under the `<BeadlTrialProtocol>`{: .inline-code-color } node, all properties of the actual protocol implementation as well as hardware-specific attributes are gathered together. A separation of hardware-specific attributes should facilitate a change of the used hardware platform, so a change does not interfere with the actual protocol implementation and interpretation.

The following code snippet shows the basic structure of a BEADL-XML file.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<BEADL version="0.1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="BEADL.xsd">
<BeadlTrialProtocol name="DummyTask" startState="InitTrial" numberOfTrials="INF">
...
</BeadlTrialProtocol>
<BeadlEditor>
...
</BeadlEditor>
```