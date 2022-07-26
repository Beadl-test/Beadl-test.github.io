---
layout: default
title: VirtualEvent element
parent: BeadlEvents element
grand_parent: BEADL XML
nav_order: 2
has_children: false
---
# `<VirtualEvent>`{: style="color: #268bd2;" } element
{: .no_toc}

`<VirtualEvent>`{: style="color: #268bd2;" } elements define specifiers within a BEADL protocol that link to virtual entities defined by the BEADL framework that could generate state transitions.

The XML definition of a `<VirtualEvent>`{: style="color: #268bd2;" } element inside the XML structure resembles the definition of `<HardwareEvent>`{: style="color: #268bd2;" } elements with the exception of how the `connection`{: style="color: #555555;" } attribute is being defined (see details below).

```xml
...
<BeadlEvents>
  <VirtualEvent eventName="Event2" connection="ConnectionName.expression" type="" comment="" />
</BeadlEvents>
...
```

## Attributes
- `eventName`{: style="color: #555555;" } defines a unique name of the event to be used within the BEADL task description.
- `connection`{: style="color: #555555;" } defines which virtual resource the event should be linked to. See the definitions of virtual resources below.
- `type`{: style="color: #555555;" } defines the type of the specified event. This attribute is meant to be used in future releases and is currently not not required.
- `comment`{: style="color: #555555;" } defines an additional documentation of the element that could be populated also in the code generation process for automatically generating the behavior task for the defined target platform of the task controlling system. This attribute is optional.

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current `<VirtualEvent>`{: style="color: #268bd2;" } element is defined in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.

## Defined virtual resources
In the current version of BEADL, the following virtual events are defined. Please note that such virtual resources have only one component `expression`{: style="color: #555555;" } specified that need to be used for the linked `<ConnectionMapping>`{: style="color: #268bd2;" } element.specified.

### ArgumentEvent
A virtual event that occurs if a [BeadlArgument]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %} has a specific value.

### VariableEvent
A virtual event that occurs if a variable that was set in a preceding state (see [VirtualAction]({{ site.baseurl }}{% link BEADL_XML/07_02_BEADL_VirtualAction.md %}) has a specific value.

### TimeSpanEvent
A virtual event that occurs if the duration between the start times of two states has a specific value.
