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
- [`<BeadlArguments>` element]({{ site.baseurl }}{% link BEADL_XML/04_00_BEADL_BeadlArguments.md %}): Container for [`<BeadlArgument>` elements]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %})
- [`<HardwareSettings>` element]({{ site.baseurl }}{% link BEADL_XML/05_00_BEADL_HardwareSettings.md %}): Definitions of the used behavioral control environment and definitions of the used resources via [`<ConnectionMapping>` elements]({{ site.baseurl }}{% link BEADL_XML/05_01_BEADL_ConnectionMapping.md %})
- [`<BeadlEvents>` element]({{ site.baseurl }}{% link BEADL_XML/06_00_BEADL_BeadlEvents.md %}): Container for the definition of events (either [`<HardwareEvent>` elements]({{ site.baseurl }}{% link BEADL_XML/06_01_BEADL_HardwareEvent.md %}) or [`<VirtualEvent>` elements]({{ site.baseurl }}{% link BEADL_XML/06_02_BEADL_VirtualEvent.md %}) to be sensed for transitioning between states.
- [`<BeadlActions>` element]({{ site.baseurl }}{% link BEADL_XML/07_00_BEADL_BeadlActions.md %}): Container for the definition of actions (either [`<HardwareActions>` elements]({{ site.baseurl }}{% link BEADL_XML/07_01_BEADL_HardwareAction.md %}) or [`<VirtualActions>` elements]({{ site.baseurl }}{% link BEADL_XML/07_02_BEADL_VirtualAction.md %}) to be executed when entering a state.
- [`<BeadlStates>` element]({{ site.baseurl }}{% link BEADL_XML/08_00_BEADL_BeadlStates.md %}): Container for the definition of the [`<BeadlState>` elements]({{ site.baseurl }}{% link BEADL_XML/08_01_BEADL_BeadlState.md %}) that define the structure of the behavioral task.
- [`<BeadlTransitions>` element]({{ site.baseurl }}{% link BEADL_XML/09_00_BEADL_BeadlTransitions.md %}): Container for the definition of [`<BeadlTransition>` elements]({{ site.baseurl }}{% link BEADL_XML/09_01_BEADL_BeadlTransition.md %}) that define the possible paths within the behavioral task.