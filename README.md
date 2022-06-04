# An Additional 100 Ideas for Computing

Welcome to the forth page of my Ideas for Computing.

This issue is heavily focused on data structures and algorithms so you might need to be familiar with algorithms and programming to understand these ideas.

There is probably a masters or PhD idea in here somewhere!

 * See [100 Ideas for Computing](HTTPS://GitHub.com/samsquire/ideas), the first issue of this series.
 * See [ideas2, Another 85+ Ideas For Computing](HTTPS://GitHub.com/samsquire/ideas2)
 * See [ideas3, An Extra 100 Ideas for Computing](HTTPS://GitHub.com/samsquire/ideas3)
 * [Follow me on Twitter](HTTPS://twitter.com/mrsamuelsquire)

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.


Thank you to all the contributors who have been sending in examples and corrections!


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

In compiled languages we have pointers and in interpreted languages such as Python and Java we have references between objects which are similar to pointers.

We also have indexing Data structures such as hashmaps and btrees. What if we could built up data structures by a query?

We want a btree indexing these columns and these relations.

GraphQL is nearest to this idea. I want a linked list of this data or an object graph that looks like this.

Can define an algebra that works with nested collections and has a primitive called associate which associates data of a source collection with another structure.

# 10. Access pattern serialization

A format or data structure that represents an access pattern for data.

For example, if you're going to be scanning items in sorted order, if you need to get data by a composite or single key, these are part of your access patterns.

If you always fetch the children relations of a piece of data, you should serialise that and represent it.

Our data access patterns determine how efficient our queries shall be.

 * Can be used to generate data structures.
 * Would be useful for designing NoSQL and Dynamodb keyspaces. 
 * Can generate SQL tables.
 * Can be used for generating sharding.
 * Can be used to parallelize queries.
 * Can be used for query planning.
 * Can be used to denormalise queries.

This could be used for implementing [ideas3 17. Query database](https://github.com/samsquire/ideas3#17-query-database) and [9. Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure).

# 11. Dream desktop

My computer should try benefit my life as much as possible. Modern desktops don’t even try. They don’t learn about me or give me advice. I want to give my demographics to my computer, my location, my salary and have the computer calculate things about me. We have all this untapped computer resource but most people only idle their computers.
Here are some ideas that desktop computers could do.

 * **Many remote indexes** – We’ve got spare resources on an average desktop. Synchronize my files with a remote server, then do some crazy indexes on the files for all sorts of combinations. Index my files contents for content based searches. It doesn’t matter if the indexing is expensive, because it’s on a different server.

 * **Arbitrary Correlations** It’s easy to arbitrarily correlate behaviours of humans on a computer. We can track what times the user opens certain programs and then open them automatically at the correlated time.

 * **Information age worker** Download various data sets to the desktop and allow users to run queries against the data. Would be nice if you could import Wikidata data this way.

 * **Digital Shop** Provide tools to view or start an online shop, including a product search engine.

 * **Overlay network** My desktop should form an overlay network with all my phones and servers so that I can share services privately. It should connect as part of login to the computer. Should be like Zerotier, but with automatic login and connection.

 * **Social P2P network** My desktop should connect to a federated social network, a bit like twitter where you can share things. I can create mockups for an app in my desktop environment and share it.

* **Program cross-referencer** We often run multiple applications in parallel and even arrange them so we can see both of them at the same time. What if you could write queries to open applications to combine data across two applications? Or write simple loops over Spreadsheet data and interact with the browser with an API? I should be able to write joins across programs visually.

* **Display Cone** It would be nice if one could control the window manager and compositing with a text API. So one could create convert a window into a custom geometry and display that. So one could create dashboards of existing programs. This would be useful for information radiators without having to run Xmonad or other tiling window manager.

* **Payments integration** Support payments and the listing of digital services in an online marketplace. We need to democratize the act of taking money and exchanging it. It shouldn’t be the purview of large corporations only taking payments. Anybody should be able to take a payment.

 * **Website management** Run a web site with your desktop computer. Desktop acts like a VPS, with dynamic IP hosting, web server and database.

* **Object maker** Describe the properties an object should have and have them stored in a collection. Write queries to retrieve them, sort them. Drag and drop text boxes, sliders etc to create a GUI.

 * **Live tree and rich GUI editor** Every window, widget, dialogue, GUI on the screen forms part of a global tree data structure which can be used to interrogate what is on the screen and automate behaviour. Think of it as a global document object model (DOM) for the desktop but is actually a scenegraph. So every widget is accounted for. Someone can copy and paste a tree branch an create an identical but separated GUI from the root and modify it with drag and drop.

 * **Life strategy quiz** Ask where you’re sleeping tonight. What you doing for food. With the ability to order food via the system or acquire accommodation with a search. When the user answers they have no food or no where to sleep, dispense information to counteract homelessness and other social problems.

 * **CPU manuals** The desktop should come with documentation about CPU instructions, a compiler, and documentation about the desktop environment. It should be possible to create apps from an installation with minimal expertise.

 * **API suite** The desktop should have an installable set of pluggable APIs that are really easy to use from different places: from programming languages, over the network and from an executor GUI. I should be able to create an API invocation and chain them together with a GUI.

 * **Event maker** The ability to view events that get fired by the desktop environment, from the network stack, from arbitrary applications and add behaviour to events. A way to hook into events over the network, so you can ‘subscribe’ to events on another machine.

 * **Log aggregation** Log errors and error dialogs to be automatically synced to the cloud where other they turn into community issues. Issues can be commented by other users.

 * **Errors become things** Errors become a thing in my desktop. They appear in the system tray and don’t go away so easily and they can be re-tried easily. They appear in an error viewer. You can then try solutions against the error to see if it works, it it works, the error will go away. You can see comments about the error and try known solutions to the error. Known solutions are gathered online.

 * **Shared desktop sessions** It should be possible for multiple users to join a desktop session. The session is not single player, reserved for one person but possible for multiple people to join the same session.

 * **Cloud designer** Advertise cloud features to me and let me use cloud features in my home network such as S3.

 * **Advertising features to me** My desktop computer has installed various services and APIs. My desktop should advertise what features are available to me

# 12. Work merging

When a user does something on a computer their patterns of work often match other people's patterns with the same general data structure. We can match trees or data structures that are visible on the screen with actions that were similar for other users and allow users to benefit from work that other people did.

For example, if you want to change your address with a company, this request looks the same to everyone. Everyone's address can be changed with one operation to change multiple individuals addresses in one operation.

If someone is looping manually down a spreadsheet pasting into an intranet webpage, we can represent the operations that the user is doing as events and pattern match the events to look for +1 or -1 operations on data. The computer can detect the repetition and carry out the action on the user's behalf: a smart macro recorder and replayer.

# 13. Window walk optimisation

Imagine you want to find a job that is near your home transport wise, near a supermarket, doctors and that pays the most and has the cheapest house to buy or rent.

You could open a browser for each of these queries but it's difficult to optimise these multiple queries manually.

Or you want to book a holiday or organise the purchasing for an office. Or equip a datacentre with hardware.

We can walk different web sites in an iterative hill climbing algorithm.

 * Enumerate list of towns, cities and villages

 * Enumerate houses to rent and to buy at lowest cost sorted first.

 * Enumerate list of supermarkets near said houses and near job, sort by smallest range.

 * Enumerate public transport options

 * Enumerate jobs, sorted by most pay first

Now walk all these datasets as an optimisation problem to find a list of efficient combinations of jobs, supermarkets, transport and housing.

This is far better than manually cross referencing data in separate tabs.

I think the walking of data can be distributed for efficiency. It doesn't make sense to walk each record one at a time. It's a lot of data to download.

I think a continuation style can be used so that the provider of the data walks each sub iteration.

So the walking of data is continuations between collaborating servers.

# 14. Data scheduling and infinite tape abstraction

I read somewhere that instruction selection is less of a cause of total performance of code compared with data layout. With data driven architecture we can use arrays of structures or structures of arrays for performance.

Much of modern programming is managing different buckets of data and scheduling them into memory for example we have heap, the stack, S3, disk files. We need some method of paging this data and scheduling data to and from each area efficiently.

Databases such as Postgres have heap managers. Virtual memory exists in kernels. Some software use arenas for memory management. There is all sorts of clever things that can be done with readahead and prefetching and amortization. The problems of chunking has wife ranging impacts to do with caching and decision to load in parallel.

Surely these problems could be solved once in a profoundly effective way and exposed as a library.

I also want to write my code the same way that scales for a 100 kilobyte file as a 10000 petabyte datastore. The approach I use should be scalable. The system can act as if memory is infinite but it's not, it's simply paged in efficiently from S3 or disk efficiently 

I imagine this being implemented as a Policy that defines the relationship hierarchy and speeds of each kind of media and the policy of when to page between them.

You could have a common API for storage that works across all levels of storage.

This could be combined with [10. Access pattern serialization](https://github.com/samsquire/ideas4/blob/main/README.md#10-access-pattern-serialization) and [9. Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure).

# 15. Mega tree

I want a mega tree data structure which has the combination of these properties:

 * Can be merged as a Conflict free Replicated Data Type (CRDT)
 * Uses the Left Right concurrency pattern for each leaf and internal node
 * Can be used as a merkle tree
 * Can be a persistent tree
 * Can act as a TreeMap
 * Can act as a prefix trie.
 * [Can be append only](http://www.bzero.se/ldapd/btree.html)

I started work on this. I've implemented a radix tree, a Left right HashMap, prefix tree and a merkle tree. I need to combine them together.

# 16. Use A* for data query generation

If I put some data into a data structure - is the computer clever enough to generate solutions that get nearer to accessing it?

If I train a computer on binary search, btree and hashing functions and create graph traversals that represent the algorithms.

If I have a keyspace that is lexicographically sorted or a HashMap or btree can a computer study an algorithm and turn it into a graph traversal and generalise the approach?

Could I generate sequences of instructions as graph traversals that become generalised algorithms that fetch data?

We know where the data is in the data structure.

There is a sequence of steps and iteration to get the query to fetch the data.

For a tree we know which nodes we have to traverse in order to get to the data, so we can generate code that knows how to fetch children recursively and do a binary search on an array.

If we want to fetch data that matches a predicate, we could create a graph traversal of the indexing functions, we can in effect trial indexing functions to see if they cheapen the retrieval process.

The pattern to iterating down a tree could be inferred.

The distance function is fairly straightforward if there is a path from the current data item being evaluated or searched then the system is nearer to the goal data.

# 17. Core algorithms should be written in a simple to understand language

The algorithms we depend on day-to-day should be written in a simple programming language with very little barrier to entry. I suggest things like the cost based optimiser, browser internals, databases, query optimisers and the operating system scheduler be written in languages like Python and lowered to C programming language.

Why? Memory management and low level implementation details in impoverished environments matter less than the overall "what gets done and why".

If compilers and optimisers were written in Python you would have more people be capable of supporting your project.

As it stands to add code to these projects you need to be seriously skilled in low level programming 

# 18. Data structure synchronization

Data structures often leads to denormalisation for performance. We need to keep data synchronized for performance and parallelism.

If I use [Rockset Converged Indexing](https://rockset.com/blog/converged-indexing-the-secret-sauce-behind-rocksets-fast-queries/) and index by column, value and row I need to store data three times which is storage costly but efficient in terms of retrieval. I need some process to keep the data synchronized.

I propose a simple system that tracks all instances of data and keeps them integrated. This would be used between systems and keep then in sync. It would also be used within an application server or database architecture. It would also have the feature to delay updating items before returning success. So indexes can be updated passively of even asynchronously.

# 19. Merge database

A distributed database that uses CRDTs to replicate and resolves concurrent edits with Myers algorithm for String Edit Sequence edit scripts.

Essentially combine CRDT technology with diff technology so merges are always seamless.

Assume there are two edits to the database and they both have previous versions A and B, find the common ancestor version of A and B which is S. Then diff3 can be used in a three way merge repeatedly between all versions from S to A and B.

You can see my implementation of diff3 and three way merge in my [text-diff repository](https://github.com/samsquire/text-diff). I implemented MerkleClocks in [merkle-crdt repository](https://github.com/samsquire/merkle-crdt). I would like to implement seamless merge in my applications.

```
def diff3(a, b):
  a_history = get_history(a)
  print(a_history)
  b_history = get_history(b)
  print(b_history)
  S = common_ancestor(a_history, b_history)
  print("common ancestor", S)
  left_sequence = versions_from(S, a_history)
  right_sequence = versions_from(S, b_history)
  last_left = S
  last_right = S
  for left, right in zip_longest(left_sequence, right_sequence):
    if left:
      
      last_left = merge_diffs(last_left, left.text, right.text)
    if right:
      
      last_right = merge_diffs(last_right, left.text, right.text)
      
  merged = merge_diffs(last_left, last_left.text, last_right.text)

  
  return merged

```

# 20. Lazy arrange or invariant maintenance

Many computer problems and algorithms can be solved with a sorting function and a set of statements that should be maintained over collections of objects.

Unfortunately to maintain invariants requires custom code when data is changed or modified. Such as recalculating the hash of an object.

If I want to arrange objects to maintain some complicated relationship or sorted relation or grouped by relation I need to write lots of custom code or use reactive features.

This idea I thought of while writing the conflict detection of my diff algorithm. I thought maybe we could use the Rete algorithm to handle many invariants of many different objects at the same time efficiently.

We often need to compare objects to sort them or group them.

It's often useful to keep sorted views and grouped views of data in memory for efficient algorithms.

If you could maintain lazily arranged data in memory this would be really powerful.

Essentially I want materialised views over objects in memory.

This comes under the idea of truth maintenance.

Once you define the arrangements you could calculate what is the most efficient source of truth based on the view generation steps.

The invariants that need to be maintained over the data have an ordering. You might find one view is cheaper to prepare from the other than the other way around.

It comes under the same theory as query optimisation and cost based planning and Object Relational Mapping.

This could be combined with [Data Views](https://github.com/samsquire/ideas#90-views-of-data).

This could be combined with [Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure)

# 21. Sort groups

It is often useful to have a single relation that is sorted with a complicated ordering function that maintains the order according to various properties 

It is common to sort on multiple columns of a record.

What is also very useful is the ability to group records together based on these sort groups and iterate on groups separately while still being aware of the overall collection.

A sort group is a relation arranged into a tree where each group is a column and is separately queryable. Traversal of the entire tree gives you the overall sorted list but there is efficient retrieval of individual columns members. I can loop over items of a status and user identifier know the index within the group or the overall collection. I can have a doubly linked list between records between items for fast retrieval.

# 22. Flat map refer

When we flat map it's often useful to refer to the group that the data came from. So I would abstract flat map to incorporate contextual information.

[My algrebralang programming language design](HTTPS://GitHub.com/samsquire/algebralang) has features to do refer to methods in previous stages of the pipeline.

# 23. Time travelling pipelines

Imagine a recursive pipeline. You can visualize it as an ordered tree.

When I write a clojure threading it's often useful to refer to the history lineage of the object that came before in the pipeline.

You have an object that is going through a stream and you want each stage of the pipeline to be associated or collected with future values of that data's children.

We can enrich the data structure of a record travelling through the pipeline to refer to futures or promises to the preceding records have references to the outputs of early pipeline steps.

```
(defn people-calorific-requirements []
(future-thread people-and-weights
 (-> person
 :stone-to-kilograms stone-to-kilograms (:kilograms-weight (* (:weight person) 6.3503)) (person :person requirements :calorific-requirements))
 :calorific-requirements (:requirements fat-sugar-protein (:kilograms-weight item) (item :item))
)
```

# 24. List of lists as graph

We often have a list of list of items with columns and references between lists.

This list of lists with columns can be represented as a graph.

This is what ORM software does for us. It maintains object graphs 

# 25. Imperative graph traversal to query

I like to change between a graph traversal with imperative code to a query and vice versa 

It's quite complicated. But I think it can be done.

If you turn a graph traversal into a set of reasons, you could generate a query.

# 26. Sort method calls of pipeline

Sometimes to change the behaviour of code we want to sort the data. Rather than be explicit of sorting of the data, we can treat the pipeline as data and sort the method calls of a pipeline.



```
(defn sort-function [data-item function-a function-b
 (if (in :pounds data-item
  (if (= function-a :pounds-to-kilograms -1 1)
  (if (= function-b :pounds-to-kilograms -1 1))
 (if (in :lbs data-item)
  (if (= function-a :lbs-to-kilogams -1 1)
  (if (= function-b :lbs-to-kilogams -1 1)
)
(defn people-calorific-requirements []
 (sort (sort-function (future-thread people-and-weights
 (-> person
 :stone-to-kilograms stone-to-kilograms (:kilograms-weight (* (:weight person) 6.3503)) (person :person requirements :calorific-requirements))
 :stone-to-pounds stone-to-pounds (:stone-weight (* (:weight person) 14)) (person :person requirements :calorific-requirements))
 :calorific-requirements (:requirements fat-sugar-protein (:kilograms-weight item) (item :item)))
)
```

# 27. Reverse pipeline and lineage finder

This would be useful for machine learning. Imagine you have a complicated pipeline. What if you could feed in data at any stage and reverse the pipeline to find objects that match your inputs?

# 28. Static garbage collection

But not how rust does it. What if you analysed the call stacks of a program and decide in between calls where to garbage collect. A bit like RAII.

We want to restrain garbage collection until after the critical path. We can track what we need to free if we look at the relationships between passed around data.

So a lifetime is defined as an overlapping callstacks of code and not necessarily at the end of a method.

# 29. Align data

When I wrote my conflict handling of my diff algorithm it might hast been easier if I could align the data accordingly to groups.

We can take two lists and align them into sections where they differ and where they are the same.

# 30. Extending code without changing it efficiently

Usually to extend code we need to change it. Or add parameters everywhere.

I think there's a better thing we can do with compilers.


A piece of code represents data flow from data items to output, it also represents changes in states.

To extend a piece of code without changing it we need to interleave our extension code around the code being extended. We might need to mutate inputs or introduce divergence of types.

What does divergence of types mean? There is an operation called associate which associates a set of lines of code with a variable or type at a place in the callstack history. Wherever the original variable appears we can also refer to the diverged type.

We can also assign changes to the type when the original type changes.

The callstack (all the methods being called and their parameters) and code structure represents the inputs or context of what is being extended against, we can use any local variable or parameter to write code that uses them. We can interleave code anywhere in the callstack. We can topologically sort these relationships to work out where the code needs to be inserted and automatically add parameters between methods.

This is the basis of [my programming language design algebralang](HTTPS://GitHub.com/samsquire/algebralang)

To implement this we need an efficient representation of loops and loop merging.

The following is an implementation of travelling salesman problem in algebralang.

```
tsp cities = {
(array(name=pairs)=cities
.permutations(name=pair, 2))
.permutations(name=solution, previous=s[i][1], size=len(cities), value+=(solution[-1][1], solution[0][0]))
thread(solution, rule(index, item)=(if item[i][0]==item[i-1][1] then item[i][0] else reject, item[i][1]))
euclidean_distance(name=distance, pair[0], pair[1])
euclidean_distance(name=solution_distance, solution)
sort(name=per_order, distance, order=ascending)
sort(name=solution_order, solution_distance, order=ascending)
pairs = first(per_order, solution_order)
= pairs
}
```

A naive implementation of algebralang would do this algorithm slowly, there is a number of optimisations that can cause this algorithm to be faster. The computer should allow us to create additional relationships of the algebraic variables that allow the computer to optimise when to do which work.

For example, we might want to include nearest neighbours. Rather than brute force.

We can add the following.

```
pair_recursively(name=city_to_every_other, pair.source, pair.source) # returns [city, [every other city]]
pair_recursively(name=distance_to_every_other_city, euclidean_distance($item[0], *$item[1]), output=$item[0], $item.value, input=city_to_every_other, $item[1][0]) # returns [city, [city, distance]]
sort(name=neighbours, distance_to_every_other_city, input=$item[1] output=$item[0])
replace(pair, neighbours)
```

I am yet to decide on the syntax for expanding a method n times but I used the * syntax go indicate this.

# 31. Algebraic materialised view edits and optimisation

This is an extension to the [9. Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure) and [20. Lazy arrange or invariant maintenance](https://github.com/samsquire/ideas4/blob/main/README.md#20-lazy-arrange-or-invariant-maintenance)

# 32. Schedule within/networked fork+join

The chain of code I am using to deploy cloud resources should have the capability to send code to execute as if is running in the same thread.

Essentially I can use cloud resources as a fork/join.

# 33. A generalised paging/chunking solution

Many performance problems go away when you chunk something and manage it at a chunk level. Such as pagination or Chrome Blink browser page painting tiles.

But then you have two problems. You have a cache of chunks and schedule the chunks coming in.

I was reading the PolarDb paper and it talks of the database pages used by the disaggregated database.

I recognise that many problems are simpler when broken into pages of data. For example, memory management.

We need to solve all these problems with an approach that works the same for every case. Advanced pager

# 34. Graph to query generation and sort

Render a data structure as a graph and allow selections of different objects and fields and references/pointers.

Work out the rule that caused everything to be selected based on user input such as an if statement like as a debugger condition or relation or mapping, then generate a query that matches that part of the data structure.

Allow highlighted items to be sorted and mapped the graph visually.

# 35. Nearest operator

A high level functional function for composing queries over complicated nested data structures where you ask for the nearest object near this value via object graph traversal or nearest XY coordinates.

# 36. Adjust with respect to operator

Imagine you are merging two documents and have an ordered list of changes and there are character indexes of each change in the source document and a character to insert.

If you insert a run of characters that run of characters could run into another run of characters by the other document. So you need to group the inserts into ranges.

If the range overlaps with another range that is a merge that must be resolved by a person.

You want to cross reference and update the coordinates as they impact eachother. 

If you merge one document in then all the offsets need to be updated to accommodate the new changes.

# 37. Query over in memory data structure

I want to query a data structure as I might a SQL database or a graph database.

If I know the field I want, I can specify the structures I want and the traversals through the code to get to them.

# 38. Dense btree

Combine a binary search with a btree and have multiple keys per node.

This would sacrifice CPU for memory latency as you fetch N keys from the btree at a time.

I think it's related to a fractal tree.

# 39. Data structure mapping studio

There should be a website or office suite software that offers views of data structures from one to another and the operations that can be done on them. These can be implemented as mappings.

For example, each DevOps tool has some JSON or YAML that means something significant. An Nginx file can be parsed and turned into a graph data structure. Kubernetes YAML means something

All these representations should be built on top of eachother. I should be capable of interacting with mapping as if it the real thing. In other words, each mapping field corresponds to the real thing.

Compilers, browsers and database servers should be publishing their internal data models and showing what the data graph looks like inside themselves at all stages of processing. So like compiler explorer I can see the internal model of the application.

People could then learn how complicated programs work and even compose new behaviour on these data models.

By defining Equivalencies we can create really powerful programs. This is materialised views on steroids.

# 40. One for many

If you know how to do something for one item, do you know by inferences know how to do it for all items at once?

Could indexes be generated from a method to calculate something?

You write a nested loop to find or collect together data from multiple sources, if you index each loop separately you can handle any number of items as a materialized view.

# 41. Happens before concurrency and Partial order maintenance

IO event loops are fairly complicated to use properly.

Tokio is good for IO scheduling but not parallel CPU scheduling.

I think we can use the happens before relation to autoparallelize.

We can sort variable use and automatically insert Object.notify Object.wait at points we need our memory to be visible to other processes. These joins before a shared variable is used represent synchronization points.


# 42. Direct concurrency and static scheduling

It's easier to schedule code in advance of its execution.

The traditional software development approach to control flow of asynchronous systems is callbacks, async/await, events, SEDA or event loops.

The problem with event loops is that work blocks the main thread and you don't have parallelism unless you start multiple event loops.

Direct concurrency means scheduling in advance and driving ordering explicitly.

Chaining together callbacks causes complexity.

Rely on sorting to decide the control flow.

The locus of execution is the tip of execution.

Essentially the kernel scheduler and the program itself decide what to do next.

When you have asynchronous code, you don't know when you shall return, you need to decide what to do when the asynchronous program finishes.

I want async/await to work on a thread pool for true parallelism.

```

```


# 43. When language

Use join calculus to be the interface of rete

# 43. Generalized transactions

We often want the semantics of all or none at all.

# 44. Duplicate everything - store everything twice

Store data in both arrays of structures and structures of arrays. Use the left right concurrency control pattern with each side so you get benefits of each.

When there's contention for the wrong data structure (ie it would be more efficient to use arrays of structures), use the code for the other structures or arrays or arrays of structures.

# 45. Code pattern matching


# 46. Snapshot isolation and duplicate everything

We want snapshot isolation in addition to the benefits of duplicate everything.

I should only see what was last committed and changed but I don't want to lower parallelism or introduce locks that lower scalability. I also don't want to clone objects and reduce scalability.

One approach is we can combine the use of persistent data structures with this idea to implement snapshot isolation.

When I change a field, I should regenerate up to root a new record and append to the log for the data structure.

This can be combined with mega tree. We need a global Log object that everyone uses to access the root of the data structure.

When there is a change, the root object is changed. The problem is parallel updates to the root object, anyone who changes before the root is changed would be overwritten.

We need to avoid last write wins as Left Right is not enough to protect the root. So we need multiversion conconcurrency control.

Alternatively we can treat the MegaTree as being threadsafe and not regenerate the tree each time there is a change, so we have internode parallelism. The MegaTree would have a commit method.

For append only illusion we can generate events walked up to the root and when we serialize we serialize new nodes but while in memory it can mutate.

To extend merkle support we can change the hash atomically when children change.

Can use postgres mintransaction maxttransaction to decide on key visibility and check active transactions to see if they are finished.

# 47. Loop selection and autoparallelization

When I create a thread for parallel work and I spend most of my time in my program in loops I need to partition the loops.

How do we partition the loops efficiently?

When we create the threads we specify named collections and partition them by thread index.

For Java lists we can use sublists. For linked lists we can cut them in half 

# 48. Loop rewriter - Avoid resource starvation by chunking loops

Most of the processing goes on in loops. But loops occupy the CPU and don't give any other process CPU time.

It's slow to call Thread.yield in every loop iteration. And it's slow to put an if statement in your loop.

What we need is a loop rewriter

We can rewrite the following

```
StringBuilder sb = new StringBuilder();
for (int i = 0; i < items.length; i++) {
  sb.append(String.valueOf(i));
  sb.append(items[i])
}
```

To:

```
int chunkSize = items.length / 10000;
int chunkStart = 0;
int chunkEnd = chunkSize;

while (chunkEnd < items.length) {
  
  for (int i = chunkStart; i < chunkEnd; i++) {
    sb.append(String.valueOf(i));
    sb.append(items[i]);
  }
  Thread.yield();
  chunkEnd = min(chunkEnd + chunkSize, items.length);
  chunkStart += chunkSize;
}
```

We can adjust the chunk size dynamically at run time to see how long it takes for a chunk to run.

We can exponentially grow the chunk size if it doesn't take long to run a chunk.

# 49. Independent data layout from structure

The layout of memory can be independent of the data structure.

# 50. Context anywhere

I should be capable of reaching anything from any position in my code.

Everything is available to me.

The runtime should schedule things for me and know the relationships between what runs when.

# 51. Rewrite synchronous code into LMAX disruptor thread pools - event loops that don't block on CPU usage

I want my CPU intensive code to be isolated from other CPU intensive code and my IO code to be isolated too.

The problem with NodeJS is that the Javascript event loop is single threaded and your callbacks cannot execute in parallel. Another problem is that heavy CPU usage blocks the IO handling and other CPU usage. This idea is a solution to this problem. Browsers also have this problem.

We can use the LMAX disruptor pattern and dynamic thread pools for efficient processing.

We want to handle multiple consumers and multiple producers. And scale by adding more of each. We can also scale each stage of a pipeline.

As LMAX does, we break up each IO request into two halves: the request itself and its response, each enqueing a new event. We map the synchronous code of what we want to do into to a tree of disruptors each independently monitoring an event queue ring buffer. This is similar to a topology in Kafka.

When an IO event or CPU completion event comes in, we generate an event that needs to be processed. This is written to the ring buffer for events down the chain of that destination type.

```
OnRequest(request):
Error = False
Unmarshalled=Unmarshal(request)
Parallel {
 addressCheck = CheckAddress(Unmarshalled.address)
 creditDetailsCheck = CheckCreditCardDetails(Unmarshallled.creditCardDetails)
 StockAvailabilityCheck = CheckStockAvailability(Unmarshalled.basket)
}
If not addressCheck.success:
 User.addError("Address not valid")
 Error = True
If not creditCardDetailsCheck.success:
 User.addError("Credit details wrong")
 Error = True
If not stockAvailabilityCheck.success:
 User.addError("stock", Items not in stock", StockAvailabilityCheck)
 Error = True
If Error:
 Return ErrorPage(User)
Parallel {
 InsertReserve = insertReserve(Unmarshalled.basket)
}
If not InsertReserve.success:
 User.addError("Could not reserve stock")
 Error = True
If Error:
 Return ErrorPage(User)
Parallel {
 TakeMoneyRequest=TakeMoney(Unmarshalled)
}
If not TakeMoneyRequest.success:
 User.addError("Could not take money")
 Error = True
If Error
 Return ErrorPage(User)
Parallel {
 CreateOrderRequest = CreateOrder(InsertReserve, Unmarshalled)
}
If not CreateOrderRequest.success:
 User.addError("Could not create order")
 Error = True
If Error
 Return ErrorPage(User)
Parallel {
 CPUTask1 = CPUTask1(Unmarshalled)
 CPUTask2 = CPUTask2(Unmarshalled)
 CreateProfile = CreateProfile(Unmarshalled)
}
If not CPUTask1.success:
 User.addError("could not do CPUTask1")
 Error = True
If not CPUTask2.success:
 User.addError("could not do CPUTask2")
 Error = True
If not CreateProfile.success:
 User.addError("could not create profile")
 Error = True
If Error:
 Return ErrorPage(User)
Parallel {
 SendSuccessEmail = SendSuccessEmail(Unmarshalled)
}
If not SendSuccessEmail.success:
 User.addError("Could not send success email")
 Error = True
If Error:
 Return ErrorPage(User)
Return OrderConfirmationPage(CreateOrderRequest)
```

This is turned into a state machine tree, like async await does behind the scenes. And there are join nodes inserted which wait for a collection of events.

If I have 32 cores and there are 27 pipeline steps so I need 27 × 32 = 864 threads this lets me pipeline every stage of the handler code!

I shall have still have disruptors for each line arranged in a tree that looks like this. The code above is rewritten into this style, each line goes inside the previous block. When a Parallel section is encountered, a Join is created at the same level and the parallel pipeline steps are linked to the join. Each pipeline step triggers its children by posting an event to all of them.

```
Unmarshall
 AddressCheck
  If not addressCheck.success
 CheckCreditCardDetails
  If not creditCardDetailsCheck.success
 CheckStockAvailability
  If not stockAvailabilityCheck.success
 Join(If not addressCheck.success, If not creditCardDetailsCheck.success, If not stockAvailabilityCheck.success)
  If Error
   insertReserve
    If not InsertReserve.success
     If Error
      TakeMoney
       If not TakeMoneyRequest.success
      Join(If not TakeMoneyRequest.success)
       If Error
        CreateOrder
         If not CreateOrderRequest.success
        Join(If not CreateOrderRequest.success)
         If Error
          CPUTask1
           If not CPUTask1.success
          CPUTask2
           If not CPUTask1.success
          CreateProfile
           If not CPUTask1.success
          Join(If not CPUTask1.success, If not CPUTask2.success, If not CreateProfile.success)
           
         
````

This generates over 27 while true threads which handle a disruptor events of that type.

When a task finished, it runs the scheduler and decided what queues to place the callback event onto.

I can scale the CPUTask1 and CPUTask2 independently and dynamically. If the capacity for any pipeline stage is 0 then we spin up a new thread to autoscale so CPU usage never affects other CPU cores or IO.

If there is a failure, the scheduler reschedules the event and tries again.

Join nodes require synchronization with a database to capture join states but it can be in memory for performance. This can be asynchronous at the risk of a erroneously restarted process. If tasks are idempotent this is perfect.

This can be implemented by the scheduler by injecting a message to a join thread. This thread has a simple stateful observer with atomic booleans for each join task. If the join fires it raises another event in all nodes that are inside it.

Load balancing occurs between threads by the scheduler moduloing the request sequence number with the count of threads available for that task.

For redundancy and failover we could run in multiple servers and only process one event of each disruptor.

We can front the entry point of the disruptor pipeline with a message queue. Immediately after Netty or your web server handles and parses the request, it is posted onto the ring buffer which is being serviced by Unmarshall. The connection or response object should also be passed into the pipeline, this lets us respond at the end of processing. We can technically process after a return statement. This would be useful to do background processing after replying to the user.

To run multiple processes works too.

How to avoid the overhead of thread context switching?

We can coordinate busy waits so that when the system is busy, busy waits are used but when the systems capacity is low, we use Thread.yield()

Can be combined with event sourcing and CQRS and scaling upwards endlessly and temporal.io event playback and event tracing.

I plan to write this without depending on LMAX disruptor itself. I [started writing the Ringbuffer](https://github.com/samsquire/multiversion-concurrency-control/blob/main/src/main/java/main/MultipleProducerConsumerRingBufferRunner.java), which I ported from [Lock-Free Multi-Producer Multi-Consumer Queue on Ring Buffer](https://www.linuxjournal.com/content/lock-free-multi-producer-multi-consumer-queue-ring-buffer) by Alexander Krizhanovsky.

For event playback, when something goes wrong, the server can be restarted and the requests replayed the same state can be recreated if all events are written to disk. We only need to fsync the first request that comes in, everything fans out from there.


# 52. Rust compiler symbol trialler

In Rust with async and lifetimes it's sometimes difficult to know what you need to do to get the code working.

I propose a random generator of symbols and combinations of lifetimes and some heuristics to cause your code to compile.

# 53. Loop indexing/algebra - data structure loops generalisation/loops to data structure

This idea is not intuitive but this idea has wide ranging impacts on efficiency and query planning.

We should arrange our data that is easiest for the human to understand and let the computer optimise actual data storage.

Each problem has an ideal data structure. We should define the data structure we want and let the computer determine the best course to get there.

Each stage of iteration represents a new intermediary data structure.

Each field access or pointer deference represents a column in the looped dataset.

A nested loop is therefore a new relation with all the columns of the previous iterations included.

Indexing could mean use btree or hashmap for O(1) lookup.

```
class Category {
  public List<Forum> forums;
}
class Forum {
 public List<Thread> threads;
 public Category category;
}
class Thread {
 public List<Post> posts;
 public Forum forum;
}
class Post {
 public Thread thread;
}
// A query to find all post's categories
List<QueryContext> contexts = new ArrayList<>();
QueryContext context = new QueryContext();
QueryContext post_context = context.newLoop();
for (Post post : posts) {
 
 Query context child_context = post_context.yield(post, "post_to_category", "post", post, "category", post.thread.forum.category)
 contexts.add(post_context)
}
context.query_all("post_to_category")

```
This loop can now be queried but not efficiently. It associates a category with a post.

We need some way of matching equivalent loops and deciding which loop to index. And depending on your processing problem, decide which data source to use to solve the query.


We can also generate all variations of data structures storage approach from the looped data structure. Each shall be useful depending on circumstance.

We might infer that you could store the category directly on the post for efficiency.

Reparenting a loop is to do a tree rotation on the loop so that intermediary data structures are the root. This could be used to optimise certain queries.

# 54. Two way placeholder binding data structure and for compiler design

Compilers are complicated pieces of software and they are often written as pipelines 

Changing the behaviour of a compiler would be easier if there was two way binding on each stage of the pipeline.

For example, I can inject new behaviour by deciding how this stage of the pipeline appears to this stage of the pipeline.

I need full contextual information to decide on things.

For example, I want to introduce a change to reorder code. I would need to find the right 

# 55. Dynamic and static and zero cost abstractions

You can do something at compile time or at runtime.

Rust prefers to do things at compile time. As a result it's more complicated.

Dynamic features are easier to write as you put in an if statement and you're done. Problem is this if statement is usually on a hot path. Such as dynamic dispatch.

We can rewrite dynamic features into static features by inserting code and transformations at the right place.

# 56. Tree aware Sorting to implement data hoisting, code motion on the hot path

To compile queries into sourcecode and compile it at run time we can use Futamura projection of taking an interpreter and generating code that is then compiled. This is similar to Java's template interpreter.

We can create a sort function that hoists data to earlier positions by being a tree aware sort.

# 57. Zero cost abstraction movement via interpreter instrumentation

This is an idea on how to implement zero cost abstractions.

You need a program that takes a compiler code, has an interpreter and a program and code generates the combination of three and is then used by a traditional compiler to turn into a program for runtime.

We split the problem of "compile time" and "runtime" as being the same problem to solve with respect to a source program.

We need to virtually execute the program to get callstack histories. We need to understand loops.

This is useful for moving things around as in code motion for efficiency.


We move things from the source program to compile time. Such as allocations, inefficient data structure usage, instantiations, free.

In other words, the compilation pipeline stages are being extended with information of the context of the where things are going on in the source program as if it was being executed in parallel by the compiler.

There is a point in the compiler's AST that corresponds to a point in in the interpreter and in the source program.

We can write naive code and it be optimised away.

```
class Server {
 @Endpoint("/query", Method.GET)
 public Response handleQuery(Request request) {
  DoSomethingExpensive(request);
  for (Item item : db.find(request.parameters.get("query"))) {
   if (expensiveOperation(item) {

   }
   thirdPartySystem.lookup(request.parameters.get("something"));

   ...
   
  }
}
```

# 58. Scheduler alongside code

When you write a complicated program you also write an accompanying scheduler.

This lets you schedule memory and asynchronous and parallelism.

# 59. Automatic semver

If we had library mesh, we could have automatic semver as you're building your dependents you know when they break.

# 60. Impossibility detection

You know the states that a client can get into that are seeded by your network communication.

So by simulating your client you know when they do something that is not possible such as an attack.

It's a state machine.

# 61. Data structure merging

If you have two algorithms and the callhistory of those algorithms with the same data you can merge the algorithms together.

It's a matter of matching up lines of the callstacks of each algorithm. And generating code by walking the matched callstacks.

# 62. Call history pattern matching

We can recognise patterns in call histories and move code around.

# 63. Call history to data structure

Write inefficient code that uses any data structure and turn it into an efficient data structure.

Automatic indexing and view maintenance.

Call histories are essentially guaranteed data access patterns.

From the call histories you can interpret a value that is passed to a method as a read or a store.

You can track the flow of a variable to a method invocation to see how it ended up at that callsite.

In the above examples they came from two tables which are inefficiently kept in memory. The outer table is kept in memory while the inner table is kept in memory.

But only one item is being processed at a time. How do we optimise this?

The call history looks like this -

```
do_domething_expensive(outer1, outer1.inner1)
do_domething_expensive(outer1, outer1.inner2)
do_domething_expensive(outer1, outer1.inner3)
do_domething_expensive(outer2, outer2.inner1)
do_domething_expensive(outer2, outer2.inner2)
```

From this information we can work on reducing the journey of the value to the method. We can also try keep the data adjacent in memory for performance.

For example, if we call a function on each item in a nested loop or do a database call in a loop, we can infer that there is a tree data structure based on the nested loop, the loop corresponds to a graph traversal.

So we can convert the data structure to one that is a graph.

Remember the perfect data structure for nested loops is one that arranged the data according to the natural progression of the loop as all the data is adjacent.

```
for outer in db.fetch(request["query"]:
 for inner in db.fetch(outer.id):
  do_domething_expensive(outer, inner);
```

The ideal data structure looks like this:
```
Outer1 inner1
Outer1 inner2
Outer1 inner3
Outer2 inner1
Outer2 inner2
Outer3 inner3
for outer, inner in items:
  do_domething_expensive(outer, inner)

```
Since we're talking to a database and fetching the items for a record, it would obviously be more efficient to the join in the database.

```
select outer, inner from outer join inner on inner.outer_id = outer.id;
```

We also need to page this data in chunks to avoid it being in memory wastefully.

```
outer_cursor = db.query("select from outer where outer.Id > :last_outer limit 100")
While outer_cursor.has_items():
 Outer = outer_cursor.next()
 Last_inner = -1
 Inner_cursor = dB.query("select from inner where inner.outer_id = outer_id inner.id > :last_inner", outer_id=outer.id, last_inner=last_inner)
 while inner_cursor.has_items():
  inner = inner_cursor.next()
  do_domething_expensive(outer, inner)
```

How do we generate a tree data structure from loop access patterns?



Btree can efficiently retrieve items by key.

If we store Outer in a tree and Inner in a tree, we can do a hash join where outer refers to an inner.



# Generating ideas
 * marketplace
 * schedule
 * tree
 * additive/combined
 * auto
 * mesh
 * hooks
 * Pattern matching
 * Merge
 * In parallel
 * Independently
 * Refer
 * Concurrently
 * topology
 * Graph

# Incomplete thoughts and ideas 

Scope magic

Tree programming
Fluent system
Flow control

Things written as communication protocols are easier to program and reason about. Concurrency too (see go and occam pi)
Turn the GUI into a communication problem.
