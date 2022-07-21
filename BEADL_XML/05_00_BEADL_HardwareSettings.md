---
layout: default
title: HardwareSettings element
parent: BEADL XML
nav_order: 5
has_children: true
has_toc: false
---
# `<HardwareSettings>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<HardwareSettings>`{: style="color: #268bd2;" } element defines a container for for  `<ConnectionMapping>`{: style="color: #268bd2;" } elements (see [here]({{ site.baseurl }}{% link BEADL_XML/05_01_BEADL_ConnectionMapping.md %})).

Only one `<BeadlArguments>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<BeadlArgument>`{: style="color: #268bd2;" } child elements.

```xml
<HardwareSettings hardware="Control_Hardware" version="1.0">
  ...
</HardwareSettings>
```

## Attributes
- `hardware`{: style="color: #555555;" } defines the hardware name of that controls the behavioral task. reference (variable name) to be accessed. The name attribute of a `<BeadlArgument>`{: style="color: #268bd2;" } is the actual variable name in the control instance.
- `version`{: style="color: #555555;" } defines the version of the specified hardware.

## Child Elements
- None