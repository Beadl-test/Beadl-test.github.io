---
layout: default
title: BeadlStateTransitions element
parent: BEADL XML
nav_order: 9
has_children: true
---
# `<BeadlStateTransitions>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlStateTransitions>`{: style="color: #268bd2;" } element defines a container for specifying all possible transitions between the different states defined by the different specified events per state..

Only one `<BeadlStateTransitions>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and must contain at least one `<BeadlStateTransition>`{: style="color: #268bd2;" } child element.

```xml
...
<BeadlStateTransitions>
  <BeadlStateTransitions ... />
  ...

</BeadlStateTransitions>
...
```

## Attributes
- None

## Child Elements
- [`<BeadlStateTransition>` element]({{ site.baseurl }}{% link BEADL_XML/09_01_BEADL_BeadlTransition.md %}): Definition of a single transition between two states in a task description.