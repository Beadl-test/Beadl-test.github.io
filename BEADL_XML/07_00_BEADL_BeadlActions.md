---
layout: default
title: BeadlActions element
parent: BEADL XML
nav_order: 7
has_children: true
---
# `<BeadlActions>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlActions>`{: style="color: #268bd2;" } element defines a container for specifying all the different actions within the BEADL task protocol that could potentially be used.

Only one `<BeadlActions>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<HardwareAction>`{: style="color: #268bd2;" } or `<VirtualAction>`{: style="color: #268bd2;" } child elements.

```xml
...
<BeadlActions>
  <HardwareAction eventName="Action1" connection="ConnectionName.Sink" type="" comment="" />
  <VirtualAction eventName="Action2" connection="VirtualEventName.expression" type="" comment="" />
</BeadlActions>
...
```

## Attributes
- None

## Child Elements
- [`<HardwareAction>` element]({{ site.baseurl }}{% link BEADL_XML/07_01_BEADL_HardwareAction.md %}): Definition of actions that are using output entities defined by the used hardware resources.
- [`<VirtualAction>` element]({{ site.baseurl }}{% link BEADL_XML/07_02_BEADL_VirtualAction.md %}): Definition of actions that are using virtual entities.