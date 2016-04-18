# Entities

All entities include the following fields

Field | Spec
----- | ----
id | int
created | datetime
updated | datetime
description | string 80


## Asset

### Relationships

Related To | Type | Comment
---------- | ---- | -------
Asset | *-1 | Parent Asset
Class | *-1 | 
Location | *-1 | Parent Location
Position | *-1 | Parent Position
Type | *-1 | 

### Fields

Field | Spec
----- | ----
model | string 80
serial | string 80


## Class

### Relationships

Related To | Type | Comment
---------- | ---- | -------
Class | *-1 | Parent class

### Fields

Field | Spec
----- | ----
type | {asset, ...}


## Employee

### Relationships

Related To | Type | Comment
---------- | ---- | -------
Employee | *-1 | Reporting to
User | 1-1 | Associated user account

### Fields

Field | Spec
----- | ----
hr_no | string 80


## Group

### Relationships

Related To | Type | Comment
---------- | ---- | -------
User | 1-* | User group

### Fields

Field | Spec
----- | ----
is_enabled | bool


## Location

Same as Asset, except no fields


## Organization

### Relationships

Related To | Type | Comment
---------- | ---- | -------

### Fields

Field | Spec
----- | ----


## Position

Same as Asset, except no fields


## Role

### Relationships

Related To | Type | Comment
---------- | ---- | -------

### Fields

Field | Spec
----- | ----


## Status

### Relationships

Related To | Type | Comment
---------- | ---- | -------

### Fields

Field | Spec
----- | ----
syscode | string 8
type | {asset, ...}


## Type

### Relationships

Related To | Type | Comment
---------- | ---- | -------
Asset | 1-* | Parent class

### Fields

Field | Spec
----- | ----
type | {asset, ...}


## User

### Relationships

Related To | Type | Comment
---------- | ---- | -------
Employee | 1-1 | Associated employee
Group | *-* | User group

### Fields

Field | Spec
----- | ----

