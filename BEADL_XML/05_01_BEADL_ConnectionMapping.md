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

A `<ConnectionMapping>`{: style="color: #268bd2;" } element element maps a specific resource of the task controlling hardware to a specifier in the task description. Furthermore, it defines the type of the resource and enables to predefine specific values of it.

## Attributes
- `name`{: style="color: #555555;" } defines a unique name of the connection mapping to be used within the BEADL task description.
- `resourceName`{: style="color: #555555;" } defines which resource of the specified hardware should be mapped onto the specifier.
- `type`{: style="color: #555555;" } defines the type of the specified resource.

Both attributes, `resourceName`{: style="color: #555555;" } and `type`{: style="color: #555555;" }, depend on the used hardware,

## Child Elements
- `<ConnectionMapping>`{: style="color: #268bd2;" } element: Definition under which condition the current ConnectionMapping should be processed in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<ConnectionMapping>`{: style="color: #268bd2;" } element.
