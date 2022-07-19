---
layout: default
title: BeadlEditor element
parent: BEADL XML
nav_order: 4
has_children: false
---

In future releases of BEADL-XML, the `<BeadlEditor>`{: style="color: #268bd2;" } element will hold the graphical represenation of a BEADL-based protocol to be used in the BEADL Editor. As of now (version 0.1.0), the BeadlEditor element can either be omitted in a BEADL-XML file or must not have any attributes nor child elements. Multiple instances of the `<BeadlEditor>`{: style="color: #268bd2;" } element are not allowed. Any violation of these restriction will cause the validation against the XSD schema to fail!