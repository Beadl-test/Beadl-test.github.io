---
layout: default
title: Dependency element
parent: BEADL XML
nav_order: 10
has_children: true
---
# `<Dependency>`{: style="color: #268bd2;" } element
{: .no_toc}

`<Dependency>`{: style="color: #268bd2;" } elements play a special role in a BEADL task description since they can be defined as child elements for different element types. Such an element allows the corresponding parent element only to be added to the task description if a specified criterion is met.

```xml
<BeadlXmlElement >
  <Dependency type="DepedencyType" expression="Criterion" />
</BeadlXmlElement>
```

## Attributes
- `type`{: style="color: #555555;" } defines which type of dependency (see below).
- `expression`{: style="color: #555555;" } defines the actual dependency. The expression depends on the type of the dependency itself.

## Child Elements
- none

## Defined Dependency Types
As of now, only the following dependency type is implemented:
- `BeadlArgumentDependency`: With this dependency type, the value of a specific `<BeadlArgument>`{: style="color: #268bd2;" } (see [here]({{ site.baseurl }}{% link BEADL_XML/04_01_BEADL_BeadlArgument.md %})) defines, if the dependency's parent element is being defined for the current trial or not.
