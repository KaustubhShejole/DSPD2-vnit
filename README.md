# Train Reservation Management System

---
Author: Kaustubh Shivshankar Shejole
---


This project implements a train reservation management system with two variants:

* **Assignment 1:** Records stored in a **linked list** of structures
* **Assignment 2:** Records stored in a **tree-based** data structure

Each node represents a passenger record.

## Data Fields

Each passenger node contains:

* Passenger name
* Passenger ID (unique key)
* Boarding train
* Boarding station
* Travelling class (Sleeper / 3AC / 2AC / 1AC)
* Destination station
* Train ID
* Seat number (automatically assigned: bogie + seat)
* Optional: confirmation for class upgrade
* Any additional useful passenger information

All records must remain **sorted by Train ID**, so passengers on the same train appear together.

## Assumptions

You may assume:

* Number of bogies per class
* Number of seats per bogie
* Seat allocation must keep passengers from the same request as close together as possible

## Functions to Implement

### 1. `insert`

* Input: List of passengers and their reservation request
* Output:

  * Reservation successful
  * Partially successful
  * Reservation failed
* Seats for passengers in the same request must be:

  * Allocated together if possible
  * If not, placed as close as possible

### 2. `delete`

* Input: Passenger ID
* Output:

  * Cancellation success message
  * Cancellation failure message

### 3. `getListDestination`

* Retrieve all passengers with the **same destination station** and **same train ID**.

### 4. `SortByTravelDate`

* Input: Passenger ID
* Output: List of destination stations for that passenger, sorted by travel date

### 5. `SortTrains`

* Input: The entire train database
* Output: Train numbers and travel dates sorted by **number of passengers** on each train

### 6. `PromotePassengers`

* Input: Train ID and travel date
* Output: Promote passengers to the next travel class when seats are available
* Rules:

  * Promotion order follows booking order
  * Classes promote in sequence: Sleeper → 3AC → 2AC → 1AC
  * If a higher-class passenger is promoted, their previous seat becomes available for lower-class promotions

---

This system models realistic railway reservation behaviour using linked lists or tree structures, with constraints on seat allocation, passenger grouping, sorting, and class upgrade logic.
