---
layout: default
title: BeadlStates element
parent: BEADL XML
nav_order: 8
has_children: true
---
# `<BeadlStates>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlStates>`{: style="color: #268bd2;" } element defines a container for specifying all states of a BEADL task protocol.

Only one `<BeadlStates>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and must contain at least one `<BeadlState>`{: style="color: #268bd2;" } child element.

```xml
...
<BeadlStates>
  <BeadlState name="StateName">
    ...
  </BeadlState>
</BeadlStates>
...
```

## Attributes
- None

## Child Elements
- [`<BeadlState>` element]({{ site.baseurl }}{% link BEADL_XML/08_01_BEADL_BeadlState.md %}): Definition of a single state of the behavioral task.