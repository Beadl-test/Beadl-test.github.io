---
layout: default
title: ConnectionMapping element
parent: HardwareSettings element
grand_parent: BEADL XML
nav_order: 1
has_children: no
---
# `<ConnectionMapping>`{: style="color: #268bd2;" } element
{: .no_toc}

A `<ConnectionMapping>`{: style="color: #268bd2;" } element maps a specific resource of the task controlling hardware to a specifier in the task description. Furthermore, it defines the type of the resource and enables to predefine specific values of it.

```xml
<HardwareSettings hardware="Control_Hardware" version="1.0">
  <ConnectionMapping name="ConnectionName" resourceName="UsedHardwareResource" type="UsedHardwareResourceType" />
</HardwareSettings>
```

## Attributes
- `name`{: style="color: #555555;" } defines a name of the connection mapping to be used within the BEADL task description. Since specific dependencies can be specified for `<ConnectionMapping>`{: style="color: #268bd2;" } elements, the name might not be unique within the whole list of defines `<ConnectionMapping>`{: style="color: #268bd2;" } elements.
- `resourceName`{: style="color: #555555;" } defines which resource of the specified hardware should be mapped onto the specifier.
- `type`{: style="color: #555555;" } defines the type of the specified resource.

Both attributes, `resourceName`{: style="color: #555555;" } and `type`{: style="color: #555555;" }, depend on the used hardware,

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current ConnectionMapping should be processed in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.
