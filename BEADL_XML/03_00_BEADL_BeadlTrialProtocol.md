---
layout: default
title: BeadlTrialProtocol element
parent: BEADL XML
nav_order: 3
has_children: true
---
# `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element
{: .no_toc}
The `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element describes and implements all properties of the trial-based behavior protocol.

## Attributes
- `name`{: style="color: #555555;" }: defines the name of the protocol. The name of the protocol will be used during the code generation process for creating needed files and folders and thus should not contain any whitespace characters.
- `startState`{: style="color: #555555;" }: defines the starting point of the trial structure. The content must refer to one state listed later in the description.
- `numberOfTrials`{: style="color: #555555;" }: defines how many trials a session should last. The content of this attribute can either be a number (must be quoted) or the string literal `INF` to indicate that the session will not be terminated based on the number of performed trials.


<!--## Child Elements-->
<!--{: .no_toc }-->
<!--{: .no_toc .text-delta }-->

<!--1. TOC-->
<!--{:toc}-->
