# An Additional 100 Ideas for Computing

# 1. Personal file archives

My personal files inevitably leads to lots of small files which take forever to copy and are transferred very slowly by my hardware when copied. I propose a personal file manager which handles archiving for our files by letting us "log into" our files by unpacking them to fast media and lets us "repack" the files back up when we logout of the file manager.

# 2. Idea management software

Society is composed of ideas, let's let everyone track the ideas they like.

# 3. Pick up and drop

Drag and drop is too hard. What about picking an item up and then dropping it. There would be no need to click and hold the mouse.

# 4. Chronological news

Each news topic should be tracked separately, I should be able to follow a news stream from beginning to end on a topic.

# 5. Permanent software / Software subscriptions

# 6. Contiguous disk layouter

A program that reads your startup configuration and then lays out files on disk so everything is contiguous. So a simple program can be written to read all the files into the disk cache on startup and every read afterwards is instant.

# 7. Automated API traversal

Imagine an API as a graph and define a traversal of the API to get what you want. In other words, the types between API methods should be inferred. Imagine I want to backup my files and I want to deduplicate them, compress them and encrypt them and upload them. Each of these steps takes a type. The formation of the circuit can be automatic if the types are well defined, it's a search through a graph.

# 8. Server server

Creating a performant server is difficult. The lessons from Nginx and Apache and pretty much every REST framework or mail server or IRC server or server runner such as gunicorn could be taken and combined into a generic server. This server would be super performant.

# 9. Query for data structure

If you're writing a compiler or programming language or business software you have a stored shape of data and relationships.

Sometimes to solve particular problems you need data in a particular shape.

What if you had a query language where you could retrieve a data structure?

In compiled languages we have pointers and in interpreted languages such as Python and Java we have references between objects which are like pointers.

We also have indexing Data structures such as hashmaps and btrees. What if we could built up data structures by a query?

We want a btree indexing these columns and these relations.

# 10. Access pattern serialization

A format or data structure that represents an access pattern for data.

Our data access patterns determine how efficient our queries shall be.

 * Can be used to generate data structures.
 * Would be useful for designing NoSQL and Dynamodb keyspaces. 
 * Can generate SQL tables.
 * Can be used for generating sharding.
 * Can be used to parallelize queries.
 * Can be used for query planning.

This could be used for [ideas3 17. Query database](https://github.com/samsquire/ideas3#17-query-database) and [9. Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure).

# Generating ideas

 * marketplace
 * schedule
 * tree
 * additive/combined
 * auto
 * mesh
 * hooks
* Pattern matching

# Incomplete thoughts and ideas 

Scope magic

Tree programming
Fluent system
Flow control

Things written as communication protocols are easier to program and reason about. Concurrency too (see go and occam pi)
Turn the GUI into a communication problem.
