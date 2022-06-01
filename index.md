---
layout: default
title: Home
nav_order: 1
has_children: false
---
BEADL
{: .fs-9 .fw-500 .lh-tight}
BEhavioral tAsk Description Language
{: .fs-9 .fw-500 .lh-tight}

A Universal Framework for Descirbing Behavioral Tasks
{: .fs-6 .fw-500 .lh-tight}

{: .no_toc}

- TOC
{:toc}

# Motivation
Technological advances in neuroscience have dramatically increased the possibilities for monitoring, quantifying, and  manipulating brain activity during behavior. In contrast, efforts to describe behavior have lagged behind. One reason for this is that there is no general formal framework to design or describe behavioral tasks, which are typically performed using specialized and often ad hoc hardware and software systems. The lack of universal behavioral task descriptions makes it challenging to communicate, share, publish, and reuse behavioral tasks.

# Approach
We propose BEADL (BEhavioral tAsk Description Language) to abstract and standardize behavioral task descriptions on two layers. A graphical layer specifies elements to describe behavioral tasks as a state machine in a formal flow diagram and how the task controlling system interacts with a subject. This graphical layer has been designed to be easy to understand while retaining all aspects of the behavioral task. The second layer is a corresponding, XML-based description of the task. This layer forms the rigid, yet extensible foundation of BEADL and hides hardware implementation related details form the graphical representation.

<!--BEADL defines a universal framework to describe Behavioral Tasks.
{: .fs-9 }

Beadl Framework
{: .fs-6 .fw-300}

[Get started now](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2} [View code on GitHub](https://github.com/BEADL/){: .btn .fs-5 .mb-4 .mb-md-0} -->