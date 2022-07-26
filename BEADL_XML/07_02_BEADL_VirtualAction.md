---
layout: default
title: VirtualAction element
parent: BeadlActions element
grand_parent: BEADL XML
nav_order: 2
has_children: false
---
# `<VirtualAction>`{: style="color: #268bd2;" } element
{: .no_toc}

`<VirtualAction>`{: style="color: #268bd2;" } elements define specifiers within a BEADL protocol that link to virtual entities defined by the BEADL framework that can specific actions.

The XML definition of a `<VirtualAction>`{: style="color: #268bd2;" } element inside the XML structure resembles the definition of `<HardwareAction>`{: style="color: #268bd2;" } elements with the exception of how the `connection`{: style="color: #555555;" } attribute is being defined (see details below).

```xml
...
<BeadlActions>
  <VirtualAction actionName="Action2" connection="ConnectionName.expression" type="" comment="" />
</BeadlActions>
...
```

## Attributes
- `actionName`{: style="color: #555555;" } defines a unique name of the action to be used within the BEADL task description.
- `connection`{: style="color: #555555;" } defines which virtual resource the action should be linked to. See the definitions of virtual resources below.
- `type`{: style="color: #555555;" } defines the type of the specified action. This attribute is meant to be used in future releases and is currently not not required.
- `comment`{: style="color: #555555;" } defines an additional documentation of the element that could be populated also in the code generation process for automatically generating the behavior task for the defined target platform of the task controlling system.

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current `<VirtualAction>`{: style="color: #268bd2;" } element is defined in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.

## Defined virtual resources
In the current version of BEADL, the following virtual actions are defined. Please note that such virtual resources have only one component `expression`{: style="color: #555555;" } specified that need to be used for the linked `<ConnectionMapping>`{: style="color: #268bd2;" } element.

### CallbackAction
A virtual action that calls a specific software function through the task controlling environment. Such kind of implementations might violate certain real-time requirements and highly depends on the implementation of the hole system in general.

### SetVariableAction
A virtual action that stores a value in a variable that can be accessed in subsequent states via the virtual event [VariableEvent]({{ site.baseurl }}{% link BEADL_XML/06_02_BEADL_VirtualEvent.md %}).
