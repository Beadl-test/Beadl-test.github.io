---
layout: default
title: BeadlEvents element
parent: BEADL XML
nav_order: 6
has_children: true
---
# `<BeadlEvents>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlEvents>`{: style="color: #268bd2;" } element defines a container for specifying all the different events within the BEADL task protocol that could potentially trigger state transitions.

Only one `<BeadlEvents>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<HardwareEvent>`{: style="color: #268bd2;" } or `<VirtualEvent>`{: style="color: #268bd2;" } child elements.

```xml
...
<BeadlEvents>
  <HardwareEvent eventName="Event1" connection="ConnectionName.Source" type="" comment="" />
  <VirtualEvent eventName="Event2" connection="VirtualEventName.expression" type="" comment="" />
</BeadlEvents>
...
```

## Attributes
- None

## Child Elements
- [`<HardwareEvent>` element]({{ site.baseurl }}{% link BEADL_XML/06_01_BEADL_HardwareEvent.md %}): Definition of events derived from inputs or other entities defined by the used hardware resources.
- [`<VirtualEvent>` element]({{ site.baseurl }}{% link BEADL_XML/06_02_BEADL_VirtualEvent.md %}): Definition of events derived from virtual entities.