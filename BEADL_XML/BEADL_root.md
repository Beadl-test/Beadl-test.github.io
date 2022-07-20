---
layout: default
title: BEADL-XML root element
parent:  BEADL XML
nav_order: 2
has_children: true
---

The root element `<BEADL>`{: style="color: #268bd2;" } in the XML format works as a container for the behavioral task protocol definition but also to non-protocol specific properties such as properties for a graphical representation of the protocol in an additional editor.
```xml
<BEADL version="0.1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="BEADL.xsd">
<BeadlTrialProtocol name="DummyTask" startState="InitTrial" numberOfTrials="INF">
...
</BeadlTrialProtocol>
<BeadlEditor>
...
</BeadlEditor>
</BEADL>
```

# Attributes
In its current version, the BEADL-XML{: style="color: red; opacity: 0.80;" } format defines 3 attributes for the `<BEADL>`{: style="color: #268bd2;" } root element.
- `version`{: .text-blue-100 }: defines the BEADL version being used for describing this protocol
- `xmlns:xsi`{: .text-blue-100 }:  declares the prefix `xsi` as a standard namespace to use `http://www.w3.org/2001/XMLSchema-instance` as its namespace
- `xsi:noNamespaceSchemaLocation`{: .text-blue-100 }: defines the XML Schema Definition (XSD) file to be used for validation without using a dedicated namespace. Right now the assumption is that it is stored in the same location as the protocol file. You can download the latest version (v 0.1.0) of the XSD file [here](https://github.com/BEADL/XSD/releases/download/0.1.0/BEADL.xsd).

# Child elements