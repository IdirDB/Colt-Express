## Introduction

This programming project aims to create a computerized and slightly simplified version of the game Colt Express.

<p align="center">
<img src="https://github.com/IdirDB/Colt-Express/assets/169926706/0d672e68-3052-4974-83a9-248aea6d7d1c" alt="Accueil style="width: 40%;">
</p>  

## Overview of the game rules

The game takes place aboard a train, consisting of a locomotive and a certain number of carriages. The players take on the roles of bandits who jump on board to rob the passengers.

**Objective:** to collect as much loot as possible, every man for himself. This is a programming game, in which players alternate between two phases:

*Planning:* each player secretly decides on a certain number of actions that their character performs in order.

*Action:* all the first actions are carried out, then all the second actions, and so on until the end.

<p align="center">
  <img src="https://github.com/IdirDB/Colt-Express/assets/169926706/0b0fc29d-48ff-4ef3-9a1b-ee578431cd15" alt="Colt Express">
</p>

## Bandit Actions and Loot

Bandits can be in the carriages or the locomotive, and for each of these elements, either inside or on the roof. In this document, by convention, the term "carriage" refers to any element of the train, which can include the locomotive. The possible actions for the bandits are:
- Move from one carriage to another, either forward or backward, while staying on the same level.
- Go inside or climb onto the roof of their current carriage.
- Rob a passenger to collect loot (or simply collect loot that has been abandoned there).
- Shoot at another nearby bandit to make them drop their loot.

The recoverable loot aboard the train includes:
- Pouches worth between 0$ and 500$, found with the passengers inside the carriages.
- Jewelry worth 500$, found with the passengers inside the carriages.
- A stash worth 1000$, inside the locomotive, guarded by the Marshal.

A Marshal is present on board the train and can move between the locomotive and the carriages, always staying inside. He shoots at any bandits in the same position as him and forces them to retreat to the roof.

<p align="center">
  <img src="https://github.com/IdirDB/Colt-Express/assets/169926706/b2c28c5e-e177-45b7-9992-e82ecde7cd09" alt="Colt Express" style="width: 45%;">
  <img src="https://github.com/IdirDB/Colt-Express/assets/169926706/584463da-3522-4124-82f6-7a5843338235" alt="Colt" style="width: 45%;">
</p>

## Organization
The application is organized according to a Model-View-Controller (MVC) architecture.

## Observer and Observable
To ensure effective interaction between our model and the view, we integrate the Observer and Observable pattern. This mechanism allows the view to automatically react to changes in the model, facilitating real-time updates without direct interactions. When changes occur in the model, such as updating character positions or changes in loot inventory, the model notifies the view through the Observer system, which reacts by updating the relevant visual elements.

## Tests with JUnit
We set up unit tests with JUnit to ensure the proper functioning of our application. These tests cover various aspects of the game, including player action logic, interactions between different game elements, and the model-to-view notification mechanisms. This approach allows us to effectively detect and correct bugs throughout the development process.

## Contributors
- Idir DJOUAB
- Zineddine Kermadj

## Thanks
- My project supervisor David Rei
- My software engineering professor Frédéric Gruau
- Durga Software Solutions
