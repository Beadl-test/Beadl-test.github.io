---
layout: default
title: BeadlTrialProtocol element
parent: BEADL XML
nav_order: 3
has_children: false
---
# BeadlTrialProtocol element
{: .no_toc}
Details. 

## Child Elements
{: .no_toc .text-delta }

1. TOC
{:toc}

### BeadlArguments
The `<BeadlArguments>`{: style="color: #268bd2;" } element defines a container for additional `<BeadlArgument>`{: style="color: #268bd2;" }. Only one `<BeadlArguments>`{: style="color: #268bd2;" } container is allowed within a `<BeadlTrialProtocol>`{: style="color: #268bd2;" } element and it can have zero or more `<BeadlArgument>`{: style="color: #268bd2;" } child elements and has no additional attributes.

### BeadlArgument
The `<BeadlArgument>`{: style="color: #268bd2;" } elements define values that are being defined outside the trial structure and are passed to a single trial and allow to update certain values on a trial-by-trial basis. This way the experiment’s control system (in case of Bpod, either the running MATLAB or Python instance) can update or predefine those values.

For `<BeadlArgument>`{: style="color: #268bd2;" } elements, the following attributes can be defined:
- **name**

### HardwareSettings

###
