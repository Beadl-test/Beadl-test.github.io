---
layout: default
title: BeadlArguments element
parent: BEADL XML
nav_order: 4
has_children: true
---
# `<BeadlArguments>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlArguments>`{: style="color: #268bd2;" } element defines a container for additional `<BeadlArgument>`{: style="color: #268bd2;" } elements (see [here]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %})).

Only one `<BeadlArguments>`{: style="color: #268bd2;" } element container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<BeadlArgument>`{: style="color: #268bd2;" } child elements.

<!-- 1. TOC
{:toc}


## `<BeadlArgument>`{: style="color: #268bd2;" } element
The `<BeadlArgument>`{: style="color: #268bd2;" } elements define values that are being defined outside of the trial structure and passed or updated to it. This way the experiment’s control system can update or predefine those values on trial-by-trial basis.

For `<BeadlArgument>`{: style="color: #268bd2;" } element, the following are specified:
- `name`{: style="color: #555555;" } defines the reference (variable name) to be accessed. The name attribute of a `<BeadlArgument>`{: style="color: #268bd2;" } is the actual variable name in the control instance.
- `expression`{: style="color: #555555;" } 
- `comment`{: style="color: #555555;" } defines a string to describe the argument and could be copied into the source code as an in-line comment there.
- `type`{: style="color: #555555;" } defines the data type of the argument. Valid values for the `type`{: style="color: #555555;" } are `numeric`, `logical`, `string`, and `other`. -->
