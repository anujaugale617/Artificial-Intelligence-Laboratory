# Assignment 1: Design and Implement a Simple Reflex Agent for the Vacuum Cleaner World

## Aim

To design and implement a **Simple Reflex Agent** for the Vacuum Cleaner World and analyze its rational behavior in a given environment.

---

# Theory

## Introduction to Artificial Intelligence (AI)

Artificial Intelligence (AI) is a branch of computer science that enables machines to perform tasks that normally require human intelligence, such as learning, reasoning, problem-solving, and decision-making.

An **AI Agent** is a system that **perceives its environment through sensors and acts upon the environment using actuators** to achieve a specific goal.

---

## What is an Intelligent Agent?

An **Intelligent Agent** is an entity that:

* Observes the environment.
* Takes decisions based on the observations.
* Performs actions to achieve the desired goal.

### Components of an Agent

* **Sensors:** Used to collect information from the environment.
* **Actuators:** Used to perform actions in the environment.

---

## Simple Reflex Agent

A **Simple Reflex Agent** selects an action based only on the **current percept (current state)** without considering previous states or future consequences.

It follows predefined **condition-action rules**.

### Rule Format

```
IF condition THEN action
```

Example:

```
IF current room is Dirty
    THEN Clean
ELSE
    Move to the next room
```

---

## Vacuum Cleaner World

The **Vacuum Cleaner World** is one of the simplest AI environments used to understand intelligent agents.

### Environment

The environment contains:

* Two rooms (A and B)
* Each room can be:

  * Clean
  * Dirty
* A vacuum cleaner that can move between the rooms.

---

## Actions Performed by the Agent

The vacuum cleaner can perform the following actions:

* **Suck** → Cleans the current room.
* **Left** → Moves to the left room.
* **Right** → Moves to the right room.

---

## Working of the Simple Reflex Agent

The agent repeatedly follows these steps:

1. Check the current room.
2. If the room is dirty:

   * Perform **Suck**.
3. Otherwise:

   * Move to the other room.
4. Repeat until all rooms become clean.

---

## Algorithm

1. Start.
2. Observe the current location.
3. Check whether the room is dirty.
4. If dirty:

   * Clean the room.
5. Else:

   * Move to the adjacent room.
6. Repeat until all rooms are clean.
7. Stop.


---

## Applications

* Robot vacuum cleaners.
* Automatic cleaning robots.
* Simple game AI.
* Basic industrial automation systems.

---

## Conclusion

The **Simple Reflex Agent** successfully cleans the Vacuum Cleaner World by following predefined condition-action rules. It behaves **rationally** by cleaning a dirty room immediately and moving only when the current room is clean. Although it works well in simple environments, it is not suitable for complex environments because it has no memory or planning capability.

---

### Viva Questions

1. What is an AI agent?
2. What is a Simple Reflex Agent?
3. What is the Vacuum Cleaner World?
4. What actions can a vacuum cleaner agent perform?
5. What is meant by rational behavior?
6. What are condition-action rules?
7. What are the limitations of a Simple Reflex Agent?
8. Why is the Vacuum Cleaner World used in AI?
9. What are sensors and actuators?
10. Give one real-life application of a Simple Reflex Agent.

