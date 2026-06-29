# Collaborative Text Editor

Real-time multi-user text editor using CRDT (Conflict-free Replicated Data Types), built as part of Advanced Programming Techniques at Cairo University.

## What it does
Multiple users edit the same document simultaneously without conflicts. CRDT guarantees all peers converge to the same document state regardless of operation order — no central coordination needed.

## How it works
- Each character is a tree node with a unique ID (UserID + logical clock)
- Deletions use tombstones — nodes are marked deleted, never removed
- DFS traversal reconstructs the document text
- Concurrent inserts at the same position resolved deterministically by timestamp then UserID

## Tech Stack
Java · CRDT (character + block level)

## How to Run
1. Open in IntelliJ IDEA
2. Run `Main.java`

## Team
4-person team at Cairo University. I contributed across CRDT implementation, operations, and integration.
