# REST

REST is a set of conventions and practices in web development that deals with accessing + manipulating **resources over HTTP**.

Resources can be abstraction of object or data

IN PRACTICE - resources referred to using **URL** (Uniform Resource Locator)

## CRUD --> BREAD

CRUD - Create, Read, Update, Delete

In REST, reading is split into two:
  1. accessing whole collection (search or browse)
  2. accessing single member of that collection 

  so REST is BREAD - Browse, Read, Edit, Add, Delete


| Action | Application | Description                        | HTTP Method |
|:-------|:------------|:-----------------------------------|:------------|
| Browse | collection  | browse the collection	            | GET         |
| Read	 | member	     | read a member of the collection    | GET         |
| Edit	 | member	     | edit a member of the collection    | PUT / PATCH |
| Add	   | collection  | add a new member to the collection | POST        |
| Delete | member	     | delete a member of the collection  | DELETE      |


## Resource Identifier

name for a resource must be chosen

typically name of object type (plural, lowercase, words seperated using - )
- member of collection indicted by their unique identifier

For example:
- resource collection  --> /users
- member of collection --> /users/1 (1 here is id = unique identifier)

## Representation

When resource is transferred (HTTP response), can be **any format** but should take into account `Accept` header

`Accept` indicates **format**. For example
- `Accept: text/html`
- `Accept: application/json`