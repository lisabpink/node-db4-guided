# Data Modeling Notes

## Requirements

A client has hired you to build an API for managing `zoos` and the `animals` kept at each `zoo`. The API will be used for `zoos` in the _United States of America_, no need to worry about addresses in other countries.

For the `zoos` the client wants to record:

- name.
- address.

For the `animals` the client wants to record:

- name.
- species.
- list of all the zoos where they have resided.

Determine the database tables necessary to track this information.
Label any relationships between table.

## A good data model

- captures ALL the information the system needs.
- captures ONLY the information the system needs.
- reflect reality (from the point of view of the system). Need model that accomodates problem, not unesscary information.
- is flexible, can evolve with the system.
- guarantees 'data integrity', without sacrificing too much performance.
- is driven by the way we access data.

## Components

- entities (nouns: zoo, animal, species), like a resource ---> tables.
- properties ---> columns or fields.
- relationships ---> foreign keys.

## Workflow

- identify entities
- identify the properties
- identify relationships

## Relationships

- one to one
- one to many: this is the most common!
- many to many

_one species has many animals_

_there can be many animals in a zoo_
_an animal could have lived in many zoos_

## Mantras

- every table must have a **Primary Key**
- work on **two or three** entities at a time.
- **one to many** relationships are modeled using a **Foreign Key**.
- the Foreign Key always goes in the **many** side.
- the Foreign Key column must be the **same type** as the Primary Key it references. Ex. if string must be string
- in a **many to many** relationships are modeled using a **thrid table**
- the thrid table could include other columns