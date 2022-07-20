---
layout: default
title: BeadlTrialProtocol element
parent: BEADL XML
nav_order: 3
has_children: true
---
# `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element
{: .no_toc}
The `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element describes and implements all properties of the trial-based behavior protocol. The element itself has the following attributes:
- `name`{: style="color: #555555;" }: defines the name of the protocol. The name of the protocol will be used during the code generation process for creating needed files and folders and thus should not contain any whitespace characters.
- `startState`{: style="color: #555555;" }: defines the starting point of the trial structure. The content must refer to one state listed later in the description.
- `numberOfTrials`{: style="color: #555555;" }: defines how many trials a session should last. The content of this attribute can either be a number (must be quoted) or the string literal `INF` to indicate that the session will not be terminated based on the number of performed trials.


## Child Elements
{: .no_toc }
<!--{: .no_toc .text-delta }-->

1. TOC
{:toc}

### `<BeadlArguments>`{: style="color: #268bd2;" } element
The `<BeadlArguments>`{: style="color: #268bd2;" } element defines a container for additional `<BeadlArgument>`{: style="color: #268bd2;" }. Only one `<BeadlArguments>`{: style="color: #268bd2;" } container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<BeadlArgument>`{: style="color: #268bd2;" } child elements and has no additional attributes.

### `<BeadlArgument>`{: style="color: #268bd2;" } element
The `<BeadlArgument>`{: style="color: #268bd2;" } elements define values that are being defined outside the trial structure and are passed to a single trial and allow to update certain values on a trial-by-trial basis. This way the experiment’s control system (in case of Bpod, either the running MATLAB or Python instance) can update or predefine those values.

For `<BeadlArgument>`{: style="color: #268bd2;" } elements, the following attributes can be defined:
- **name**

### HardwareSettings

###
