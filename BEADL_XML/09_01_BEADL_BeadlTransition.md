---
layout: default
title: BeadlStateTransition element
parent: BeadlStateTransitions element
grand_parent: BEADL XML
nav_order: 9
has_children: true
---
# `<BeadlStateTransition>`{: style="color: #268bd2;" } element
{: .no_toc}

```xml
<BeadlStateTransitions>
  <BeadlStateTransition from="StartState" to="DestinationState" eventTransition="Transition" label="" />
  ...

</BeadlStateTransitions>
```

## Attributes
- `from`{: style="color: #555555;" } defines the origin of the transition (state in which the event occurs).
- `to`{: style="color: #555555;" } defines the destination of the transition.
- `eventTransition`{: style="color: #555555;" } defines the identifier of the event in the start state of the transition.
- `label`{: style="color: #555555;" } defines a label (description) of the transition.

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current `<BeadlStateTransition>`{: style="color: #268bd2;" } element is defined in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.