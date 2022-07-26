---
layout: default
title: BeadlState element
parent: BeadlStates element
grand_parent: BEADL XML
nav_order: 1
has_children: true
---

1. TOC
   {:toc}

# `<BeadlState>`{: style="color: #268bd2;" } element

A `<BeadlState>`{: style="color: #268bd2;" } element define the actual description of a state in the BEADL's underlying state machine concept. 

</BeadlStateTransitions>
```

## Attributes
- `from`{: style="color: #555555;" } defines the origin of the transition (state in which the event occurs).
- `to`{: style="color: #555555;" } defines the destination of the transition.
- `eventTransition`{: style="color: #555555;" } defines the identifier of the event in the start state of the transition.
- `label`{: style="color: #555555;" } defines a label (description) of the transition.

## Child Elements
- `<Dependency>`{: style="color: #268bd2;" } element: Definition under which condition the current `<BeadlStateTransition>`{: style="color: #268bd2;" } element is defined in a trial. See [here]({{ site.baseurl }}{% link BEADL_XML/10_00_BEADL_Dependency.md %}) for a detailed description of the `<Dependency>`{: style="color: #268bd2;" } element.