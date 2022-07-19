---
layout: default
title: BEADL XML
nav_order: 3
has_children: true
---
# BEADL XML
{: .no_toc}
In its current version, BEADL defines a rigid, yet extensible framework by using XML (eXtensible Markup Language) to describe behavioral tasks. This way, the main concept of the task logic can be precisely defined as well as the requirements of the different behavioral control environments can be met. In addition to that, using an XML Schema Definition (XSD) ensures the formal verification of the content of a XML-based BEADL definition.
<hr>

# BEADL XML Element Overview
{: .no_toc}
Since BEADL is implemented using XML, there should only be a single root element `<BEADL>`{: style="color: #268bd2;" } in the structure of a well-formed BEADL file. Under this root element two different child elements are currently designated, describing the trial-based protocol implementation `<BeadlTrialProtocol>`{: style="color: #268bd2;" } and properties for the graphical editor `<BeadlEditor>`{: style="color: #268bd2;" }.
Under the `<BeadlTrialProtocol>`{: style="color: #268bd2;" } node, all properties of the actual protocol implementation as well as hardware-specific attributes are gathered together. A separation of hardware-specific attributes should facilitate a change of the used hardware platform, so a change does not interfere with the actual protocol implementation and interpretation.

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
</BEADL>
```

# Naming Convention
Looking at the code snippet above, an XML description consists basically of four different entities:

- XML elements: XML elements are the main building blocks to describe a data structure in XML. They are delimited by angled brackets (`< >`) as tags and must be properly terminated. An element starts with the start-tag (`<elementName>`) and can have nested elements (child elements). If an element has at least one child element, the termination of the element must be done with an end-tag (`</elementName>`). If an element does not have any child elements, it can be terminated within the start-tag itself (<elementName />)
- XML attributes: 

- Attribute values: 
- XML Prolog: The first line within an XML document is some kind of a special XML element and describes the XML-version and character encoding of the XML file itself using the attributes `version` and `encoding`. All valid XML files must start with a prolog, whereas the attribute values might be different.

# XML Schema Definition
The formal structure of an XML description can be validated using a so-called XML Schema Definition (XSD). This is a description of the XML structure, using an XML-based description itself. The latest version of XSD-based schema definition for BEADL-XML can be accessed [here](https://github.com/BEADL/XSD/blob/main/BEADL.xsd).