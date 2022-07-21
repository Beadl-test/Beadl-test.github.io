---
layout: default
title: BeadlArgument element
parent: BeadlArguments element
grand_parent: BEADL XML
nav_order: 1
has_children: no
has_toc: false
---
# `<BeadlArgument>`{: style="color: #268bd2;" } element
{: .no_toc}

The `<BeadlArgument>`{: style="color: #268bd2;" } elements define values that are being defined outside of the trial structure and passed or updated to it. This way the experiment’s control system can update or predefine those values on trial-by-trial basis.
```xml
...
<BeadlArguments>
  <BeadlArgument name="ExampleArgument" expression="123" comment="Description" type="numeric" />
</BeadlArguments>
...
```

## Attributes
- `name`{: style="color: #555555;" } defines the reference (variable name) to be accessed. The name attribute of a `<BeadlArgument>`{: style="color: #268bd2;" } is the actual variable name in the control instance.
- `expression`{: style="color: #555555;" } defines the value of the argument. Since it is being stored as a string, this element can have an arbitrary content but together with the attribute `type`{: style="color: #555555;" } it affects the outcome of possible parsing or code-generation process for the used target platform of the behavior control environment.
- `comment`{: style="color: #555555;" } defines a string to describe the argument and could be copied into the source code as an in-line comment there.
- `type`{: style="color: #555555;" } defines the data type of the argument. Valid values for the `type`{: style="color: #555555;" } are `numeric`, `logical`, `string`, and `other`.

## Child Elements
- None