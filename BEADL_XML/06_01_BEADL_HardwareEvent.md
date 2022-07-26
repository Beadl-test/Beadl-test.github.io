---
layout: default
title: HardwareEvent element
parent: BeadlEvents element
grand_parent: BEADL XML
nav_order: 1
has_children: false
---
# `<HardwareEvent>`{: style="color: #268bd2;" } element
{: .no_toc}

`<HardwareEvent>`{: style="color: #268bd2;" } elements define specifiers within a BEADL protocol that link directly to the physical input entities of the task controlling system. Therefore, a corresponding `<ConnectionMapping>`{: style="color: #268bd2;" } has to be defined, to which this physical input can be linked to. By introducing this layered structure, the process of describing events becomes more organized in case the physical hardware connection has multiple grouped individual inputs that need to be referred to, and simplifies compatibility between different hardware platforms.

```xml
...
<BeadlEvents>
  <HardwareEvent eventName="Event1" connection="ConnectionName.Source" type="" comment="" />
</BeadlEvents>
...
```

## Attributes
- `eventName`{: style="color: #555555;" } defines a unique name of the event to be used within the BEADL task description.
- `connection`{: style="color: #555555;" } defines which physical input resource of the specified hardware should be linked to this event.
- `type`{: style="color: #555555;" } defines the type of the specified event. This attribute is meant to be used in future releases and is currently not not required.
- `comment`{: style="color: #555555;" } defines an additional documentation of the element that could be populated also in the code generation process for automatically generating the behavior task for the defined target platform of the task controlling system. This attribute is optional.

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current `<HardwareEvent>`{: style="color: #268bd2;" } element is defined in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.