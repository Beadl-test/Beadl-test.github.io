---
layout: default
title: BeadlTrialProtocol element
parent: BEADL XML
nav_order: 3
has_children: false
has_toc: false
---
# `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element
{: .no_toc}
The `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element describes and implements all properties of the trial-based behavior protocol.

## Attributes
- `name`{: style="color: #555555;" }: defines the name of the protocol. The name of the protocol will be used during the code generation process for creating needed files and folders and thus should not contain any whitespace characters.
- `startState`{: style="color: #555555;" }: defines the starting point of the trial structure. The content must refer to one state listed later in the description.
- `numberOfTrials`{: style="color: #555555;" }: defines how many trials a session should last. The content of this attribute can either be a number (must be quoted) or the string literal `INF` to indicate that the session will not be terminated based on the number of performed trials.

## Child Elements
- `<BeadlArguments>` element: Container for `<BeadlArgument>` elements
  - `<BeadlArgument>` element: Definition for trial-dependent arguments which values are controlled outside the trial structure
