# The EFBO-Core Ontology
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
