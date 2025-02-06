# java-nodes

## Challenge

The data tree structure is a way to organize and store data in a hierarchical
form. It is composed of nodes each connected by lines/edges. A parent node is a
node connected to another node downline. The downline node is called a child
node. A child node can have its children. A node with no children is called a
leaf node. The root node is the topmost node and it doesn't have any parent.
Each child node can only be a child of one parent node.

```mermaid
flowchart TD
 A --> B
 A --> C
 A --> D
 B --> E
 B --> F
 B --> G
 B --> H
 D --> I
 D --> L
 D --> M
 I --> J
 J --> K
 M --> N
```

Please create a restful API service (no UI) for the node management system. It
should have the following functionalities:

1. Add nodes
    * Given a node, the user should be able to add a child to that node
2. Delete nodes
    * Given a node, the user should be able to delete a child of that node
3. move nodes from one parent to another
    * Given a node, a user should be able to transfer it to a different parent.
4. return the list of all downline nodes. For example, in the structure above,
    * Given a user invoked the endpoint to get the child nodes of A, the
      response will be `[B, C, D, E, F, G, H, I, J, K, L, M, N]`
    * Given a user invoked the endpoint to get the child nodes of D, the
      response will be `[I, J, K, L, M, N]`
    * Given a user invoked the endpoint to get the child nodes of C, the
      response will be `[ ]`

The application can start with a pre-defined root node.

## Requirements

* Please use
  * springboot, latest version
  * Java 17 or later versions
  * any RDBMS or no SQL database
  * maven or gradle
* Append to this file how to `run`/`use`/`test` your app. If your app can
 host or include a generated **how to use my web service** it would be cool but
 not required
* Apply REST best practices in terms of endpoint design, proper status
 xheaders for the operations, correct use of HTTP Verbs, content negotiation
 and entity representation.
* Support JSON and xml as content-type

## Submission

Deadline, 5 days after receiving the invitation
