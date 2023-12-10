# The EFBO Ontology Repository
This repository contains three ontology files relevant to the Event-Based Functional Behaviour Ontology (EFBO) project as part of a Software Engineering thesis.

## The EFBO-Core Ontology
The Event-Based Functional Behavior Ontology (EFBO) is an ontology to represent the functional behavior of event-based systems. The ontology provides logical descriptions of the core concepts associated with event-based systems. Based on the understanding of functional reasoning, the notion of affordances, and the notion of action, events, and change in commonsense reasoning the ontology can effectively represent the functional behavior of event-based systems. The ontology-based representation that we have developed promotes an enhanced comprehension and control over the following defining aspects of the event-based systems.
* **Allowable set of events**: What is the set of events that exist for an application system and how to represent them?
* **Allowable flow of events**: How to represent the partial order restrictions on the allowable set of events?
* **Event locations and interfaces**: How to describe the system in terms of its events and their associated interfaces?
* **Allowable event-interface-agent interactions**: How to represent the interactions between the agents, interfaces, and the events of the system?

The EFBO is written in OWL-DL formalism and we have verified its consistency using the HermiT reasoner. The following figure presents the key classes and properties (relations) of the EFBO ontology.

![image](https://github.com/smtifahim/EFBO-Ontology-Repository/assets/13155192/7482c524-9686-41f1-bccf-4a6f7078eafc)
**Figure:** EFBO Classes and Properties. On the left of the figure, we have the logical is-a hierarchy of the EFBO classes. On the right, we display the relational properties of the ontology.

## The EFBO Functional Reasoning Category (EFBO-FRC) Ontology
The EFBO-Functional Reasoning Category (EFBO-FRC) includes the classes associated with different functional reasoning categories under the Entity Classifier Class of the core EFBO. The EFBO-FRC is an importable module for the EFBO core ontology and includes logical axioms to define its reasoning categories based on different EFBO core classes and properties. It should be noted that the EFBO-FRC does not contain any new properties for itself and simply reuses the properties form the EFBO core.

## The EFBO Consistency Validation (EFBO-V) Ontology
To facilitate the validation process, we have developed this utility ontology called the EFBO Consistency Validation Ontology (EFBO-V). The EFBO-V imports the core EFBO along with the EFBO-FRC ontology and is designed to integrate and classify the functional entities of two given source models into a comparable representation.
