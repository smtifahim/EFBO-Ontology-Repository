# The EFBO Ontology Repository
This repository contains three ontology files relevant to the Event-Based Functional Behaviour Ontology (EFBO) project as part of a Software Engineering thesis. The thesis introduces an effective ontology-oriented formal approach to representing event-based software systems, that is designed to be both machine-processable and human-comprehensible. Based on the theory of events and change in AI-based commonsense reasoning and the notion of affordances, we developed a novel approach to functional reasoning which is more intuitive and practical compared to the existing formal systems of representation. 
* Link to the Event-Based Functional Behaviour Ontology (EFBO-Core)
  * [Link to the readable web version](https://htmlpreview.github.io/?https://github.com/smtifahim/EFBO-Ontology-Repository/blob/master/ebfo-core/Event-Based%20Functional%20Behavior%20Ontology%20(EFBO).html)
* Link to the EFBO Functional Reasoning Category (EFBO-FRC) Ontology
  * Link to the readable web version
* Link to the EFBO Functional Consistency Validation (EFBO-V) Ontology
  * Link to the readable web version

https://htmlpreview.github.io/?https://github.com/bartaz/impress.js/blob/master/index.html

Refer to the thesis document to learn more about the project.
* F. T. Imam (2017). [An ontology-oriented approach to represent and compare the functional behavior of event-based systems](https://qspace.library.queensu.ca/items/5456ca18-bf0a-4cd8-86e7-0e60222eac5d). Doctoral dissertation, Queen's University (Canada).

## The Event-Based Functional Behaviour Ontolog (EFBO-Core)
The Event-Based Functional Behavior Ontology (EFBO) is an ontology to represent the functional behavior of event-based systems. The ontology provides logical descriptions of the core concepts associated with event-based systems. Based on the understanding of functional reasoning, the notion of affordances, and the notion of action, events, and change in commonsense reasoning the ontology can effectively represent the functional behavior of event-based systems. The ontology-based representation that we have developed promotes an enhanced comprehension and control over the following defining aspects of the event-based systems.
* **Allowable set of events**: What are the set of events that exist for an application system and how to represent them?
* **Allowable flow of events**: How to represent the partial order restrictions on the allowable set of events?
* **Event locations and interfaces**: How to describe the system in terms of its events and their associated interfaces?
* **Allowable event-interface-agent interactions**: How to represent the interactions between the agents, interfaces, and the events of the system?

The EFBO is written in OWL-DL formalism and we have verified its consistency using the HermiT reasoner. The following figure presents the key classes and properties (relations) of the EFBO ontology.

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/7482c524-9686-41f1-bccf-4a6f7078eafc)
**Figure:** EFBO Classes and Properties. On the left, we have the logical is-a hierarchy of the EFBO classes. On the right, we display the relational properties of the ontology.

The EFBO classes under the `System Entity` correspond to a set of conceptual entities that are required to describe an event-based system. A system's functional behavior cannot be reasoned without specifying the logical axioms of these
entities. In EFBO, the system entities are classified into four mutually disjoint classes called the `Agent`, `Event`, `Interface`, and the `Functionality`.

**Agent:** The class `Agent` represents a set of system entities that interact with a set of interfaces of the system. To be an instance of the `Agent` class, it is necessary and sufficient for a system entity to interact with an `interface` through the `interactsWith` property.

**Event:** The class `Event` represents a set of entities that are the occurents of a system. The events, i.e., the instances of the class Event, therefore are atomic and do not travel through time. It is necessary for a system entity to have an interface through the `hasInterface` property for that entity to be an instance of the class `Event`.

**Activity:** The class `Activity` represents a set of actions that are performed by some agent. To be an instance of the class `Activity`, it is necessary and sufficient for an action entity to be connected to an agent entity through the `isPerformedBy` property. By definition, an activity must inherit all the properties of an action.

**Interface:** The class `Interface` represents a set of system entities that serve as a shared boundary between an agent and an event entity. It is necessary for an interface to be associated with an event through the `isInterfaceOf` property.

**Functionality:** A functionality of a system is a named entity that represents a set of activities of a system within an interval. A functionality `f` of a system can represent a single activity; i.e., `f = {a1}`, or a series of contiguous activities; i.e.,
`f = {a1, a2,..., an}`. The overall functionality of a system can be broken down into a set of named functionalities chosen by a human modeller. Each of the functionalities, in that case, must have a boundary that marks the beginning and the ending events associated with that functionality. Refer to the thesis document for a detaild understanding of the notion of functionality within the context of software systems.

The following figure provides the list of EFBO classes along with their logical expressions in pure DL syntax. The figure also includes the axioms for the remaining defined classes within the EFBO that represent specific types of agents and agent specific user interfaces.

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/157a792c-2895-42b7-bb53-a50c1ad90f21)
**Figure:** The EFBO Class Expressions in Pure DL.

The following figure illustrates different properties among the EFBO classes that reflect the relationships formed by different classes. The dotted arrows represent different inferred properties based on the definitions of the EFBO core classes. 

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/1b9ccc6a-f12c-4d19-9aa1-698d80b02e3b)
**Figure:** EFBO properties among its core classes. 

## The EFBO Functional Reasoning Category (EFBO-FRC) Ontology
The EFBO-Functional Reasoning Category (EFBO-FRC) includes the classes associated with different functional reasoning categories under the Entity Classifier Class of the core EFBO. The EFBO-FRC is an importable module for the EFBO core ontology and includes logical axioms to define its reasoning categories based on different EFBO core classes and properties. It should be noted that the EFBO-FRC does not contain any new properties for itself and simply reuses the properties from the EFBO core.

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/4ddc23b3-271f-4823-93f3-d0c2e04b57c7)
**Figure:** The EFBO Functional Reasoning Category (EFBO-FRC) Classes.

Closely based on the general reasoning categories in event calculus such as deductive, abductive, and inductive reasoning, we have included several functional reasoning categories for the systems that are modeled based on the EFBO representation. These categories are defined within this utility ontology called EFBO-FRC.


## The EFBO Functional Consistency Validation (EFBO-V) Ontology
To facilitate the validation process, we have developed this utility ontology called the EFBO Consistency Validation Ontology (EFBO-V). The EFBO-V imports the core EFBO along with the EFBO-FRC ontology and is designed to integrate and classify the functional entities of two given source models into a comparable representation. There are two interrelated categories of classes within the EFBO-V. First is the set of classes under the system validation entity and the second is the set of classes under the functional reasoning category of the EFBO-FRC ontology.

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/3d08ae7e-063d-4d33-9f6a-ea887949daff)

**Figure:** The classes under the System Validation Entity and the properties of the EFBO Validation Ontology (EFBO-V).

The figure above presents the EFBO-V classes under the System Validation Entity along with the properties of the EFBO-V ontology. The classes in the  figure are self-descriptive and are used to classify different kinds of entities based on their source systems. Directly under the System Validation Entity, we have four kinds of classes as follows: Consistent Entity, Inconsistent Entity, Participant Entity, and Participant System. The rerst two of the latter classes are used to classify the entities based on a set of consistency validation rules that we are going to describe in the next section. The rest of the classes are there to classify the set of individuals under the core EFBO classes; i.e., the Event, Agent, and Interface classes, for each of the participating systems.

