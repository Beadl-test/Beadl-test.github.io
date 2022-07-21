---
layout: default
title: BeadlArguments element
parent: BEADL XML
nav_order: 4
has_children: true
has_toc: false
---
# `<BeadlArguments>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlArguments>`{: style="color: #268bd2;" } element defines a container for additional `<BeadlArgument>`{: style="color: #268bd2;" } elements (see [here]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %})).

Only one `<BeadlArguments>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<BeadlArgument>`{: style="color: #268bd2;" } child elements.

```xml
...
<BeadlArguments>
  <BeadlArgument name="ExampleArgument" expression="123" comment="Description" type="numeric" />
</BeadlArguments>
...
```

## Attributes
- None

## Child Elements
- [`<BeadlArgument>` element]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %}): Definition of values that are being defined outside the trail structure and being passed to it on a trial-by-trial basis.