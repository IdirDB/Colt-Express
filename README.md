## Introduction

This programming project aims to create a computerized and slightly simplified version of the game Colt Express.

## Overview of the game rules

The game takes place aboard a train, consisting of a locomotive and a certain number of carriages. The players take on the roles of bandits who jump on board to rob the passengers.

**Objective:** to collect as much loot as possible, every man for himself. This is a programming game, in which players alternate between two phases:

*Planning:* each player secretly decides on a certain number of actions that their character performs in order.

*Action:* all the first actions are carried out, then all the second actions, and so on until the end.

## Bandit Actions and Loot

Bandits can be in the carriages or the locomotive, and for each of these elements, either inside or on the roof. In this document, by convention, the term "carriage" refers to any element of the train, which can include the locomotive. The possible actions for the bandits are:
- Move from one carriage to another, either forward or backward, while staying on the same level.
- Go inside or climb onto the roof of their current carriage.
- Rob a passenger to collect loot (or simply collect loot that has been abandoned there).
- Shoot at another nearby bandit to make them drop their loot.

The recoverable loot aboard the train includes:
- Pouches worth between $0 and $500, found with the passengers inside the carriages.
- Jewelry worth $500, found with the passengers inside the carriages.
- A stash worth $1000, inside the locomotive, guarded by the Marshal.

A Marshal is present on board the train and can move between the locomotive and the carriages, always staying inside. He shoots at any bandits in the same position as him and forces them to retreat to the roof.

## Organization

The application is organized according to a Model-View-Controller (MVC) architecture.
## Observer and Observable

To ensure effective interaction between our model and the view, we integrate the Observer and Observable pattern. This mechanism allows the view to automatically react to changes in the model, facilitating real-time updates without direct interactions. When changes occur in the model, such as updating character positions or changes in loot inventory, the model notifies the view through the Observer system, which reacts by updating the relevant visual elements.
## Tests with JUnit

We set up unit tests with JUnit to ensure the proper functioning of our application. These tests cover various aspects of the game, including player action logic, interactions between different game elements, and the model-to-view notification mechanisms. This approach allows us to effectively detect and correct bugs throughout the development process.
