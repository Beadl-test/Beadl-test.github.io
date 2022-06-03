---
layout: default
title: BEADL XML
nav_order: 3
has_children: true
---
# BEADL XML
{: .no_toc}
In its current version, BEADL defines a rigid, yet extensible framework by using XML (eXtensible Markup Language) to describe behavioral tasks. This way, the main concept of the task logic can be precisely defined as well as the requirements of the different bevaioral control environments can be met. In addition to that, using an XML Schema Definition (XSD) ensures the formal verification of the content of a XML-based BEADL definition.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Beadl version="0.1">
<BeadlTrialProtocol name="DummyTask" startState="InitTrial" numberOfTrials="Inf">
...
</BeadlTrialProtocol>
<BeadlEditor>
...
</BeadlEditor>
```