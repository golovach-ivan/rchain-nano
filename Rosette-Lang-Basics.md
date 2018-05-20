# Rosette Lang Basics

## Types

### Primitive Types (Constants), Basic constants
> Constants are actors that always have the same behavior.

#### Boolean 

##### Boolean Literal

##### Boolean Operations

#### Character

#### Fixnum

#### Float

#### #absent
> #absent, which is used to indicate that no value is present

#### #eof
>  #eof which is used to signal that the end of a stream has been reached

#### #niv
> #niv (no-intrinsic-value), which is used when no other value is appropriate

### Compount Constants

#### String

#### Tuple
> Tuples are used to represent messages that convey information between two actors in a communication, to introduce sub-structure in messages, and as a primitive data structure in the definition of other actors. The first form above permits 0 or more actors to be packaged up in a tuple. The second form requires that the expression following the & must evaluate to a tuple, and the resulting tuple is the concatenation of the preceding actors and the tuple actor resulting from the last expression:\
> \[3 2 \[1 2 3]]   ⇒ \[3 2 \[1 2 3]]\
> \[3 2 & \[1 2 3]] ⇒ \[3 2 1 2 3]

#### Expression Literal

## Operations
> An operation is an Actor that determines the protocol for finding a method to perform some request or command. The concept of operations as defined in Rosette is similar to that of generic functions in CLOS \[Gabriel et al. 1988]. A message is sent to an operation and the operation determines the next step in getting the work accomplished. Rosette provides a number of built-in operations called primitives that implement basic behaviors on the entities in the initial environment. For example, consider (+ 3 4), the + is an operation that determines what action to take based on the arguments sent to it in the message. In this case, there are two Fixnums and the operation selects the Fixnum addition primitive.

### Operations: Oprn

### Operations: SyncOprn

## Constructs

### Simple Constructs

#### block

#### free

#### goto

#### if

#### label

#### let

#### let*

#### letrec

#### method

#### proc

#### send

#### seq

#### set!

### Compound Constructs / Macro

#### and

#### become

#### break

#### cond

#### dec

#### define

#### defActor

#### defExpander

#### defOprn

#### defMethod

#### defProc

#### defPure

#### defSlot

#### defSlots

#### defSync

#### defValue

#### do

#### do*

#### inc

#### iterate

#### local

#### m!

#### next

#### not

#### method

#### or

#### proc

#### pure

#### set

#### slot

#### super

#### update

#### value

#### void

#### s!
