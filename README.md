# Additional 100+ Ideas for Computing

Welcome to the forth page of my Ideas for Computing. This is a stream of my thoughts while working on computers with the theme of integration and improvement of how computers work.

This issue is more focused on parallelism, data structures and algorithms so you might need to be familiar with algorithms and programming to understand these ideas.

This is a long document but each section is a few paragraphs. There is probably a project idea in here somewhere but I hope you can be patient and bear with me, this document is a stream of thoughts so you might not like or see the originality of every idea. I see the state of the technology world as being impoverished or poor, many good ideas are not adopted or in the mainstream. You might think an idea is obvious but I might not have seen it or seen it in the manner I want to see it. I am still trying to express my vision of computing but it is different to how computing works today. I think the computer industry is in its infancy and unevenly distributed; the goodness and lessons of industry are yet to percolate everywhere. In my limited experience of the computer industry, most environments are impoverished and don't realise how poor they are and how much better they could be. I don't underestimate how much work is needed to get to where we could be.

 * See [100 Ideas for Computing](HTTPS://GitHub.com/samsquire/ideas), the first issue of this series.
 * See [ideas2, Another 85+ Ideas For Computing](HTTPS://GitHub.com/samsquire/ideas2)
 * See [ideas3, An Extra 100 Ideas for Computing](HTTPS://GitHub.com/samsquire/ideas3)
 * [Follow me on Twitter](HTTPS://twitter.com/mrsamuelsquire)
 * Looking for business ideas? Checkout my [startups repository](https://github.com/samsquire/startups) where I list business ideas.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

If you're accessing this from [the GitHub repository](https://github.com/samsquire/ideas4), there's a table of contents if you click the icon at the top left:

![image](https://user-images.githubusercontent.com/1983701/175236707-835a315e-7f94-43d6-97d7-f2114b3052c7.png)


Thank you to all the contributors who have been sending in examples and corrections!


# 1. Automatic Personal file archives

My personal files inevitably leads to lots of small files which take forever to copy and are transferred very slowly by my hardware when copied. I propose a personal file manager which handles archiving for our files by letting us "log into" our files by unpacking them to fast media and lets us "repack" the files back up when we logout of the file manager.

It should be extracted on desktop environment login and repacked asychronously in the background. Then you can copy the file to your NAS or cloud backup solution as one fast contiguous file transfer. You could also layer encryption and deduplication ontop of this.

# 2. Idea management software

Society is composed of ideas, let's let everyone track the ideas they like. Ideas are informally collected throughout life, there's no central knowledgebase for an individual. There's Wikipedia which represents society's knowledge but there are few systems for collecting ideas you agree with and want to see more of. This document is actually an example of what I want to see: people aggregating ideas they like and want to invest time and resources in.

# 3. Pick up and drop

Drag and drop is too hard, especially on laptop trackpads or trackpoint. What if instead we visually pick up an item up and then drop it. There would be no need to click and hold the mouse. Copy and paste APIs are usually separate from drag and drop APIs, but they don't need to be.

# 4. Chronological news

Each news topic should be tracked separately, I should be able to follow a news stream from beginning to end on a topic.

# 5. Permanent software/platform/language / Software subscriptions and outsourceable stack

At the cost of innovation we can solve swathes of computer problems with common parts of a stack. The BSD networking stack is standardised and solved the communication problem, it seems BSD sockets are in most software products today. But there is a lot of work needed to standardise the rest of the technology stack. See [idea4 on 135. Recursive Coordination and decision portfolios](https://github.com/samsquire/ideas4/blob/main/README.md#135-recursive-coordinations-and-decision-portfolios-and-time-allocation-portfolio-and-recursive-dividends) for how we could implement social and technical leverage to solve this problem of standardisation without the effort of standardisation.

Unfortunately the ground is shifting beneath us at all times. There is no stable space on which to build. Upgrading RHEL 6 to RHEL 7 and to RHEL 8 is a pain and you need to reharden everything again.

To build an app things you need to worry of and solve:
 * Packaging your app
 * Writing a platform abstraction layer for Windows, Mac and Linux compatibility. Packaging for over 200 Linux distributions. Flatpak, Snap or AppImage
 * Twelve factor app
 * Need to decide on how to configure machines so you need configuration management.
 * Need to decide how to deploy your software
 * Need logging need log storage and search
 * Need Application Performance Monitoring
 * Need tracing
 * Need database
 * Need security updates, patching and testing
 * Need multiple environments and repeatable way to deploy environments
 * Need containers
 * Need to orchestrate containers so you need Kubernetes
 * Need to manage Kubernetes manifests 
 * Need a container registry
 * Need backups of databases and container registry and sourcecode and keys
 * Need secret management
 * Need encryption at rest and in transit
 * Need to check returncode every syscall or API call
 * Need rollback deploys
 * Need zero downtime deployment
 * Need feature flags and feature flag toggles
 * Need app configuration and service discovery
 * Need separate release and deploy
 * Need to migrate database
 * Need to harden your app and servers
 * Need to scale application database and support services.
 * Need continuous integration
 * Need dependency security scanning
 * Need a buildserver
 * Need storage for buildserver
 * Need reliable builds
 * Need end to end testing
 * Need a package repository server or cache or mirror
 * Need a development virtual machine for all the platforms you develop on
 * Need due diligence to use an open source library and to be a maintainer of a open source library. Need to do a lot of unpaid work.

Each if these areas is changing all the time. There is nothing permanent to develop against that won't be obsolete soon. But some technologies seem to avoid going obsolete. Let's subscribe to those!

I would like to see some permanent foundations on which to build. Moving towards profoundly stable software and away from the existence of an impoverished software engineering world:

 * I feel a very large problem in the computing industry is that everybody is reinventing the wheel repeatedly and software ends development within a company and has only one deployment. People are working on the wrong problems. What you see on Hacker News as people's personal projects are not solutions to these common problems. People are working on the wrong things.
 * People do not necessarily share their solutions to problems.
 * Maintenance costs of software are very expensive. Everything is constantly changing underneath our feet. The only stable platform is maybe the amd64 instruction set.
 * APIs and abstractions are changing all the time. Every Linux distribution required its own packaging.
 * Each Linux distribution is duplicating effort and repackaging the same set of software for multiple systems.

I should be capable of outsourcing these decisions to experts.

When you pick a stack you inherit all the problems of the stack and you benefit from expertise in one direction: the written code to solve a problem.

But you don't benefit from the executional skills of deploying and using that software. This needs to change.

This idea is so we subscribe to a practice. If you want to use code to drive your configuration that's a decision and something you can build against. Or you want to use YAML.

```
require('system-upgrades') as upgrades;
require('backup') as backups;
schedule(backups.backup, '00 00 * * *')
schedule(upgrades.security_update, '00 05 * * *')

```

# 6. Contiguous disk layouter

A program that reads your startup configuration and then lays out files on disk so everything is contiguous. So a simple program can be written to read all the files into the disk cache on startup and every read afterwards is instant.

# 7. Automated API traversal

Imagine an API as a graph and define a traversal of the API to get what you want. In other words, the types between API methods should be inferred. Imagine I want to backup my files and I want to deduplicate them, compress them and encrypt them and upload them. Each of these steps takes a type. The formation of the circuit can be automatic if the types are well defined, it's a search through a graph.

# 8. Server server

Creating a performant server is difficult. The lessons from Nginx and Apache and pretty much every REST framework or mail server or IRC server or server runner such as gunicorn could be taken and combined into a generic server. This server would be super performant.

The server should be defined a bit like Backus-Naur format but defines a protocol instead. Parsing could be generalised and raised a level in terms of abstraction and applied to protocol communication of arbitrary number of simultaneously communicating processes. It's a state machine and parsing problem.

What would IRC or HTTP look like at a high level?

I want a server to handle as much traffic as it can, concurrently and parallel with low latency, jitter and errors. Nothing should block its IO loop. And other long running computations/CPU usage shouldn't slow down other users.

# 9. Query for data structure

If you're writing a compiler or programming language or business software you have a stored shape of data and relationships at every stage of processing. In business software we call this marshalling or an intermediate representation in compiler technology.

Sometimes to solve particular problems you need data in a particular shape. That is, a problem becomes simpler to write an algorithm for if the data is in the right shape.

What if you had a query language where you could retrieve a data structure?

In compiled languages we have pointers and in interpreted languages such as Python and Java we have references between objects which are similar to pointers.

We also have indexing Data structures such as hashmaps and btrees. What if we could built up data structures by a query?

We want a btree indexing these columns and these relations. As a result, we get a data structure with these indexing structures.

GraphQL is nearest to this idea. I want a linked list of this data or an object graph that looks like this.

Place source structure on the left, target on the right. Can define an algebra that works with nested collections and has a primitive called associate which associates data of left with data on the right.

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

 * **API suite** The desktop should have an installable set of pluggable APIs that are really easy to use from different places: from programming languages, over the network and from an executor GUI. I should be able to create an API invocation and chain them together with a GUI. This is a bit like Swagger, Jupiter Notebook/Ipython and Postman and SOAPUI.

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

Databases such as Postgres have heap managers. Virtual memory are managed by kernels. Some software use arenas for memory management. Memory management is too complicated so browsers such as Chromium just use arenas and free it when the tab is closed. There is all sorts of clever things that can be done with readahead and prefetching and amortization. The problems of chunking has wide ranging impacts to do with caching and decision to load in parallel.

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

We know where the target data is in the data structure.

There is a sequence of steps and iteration to get the query to fetch the data we want.

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

I propose a simple system that tracks all instances of data and keeps them integrated. This would be used between systems and keep then in sync. It would also be used within an application server or database architecture. It would also have the feature to delay updating items before returning success. So indexes can be updated passively or even asynchronously.

Denormalisation solves performance including parallelism problems as in Left Right concurrency control. We need an industry standard way to keep data in synchronisation, in memory.

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

Many computer problems and algorithms can be solved with a division and sorting function and a set of statements that should be maintained over collections of objects.

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

# 21. Sort group tree

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

I would like my ORM to be explicit in its workings and literally accept lists of lists to populate objects, not do magic with annotations or decorators.

# 25. Imperative graph traversal to query

I like to change between a graph traversal with imperative code to a query and vice versa 

It's quite complicated. But I think it can be done.

If you turn a graph traversal into a set of reasons, you could generate a query.

Existing
 * [Chiselstrike, my other database is a compiler](https://blog.chiselstrike.com/my-other-database-is-a-compiler-10fd527a4d78)

# 26. Sort method calls of pipeline and sort reject

Sometimes to change the behaviour of code we want to sort the data. Rather than be explicit of sorting of the data, we can treat the pipeline as data and sort the method calls of a pipeline.



```
(defn sort-function [data-item function-a function-b
 (if (in :pounds data-item
  (if (= function-a :pounds-to-kilograms -1 1)
  (if (= function-b :pounds-to-kilograms 1 -1))
 (if (in :lbs data-item)
  (if (= function-a :lbs-to-kilogams -1 1)
  (if (= function-b :lbs-to-kilogams 1 -1)
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

Usually to extend code we need to change it. Or add parameters everywhere. We write methods to abstract ideas, but those methods cause code to become too complicated to change if we want to create a far reaching change.

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

# 31. Algebraic materialised view edits and whole program optimisation

This is an extension to the [9. Query for data structure](https://github.com/samsquire/ideas4/blob/main/README.md#9-query-for-data-structure) and [20. Lazy arrange or invariant maintenance](https://github.com/samsquire/ideas4/blob/main/README.md#20-lazy-arrange-or-invariant-maintenance)

If I have a materialised view based on another materialised view, I can use algebra to decide which view to update first and which to map to what

We can change computer programs into queries and therefore algebra then optimising queries the same way a database optimises the algebra of a query using a cost based optimiser. if we represent programs as algebra they can be optimised.

I also want materialised views layered ontop of eachother and the computer decide which one to use for source of truth.

I can also decide where to insert records based on the views that are used.



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

Allow highlighted items to be sorted overall or independently.

For example if I have a complicated hierarchy of objects, I can select subitems of collections but retain references to the path that I used to get those items

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

We can sort variable use and automatically insert CountDownLatch at points we need our memory to be visible to other processes. These joins before a shared variable is used represent synchronization points.

I propose a cas sort algorithm to maintain order between an arbitrary number of readers and writers. [I partly implemented this in my compare and swap sort repo. I need to add support for any number of readers and writers.](HTTPS://GitHub.com/samsquire/compare-and-swap-sort)

We need a scalable equivalent of Java's synchronized.

I should be capable of writing code like this:

```
Def Happens_before(self.head, self.head.previous) update_linked_list(new_head)
  old_head = self.head
  Self.head.previous = new_head
  Self.head = new_head
  New_head.next = old_head
```

This should be rewritten to:

```
Def update_linked_list(new_head)
  Trying = true
  While trying:
    old_head = self.head
    Trying = !Self.head.compareAndSet(self.head.previous, new_head)
    if not Trying:
      continue
    Self.head.previous = new_head
    Trying = !Self.head.compareAndSet(old_head, new_head)
    if not Trying:
      continue
    New_head.next = old_head
```


Now all calls to update_linked_list are partially ordered.

But would this be more efficient as an explicit queue?

All threads enqueue their operations and if there is someone already modifying the same value, we don't block but we are dequeued by the committing thread.

Then you need a callback when the work is done. Or you block until the work is done.

The whitepaper Wait-Free Queues With Multiple Enqueuers and Dequeuers algorithm could be used to queue up work.

It could be changed not to block, and callbacks could be checked for by the committing thread 




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

# 45. Rendering engine reflow diff and pregenerated positions for each resolution

Relayout and reflow is slow. Rendering a catalogue of items is really slow, even though the positions and sizes of everything is the same each time.

We can obviously cache the numbers before reflowing.

We can identify patterns in the numbers across rows and columns.

For example if I am rendering 5 columns by 16 rows and do a load for 16 more items, if the items go above the existing items, we can push the bitmap down, we don't need to reflow all those old items.


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

Each problem has an ideal data structure. We should define the data access pattern we want and let the computer determine the best course to get there.

Imagine a special object called a relation that supports all operations that are possible with all algorithms and data structures. What data structure gets ultimately used depends on what operations are executed against the relation.

So in other words, we implement binary search, hash join, hashmaps, vectors, linked list, splice, filtering, mapping, flat map, insert operations and inserts operations on this relation. Think of relation being an imaginary data structure that implements all data structure operations.

Some operations for some data structures are more efficient than others. But if the user requests two access patterns that conflict, you might either need to accept a degradation for one or duplication of data for performance.

Think of the data structures for a text editor. I would define lots of loops for my access patterns for inserting text between regions, creating lines between lines, being line aware and jumping to particular lines. I would also have view recycling and cannot render large files without efficient handling of rendering.

A linked list is cheap to splice between items. Whereas a vector is cheap to copy and loop over.

This idea is based on using loops to define data access patterns, the loop itself as a tree or graph represents the relationships between one relation and another.

For example, the following loop represents membership or association of relation("b") to relation("a").

```
For a in relation("a"):
  For b in item.relation("b"):
    Do_something(a, b)
```

This represents the following data structure:

```
class A {
 B b;
}
```

We should arrange our data that is easiest for the human to understand and let the computer optimise actual data storage, layout and data structure.

Define all your loops and let the computer decide how to structure data so the loop is efficient.


Each stage of iteration represents a new intermediary data structure. For example, if we're modifying a data structure we might want to use a HashMap or a vector, or linked list.


```
For a in relation("a"):
  For left, right in zip(a.relation("b"), a.relation("b")[1:]):
    Insert_between(left, right, relation("b").newitem(a.value+b.value)
```


We should always be looping over a data access pattern, that way the computer can work out what the loop corresponds to.

Rather than
```
Document.onkeypress = function (event) {
  Document.insert(cursor.position, event.character);
}
```
We replace the event handler with an algebraic loop.
```
For letters in user.typing:
  Document.text.insert(cursor.position, letters)
  
```

If we parse this loops as an AST and to an algebra that it maps keypresses to a data structure modification.

This data structure modification could be efficiently handled by a rope data structure as the document is large.


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

For example, I want to introduce a change to reorder code. I would need to find the right insertion points relative to each other.

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

# 61. Data structure and algorithm merging

If you have two algorithms and the callhistory of those algorithms with the same data you can merge the algorithms together.

It's a matter of matching up lines of the callstacks of each algorithm. And generating code by walking the matched callstacks.

# 62. Call history pattern matching

We can recognise patterns in call histories and move code around to generate data in advance of where it shall be used.

# 63. Call history to data structure

Write inefficient code that uses any data structure and turn it into an efficient data structure.

```
for outer in db.fetch(request["query"]):
 for inner in db.fetch(outer.id):
  do_domething_expensive(outer, inner);
```

We want automatic indexing (see loop indexing) and view maintenance.

We can also merge SQL statements together.

Call histories are essentially guaranteed data access patterns.

From the call histories you can interpret a value that is passed to a method as a read or a store.

You can track the flow of a variable to a method invocation to see how it ended up at that callsite.

In the above examples they came from two tables which are inefficiently kept in memory from the database. The outer table is kept in memory while the inner table is kept in memory.

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

```
class Outer {
 public int id;
 public Inner inner;
}
class Inner {
 public int id;
}
```

Remember the perfect data structure for nested loops is one that arranged the data according to the natural progression of the loop as all the data is adjacent.

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

We could write a function that knows how to merge SQL statements for efficiency.

```
select outer, inner from outer join inner on inner.outer_id = outer.id;
```

We also need to page this data in chunks to avoid it being in memory wastefully.

```
outer_cursor = db.query("select from outer where outer.Id > :last_outer limit 100")
While outer_cursor.has_more():
 Outer_items = outer_cursor.next()
 Last_inner = -1
 For outer in outer_items:
 Inner_cursor = dB.query("select from inner where inner.outer_id = outer_id inner.id > :last_inner limit 100", outer_id=outer.id, last_inner=last_inner)
 while inner_cursor.has_more():
  inner_items = inner_cursor.next()
  For item in inner_items:
  do_domething_expensive(outer, inner)
```

Even this is inefficient as we can process every inner item in parallel. So now we need a thread pool or parallel for.

How do we generate a tree data structure from loop access patterns?

```
class Work {
 public Work(Db db, ExecutorService pool) {
  this.pool = pool;
  this.db = db;
 }


 public Map<Outer, Map<Inner, Result>> results() {
  Last_outer = -1;
  outer_cursor = db.query("select from outer where outer.Id > :last_outer limit 100")
  While (outer_cursor.has_more()) {
    Outer_items = outer_cursor.next()
    Last_inner = -1
    For outer in outer_items:
      Inner_cursor = db.query("select from inner where inner.outer_id = outer_id inner.id > :last_inner limit 100", outer_id=outer.id, last_inner=last_inner)
      while (inner_cursor.has_more()) {
        inner_items = inner_cursor.next()
         List<Callable<Result>> tasks = new ArrayList<Callable<Result>>();
         for (final Object object: objects) {
           Callable<Result> c = new Callable<Result>() {
             @Override
             public Result call() throws Exception {
              return expensiveTask(outer, inner);
             }
           };
           tasks.add(c);
         }
         List<Future<Result>> results = pool.invokeAll(tasks);
 }
}

new Work(Executors.newCachedThreadPool()).results()
```

Btree can efficiently retrieve items by key.

If we store Outer in a tree and Inner in a tree, we can do a hash join where outer refers to an inner.

# 64. Parallel linked iterators


# 65. High zipper

A special zipper across graph data structures that remembers the traversals from each value to every other value and allows you to refer to them.

# 66. Program equivalence or merging code together

Track the callhistory of every method, history of every variable,

Write some code that does something similar with the same data, duplicating all the looping.

Track common elements in callhistories for each code, work out where to insert one algorithm into another.

How do you wrap something in an if statement for security?


# 67. RPC to stream

Writing code as RPC is powerful and works for many large corporations.

But it does not necessarily look like a stream.

# 68. Hot path scheduler aware matching - eliminate polling and scheduler hooks

When you're waiting for a case to be true such as in a multithreaded system you use the CPU repeatedly in a busy wait or one with yields to the scheduler.

```
While (root.isDirty()) {
 // Busy wait
}


While (root.isDirty()) {
 Thread.yield();
}
```

The obvious problem with this while you are busy waiting or yielding, you are not informed of state changes. Work stealing algorithms typically do work for other threads to help them.

This idea is for the scheduler to be aware of substates and act as a communication mechanism by providing a matching function that should be intercepted.

When we thread yield we should provide a tree of evaluation that should be true when we are to run. When that tree is changed, we evaluate the function to see if we can run.

For example:

```
While (root.isDirty() {
  Thread.yield(root.setClean);
}
```

Rete algorithm can be used if the object is complicated.

 
# 68. Atomic blocks

Since writing this idea I learned of software transactional mem which is very similar to this idea. I even used the same scenario for updating a doubly linked list as I did in [compare and swap sort algorithm](HTTPS://GitHub.com/samsquire/compare-and-swap-sort)

In my code I should be capable of specifying atomic sections of code.

For example:

```
Atomic {
  Previous = node.next;
  Node.next = newNode;
  Previous.previous = newNode;
}
```

If this code is not atomic, you introduce bugs when iterating forward or backwards over this data structure in a multithreaded environment.

This should be extended to network and database calls, for example:

```
Atomic {
 db.query("update users set last_order_time = :last_order_time;", datetime.now())
 db.query("insert into orders (user_id, total_cost) values (:user_id, :cost);", user_id, cost);
 db.execute_values("insert into order_items (product_id, quantity) values %s", basket);
}
```

I expect all three commands to work and if any fail, the others rollback. How to implement this?

When we begin an atomic block, we ` insert into versions (start, finished, id) values (true, false :transaction_id);`

We keep a log of what we did do, and how to reverse each process. Ideally the database is designed so that new items are inserts. We can delete inserted items. 

We also store a version number. We also have a commit timestamp. This is a system wide timestamp.

If all the subtransactions successfully complete, we `insert into versions (Id, false, true, :transaction_id)`.

Versions without matching finished entries are failed rolled back transactions.

We join on versions that are complete.

```
Select product_id, quantity
from order_items
inner join on versions
where order_items.version_id = versions.transaction_id
And versions.transaction_id = max(transaction_id)
and versions finished = true


```

# 69. Societal truth maintenance for business and person welfare

Any personal decision or business has a set of supporting statements that must be true for success.

We can track these backing statements and depend on them

For example, if you depend on the fact you know Python to get a good paying job, you might want to know when this is no longer true.

Companies and individuals are expected to adapt with the changing world.

Let's track all the clauses that people depend on and inform them when things are no longer true.

# 70. Depoll

Polling is the slow and poor use of resources way of reacting to change.

I propose that applications register interceptors on data structures and they are executed when data changes.

There should be a standard network protocol for registering or hooking into data changes for reactivity.

This way we can solve all polling issues with a single websocket implementation.

# 71. Partial order scheduler

Clearly we want to run multiple threads in parallel, the problem occurs when they both want to write and read to the same data structure.

I propose a scheduler that deschedules threads that want to read or write to values that are being written to.
This idea is based on the whitepaper Wait-Free Queues With Multiple Enqueuers and Dequeuers.

When we go to write or read from X we set our thread's state to read or write X and we set our phase number to the maximum phase number of all threads + 1.

When someone goes to read write X, they check the phase number of all threads and if there is one less than itself, it unscheduled this thread. Then when that other thread is finished it reschedules threads that are the lowest phase number excluding the thread that was finished.

# 72. Loop expansion and live iterators

Index some code for loops and expand loops outside their enclosing method.

Compose a single source of truth for loops that is maintained across the whole system.

In other words, I can define behaviour across multiple loops over records and declaratively define relations for those things being looped over.

For example, to define all the pages a user can see on a website, I might write the following loops:

If any items change in any of the underlying queries, that loop iteration gets reexecuted. This can be mapped to a web framework.

```
For user in db.query("select user_id from user"):
  
  For user_product in db.query("select * from products where user_id = :user_id", user_id=user_id):
    For permission in db.query("select allowed, resource_id in security where resource_id = :user_product_id and type = 'product'", user_product.id):
     If permission.allowed:
       Yield_page("/:user_id/:product_id/", user_id,user_product.id, "user_product.html")
     Else:
       Yield_page("/:user_id/:product_id/", user_id,user_product.id, "permission_denied.html")    
     Yield_method(POST, "/add_to_cart", add_to_cart)
```



# 73. Loop to schema

Rather than define relations between things with special classes as in Django and Hibernate, define them as loops.

```
for category in categories:
  for thread in category:
   assign(category, thread)

for thread in category.threads:
 for post in thread:
  for like in post:
   assign(thread, post, like)
  for thank in post:
   assign(thread, post, thank)
  for inlink in post:
   assign(thread, post, inlink)
  for attachment in post:
   assign(thread, post, attachment)
  
```

# 74. Code equivalence

How do you detect if two pieces of code have the same outcome?

You need to provide the same inputs to both pieces of code. And the expected output.

Turn each piece of code into an AST.

Turn every variable name into a relation.

Turn loops into multi relations.

How do you detect common algorithms?

Remove all methods and inline everything.

What is the outcome after each statement of code? How does it get nearer to the same output as another piece of code. 

Does the relations of one program match with the relations of the other program?

The output data matches if the same relationship matches, for example, 

```
{
  "Name": "item1",
  "Tags": [{"name": "tag1"}, {"name":"tag2"}]
}
```

Is equivalent to

```
{
 "Name": "item1",
 "Tags": ["tag1", "tag2"]
}
```

Why is this idea so important? If we can compare implementations for equivalence we can also compare their relative costs.

We can think of programs or code as queries. And we can tweak queries to be more efficient.

If programs are algebraic relations we can reorder them!

If we can reorder programs we can optimise them. This is what relational algebra allows us to do.

So we can have whole program optimisation.

If we model programs with pi calculus or lambda calculus or process calculus we can optimise programs automatically 

We can convert variable based programs into these calculuses and algebraic transformations.


# 75. Internet Creator-advertiser-searcher utopia

The problem on the internet is a funding and a collective action problem. Search engines want to earn the most money so they show adverts. Websites and news websites and content producers want to earn money and views so they place adverts. Advertisers want to earn money by showing people things. Advertisers want to target people who shall action (buy something, believe or change their mind or awareness of something) what they see.

I want to normalise paying for content and advertiser's paying for viewer's time.

Content producers need to pay the server costs and bandwidth.

Users want evergreen high quality content.

So I propose a community where a utopian scenario is created.

* Users decide how much money they want to spend and they decide what they want and answer questions of it.
* Users decide how much they want to be paid to see an advert that is targeted to them. The price of an advert is calculated by market forces.
* Searches are non private and available to everyone on the community. Users and advertiser's can see people's searches.
* Advertisers who want attention can fill out a profile of who they want to target.
* Everyone can comment on a search term and talk of it, each search term is an open forum thread for open talking of the relevance of each result.
* Content creators can accept commissions in return for money. The created content is then publicly available for purchase.

# 76. Asychronous community

Network effects means sites don't get used unless they have things on them or other users.

There should be a website that aggregates websites that are new and don't have many users. You can then register on all of them and be pinged when new things appear on them.

# 77. Code between

Most of the time monolithic and microservices have deep callstacks.

I would like to see the shape of the data between calls and run the code inside a hot loop.

So I propose a debugging system that records all arguments and allows replay of arbitrary lines of code.

I want it to be less difficult to test real code with real data.

Software should come with traces of data that can be used with the program. And I can decide which methods to run between with the data.

# 78. Scale to zero and cost saving apps

Serverless is essentially scale to zero. I feel we need scale to zero for regular software in virtual machines.

The problem with scale to zero is that you need a coordinator that coordinates the bringing up of services. For servless cloud services this is the cloud provider's own service.

I propose a mobile application that has a front-end that is designed to queue actions while the backend is unreachable.

When the user does things on the app, the actions are queued up. It takes around 10-30 seconds to deploy from cold and startup and be ready to serve requests.

So when you're not using the service, the service scales down to zero.

# 79. Interface search

If we have 74. Code equivalence can we transform one interface to another?

If I refactor the objects needed to enter into a request but largely the code relations is the same inside, can we search the code for a path that leads to the same output?

The options to invoke a request are limited to what the API provides.

We have types! We can look at what relations were used in the original code and diff them with options in the new code.

So if someone refactors an interface, can we automatically port our code to use the new interface based on context that is available in the original request.


# 80. Implicit sort or sort percolation and sort invalidation

In a multithreaded system, you cannot have overlapping reads and writes to the same data.

I want to define a sort function that detects if a transaction is invalid.

This causes multiversion concurrency control to be easy.

But I want my sort function to detect invalid states.

It's not efficient to sort repeatedly, so we need some way of lowering a sort into code and percolate the if statements of the sort.

How do you percolate a sort function?

Sort percolation takes a sort function and tries to weave the if statements into a wider program. Whenever objects of the kind being sorted are in scope, the if statements are inserted to prioritise which comes first.

Sort functions also have a grouping property, such as when the group changes. We also want to detect this and returning 1, 0 or -1 is not enough, we also want a sort reason from a sort function.

# 81. Reordering IO at runtime - a crash safe language

I want a programming language that can crash at any point and recover when restarted. It should update the disk data structures in an order that is recoverable.

The recovery process can be very similar to the code path used for handling requests.

It should schedule writes and network calls to be robust by ordering writes so that the database is always consistent. The approach that ShardStore takes could be generalized.

For example, in ShardStore which is used by S3 there is an append only log and 4 things need to be updated on disk when a PUT is received. The data of the PUT needs to be written to a free extent (that's a contiguous block of space), an LSM index node needs to be written, the LSM metadata and the superblock which refers to the extents start position needs to be updated.

Every extent is prefixed with the request metadata. On recovery, every extent can be walked and checked if the other data has been updated and the data is accurate.

This also needs to be written in parallel to every other transaction going on concurrently - so you need to merge writes to the same data structure such as two writes to the superblock.

Write a forward progress function and the recovery function is written.

# 82. Symmetric reflection of software layers

With how traditional software is broken up into layers and layers go in one direction it requires invasive changes to support features that have mutually recursive interactions between layers.

We can solve this problem! We can introduce mutual recursion across layers which adapt behaviour in two places simultaneously.

For example, you have a desktop environment and a display server. Some features need to cross the boundary and manipulate both. And vice versa.

It requires a drastic rethinking of cause and effect and atomic behaviours.



# 83. Multiversion concurrency control as part of a language

It should be mark up code as being concurrent.

For example 

```
concurrent (X) {
 do_thing1_with(X);
 do_thing2_with(X);
}
```

Can be combined with parallel blocks

```
parallel {
 concurrent (X) {
   Y = do_thing1(X)
   Z = do_thing2(Y)
 }
}
```

This would abort the concurrent block and restart it if another process interacts with X.

# 84. Adaptive acceptability social network

Inevitably on any group chat or community there is behaviour by a minority that the rest finds to be not pleasurable or acceptable. But there is a split in the community in who agrees what is fine and what isn't.

So to avoid the community splintering we can do something else. Users can tag comments with what the message is an example of. When enough people tag something as exhibiting something, we filter out messages that are tagged enough times. You rely on web of trust and mark which tags you don't want to see.

So we can have one large community but everyone sees different subsets of posts.

# 85. Multiple direction code

Most code executes from top to bottom.

What if every line was an entry point relative to every other?

This is the basis of [algebralang](HTTPS://GitHub.com/samsquire/algebralang).

So every line of code affects every other line of code.

Mutual recursion, with one preferred path.

We can optimise with this approach.

# 86. Dream browser

Similar to my idea for an [Instanceable Wiki](https://github.com/samsquire/ideas2#36-instanceable-wiki) I like how browsers allow you to surf into an app without an install.

Features I think browsers should have:
 
 * **SQL** browser engines should provide SQL APIs. SQL is industry standard approach for querying data and it can be optimised.
 * **Distributed storage** Sync should be built into the browser and any offline data should be backupable to the cloud.
 * **Seamless merge with CRDTs** Browsers should implement CRDTs ala Automerge and Yjs and Braid protocol.



# 87. The unwritten program and overspecified systems

When you've written a system such as PostgreSQL or the Linux kernel you have a lot of code that does something and does it well. Or you're Google with millions of lines of code.

The problem you have now is that you need to understand and read this code to see how the system works as it is at this time. To change the system you have a lot of work to do as you need to gradually transform how things are done to the new approach.

This is very complicated. Changing running software is very difficult and maintenance is a huge cost of software engineering.

When we look at code from a high level there is a large limitation of what code you shall write next, it's not random. Github Copilot proves this.

There are patterns that are true of every software such as book keeping functions and constants such as - 1 or + 1. 

We should be capable of writing what should be true rather than how to do it. I think this is the next step for programming languages.

We should be specifying what we want to be true. And let the computer decide how to do it.

How do we implement this? We overspecify the system.

If we overspecify the system and say what should be true, we can solve algorithmic problems with pattern matching.

Overspecification is to define all the states and invariants of the program.

So we should be using set syntax to refer to recursive sets. Or we should be directly using algebra to specify invariants.

# 88. Stacks to code

We spend most of our time writing code to generate stacks.

What if we wanted to achieve something complicated instead and wrote the stack callhistory we want to see and generate code from it?

# 89. Rewrite Performance and refactoring problems translated into problems that can be solved as intellectual puzzles

AI has not surpassed the capability to automatically refactor to human understanding or rewrite problems to be efficient to solve performance problems.

But We have 7 billion people in the world. Each is capable of solving puzzles. If we strip technical nature of performance problems and code understandability into high level problems.

Could quizzes be used to lead to nearer answers that solve technical problems?

Could the average person refactor and solve performance problems?

Humans are good at pattern recognition. With enough data humans could solve algorithmic problems.

The functions of a computer could be rewritten as a people problem or road problem and people puzzles. For example, this group of people represent the kernel, this group of people represent user space and these people represent packets and these people represent the CPU.

IDEs should automatically profile your code and generate flamegraphs. The user is asked why are these people taking so long.

Refactoring is introducing new people to represent or handle certain things. Some people represent an interface (types matching).

I imagine a website that lets people solve technical problems with these metaphors. In aggregate the wisdom of crowds shall find out answers to problems. 

Let's map programs to what they're actually doing in English terms and use intuition to reason what should solve the problem or how we want to think of the problem.

# 90. Dream IDE


 * **Continuous integration** CI that runs locally and standardised.
 * **Standardised deployment** automatically deploy to Kubernetes

# 91. Methods, classes are local optimum of computer science

What gets executed on a CPU is instructions that manipulate registers and memory.

Classes and methods only exist in the compiler. Even a stackframe is virtual.

I kind of feel these are local Optimums that we learned throughout history in computer science.

There must be a better approach to structuring code, maximising interoperability and maintainability of code and minimising complexity. Code communicates how something is done but not what it is trying to do.

I think types are useful but they are not a panacea or silver bullet.

When I look at what needs to be implemented to implement a text editor in Apple MacOs or Kubernetes I think we're reaching the limits of understandability in computer engineering.

# 92. Indexed code execution and code generation

When you parse Quicksort, mergesort and insertion sort the algorithms have very little variation from a tree perspective.

I wonder if code can be indexed to identify patterns.

And trialled on data to see if generates the right answer.

# 93. Type collections

What does the type:

```
Upload<Servers[]>Encrypted<PublicKey>ZippedDeduplicatedWithReferenceTo<ReferenceData>
```

Represent? It represents a deduplicated data that has been compressed, encrypted and uploaded.

Or is it a monad? It takes an operation and wraps it with an operation.

# 94. Oplog concurrency control

This is an idea of a granular lockfree algorithm that doesn't block, that is it should be wait free.

There is a tree or complicated data structure that needs to be updated and visible to multiple threads. Multiple threads want to read and update this data structure.

All threads serve a shared FIFO buffer for enqueing modifications potentially a ringbuffer.

When a thread wants to modify the complicated data structure it creates an Op event with the parameters for the change.

The op event has a granularity setting which corresponds to the field being modified.

Two pointers or indexes to the oplog are kept. One is the current position and one is the scanahead.

Each thread scans the oplog from the current position and then from the scanahead pointer and handles requests

Another HashMap is kept per thread that marks what is blocked based on the oplog.

As they are scanning the oplog if they encounter a read or write event they mark the blocked HashMap with the key that is blocked and the granularity that is blocked. They skip these items and let the thread whose responsibility is to handle that request, then they handle requests that aren't blocked.

When a thread successfully reads or modifies, it inserts an oplog finish event, this advances the current pointer by one and resets the scanahead to current.

The idea is that all threads can successfully read and write the same data structure if the granularities do not match. But threads can always progress even when their own work is blocked.

To do an operation a thread must enqueue all its operations it wants to do to the oplog

```
NewNode = new Node(value=6)
NewNext = new NewNext(previous=complicated.next,
  field=complicated.next, 
  new=NewNode,
  granularity=(complicated), id=500)
NewPrevious = new NewPrevious(previous=complicated.next,
  field=complicated.next.previous,
  new=NewNode, granularity=(complicated.next, complicated.next.previous),
  id=500)
NewNodeNext = new SetNext(previous=null, field=NewNode.next, granularity=(NewNode))
NewOps = [NewNext, NewPrevious, NewNodeNext]
FinishOp = new FinishOp(granularity=[NewNext.granularity, NewPrevious.granularity, NewNodeNext.granularity])
For op in NewOps:
  Oplog.add(op)
Pending = true
While pending:
  AllWorked = True
  For op In NewOps:
    If op.pending and !TryCAS(op):
      Op.reset() # resets previous and granularity
      AllWorked = False
  If AllWorked:
    pending = false
    Oplog.add(FinishOp) # unblocks all the data structures
   
    
```

This scheme needs multiversion concurrency control or persistent structures due to the fact that arbitrary fields can be changed by other threads.

This could be implemented as simply as this:

```
class DoublyLinkedList {
 int version;
 RingBuffer<DoublyLinkedList> root;
 RingBuffer<DoublyLinkedList> next;
 RingBuffer<DoublyLinkedList> previous;
}
```

When you read from the DoublyLinkedList you always receive fields highest of less than or equal to root.version. That way you have data sharing as in a persistent data structure.

# 95. Visual data structure and program synthesis

This idea relies on the graph isomorphism problem and the ability to match graph morphisms.

Represent algorithms and data structures as graphs.

Define two data structures one before an operation and one after operation and the operations parameters.

Calculate a diff between the graphs. Allow the user to provide sub operation steps for more complicated data structures.

The diff can then be changed into a DFS/BFS/dynamic programming/graph Search algorithm to transform the input into the output.

We can represent algorithms as graphs and use a morphism search to find algorithms that implement the transformation We need to define sorts and partial orders explicitly.

Merging data structures should be possible with a hint to merge and what to merge and the reason for merging.

The computer can work out how to take the arguments and the source input and the end input and create an series of steps to transform the input graph to the output graph.

For example if you were implementing garbage collection you need to do some wide reaching graph transformations over the stack and track alive pointers. What if you could see that memory list in memory and then define what should go on to it with rules and an input to output mapping. As long as you provide the reasoning for a change to the input structure you can generalise the activity with objects that look different.

This could be combined with [34. Graph to query generation and sort]() and Object manager and [20. Lazy arrange or invariant maintenance](https://github.com/samsquire/ideas4/blob/main/README.md#20-lazy-arrange-or-invariant-maintenance)

# 96. Core developers and opaque projects

Some technologies are built by few people and very few people understand the technologies they build upon intimately.

Similar to Non leaf framework I feel this leads to technological mountains where very few people understand the code they rely on.

How many people realistically understand the Postgresql, Chromium, Firefox, Linux kernel, Kubernetes?

Why aren't these projects documented to the level I want? Why don't they explain their algorithms?

# 97. Multiplexing as a computer primitive, API and Visual Multiplexing 

Treating one thing as if it's multiple things is extremely powerful.

 * Multiplex N goroutines/green threads over M threads and processes. [See my preemptible-thread repository for my implementation of this.](https://github.com/samsquire/preemptible-thread) See my [multiplexing repository](HTTPS://GitHub.com/samsquire/multiplexing) for a highly parallel event architecture
 * Multiplex traffic over a connection.
 * Multiplex memory in a an memory allocator (different pages sizes)
 * Multiplex DOM operations over time (React)
 * Multiplex parts of queries in a database engine (query parallelization)
 * Multiplex lines and characters in a document (Rope data structure)
 * Union types in a data struct
 * Monads
 * IO multiplexing as in epoll and kqeueue or IO ports
 * Syscall multiplexing: doing syscalls in a thread to avoid blocking
 * Event loops
 * Batch processing systems that use windows
 * Locking, semaphores, mutexes multiplex the CPU
 * Scheduling, assignment problem
 * Containerisation
 * Concurrency
 * Bit torrent
 * Continuations
 * Currying
 * Layout engines multiplex what is on the screen
 * Multiplex Turing machine tape memory over tip of execution
 * Multiplex virtual memory paging
 * Load balancing
 * Compilers multiplex instructions over time
 * Compiler registry allocation (there's a limited number of things and they need to be shuffled around)

These problems could be solved in a profoundly effective way with the right abstraction, API and used for all cases.

Imagine the same code being used for scheduling tasks onto threads and green threads as used for bittorrent.

The kernel should provide this abstraction as multiplexing is a higher level of resource sharing.

The same algorithm can be used to schedule all these things.

The key component is time or execution time and scheduling.

The tip of execution is what is being executed at this time to multiplex we need to switch between it and multiple other items.


We want to change the tip of execution between multiple things.

For the Linux kernel this is a hardware interrupt on a timer where each process is ordered in a tree by priority and the highest priority process is cached. The schedule() function in kernel/sched/core.c and switch_to in process_64.c.

Unfortunately it's not really possible to prempt a thread in user space. When a thread is executing it can only be prempted by the kernel scheduler. But if we are an interpreter we can do what Golang does, we can preempt virtual threads/goroutines by having a stack per process and multiplex between processes and inserting scheduler commands when the stack grows.


The problem with this is that you need to rewrite instructions to point to correct jump locations and branches.

```

```

# 98. Virtual interrupts

One approach to prempt a hot loop is to insert an if statement in the loop that checks for number of iterations before calling scheduler to see if the hot loop should stop or be cancelled.

This obviously introduces an overhead as the cost of providing interactivity or liveness.

I propose a virtual interrupt statement. The virtual if statement is only ran when another thread interrupts it in user space, by modifying its memory.

In the [asynchronous non cooperative premption proposal for Golang they suggested inserting code into the instruction stream](https://github.com/golang/proposal/blob/master/design/24543-non-cooperative-preemption.md) to cause a scheduler trap. [See this design document on Scalable Go Scheduler Design Doc](https://docs.google.com/document/d/1TTj4T2JO42uD5ID9e89oa0sLKhJYD0Y_kqxDv3I3XMw)

How to do this in a compiler, we generate two loops in assembly. One has the scheduler trap one doesn't.

When another thread, the scheduler, decides that a process has executed for too long it switches the jump address to switch the loop to the one with the scheduler call.

In C we can modify a hot loop by writing to the memory of opcodes of the loop. For example, [see this stackoverflow post](https://stackoverflow.com/questions/7447013/how-to-write-self-modifying-code-in-c) if we add a disassembler and identify the conditional jump of the hot loop, we can modify the jump target to a line that calls the scheduler. It's possible for the cancel button to actually cancel.

# 99. Register loop

One approach to implementing hot loop preemption is to introduce a register loop function.

For example, we register the loop variable as a global variable and register the invariant function 

When we want to prempt the loop, we set the global loop variable to the end of the loop causing the loop to end.

I implemented this as a multithreaded scheduler of lightweight threads multiplexed onto kernel threads in C and Java, see my [preemptible-thread repo](HTTPS://GitHub.com/samsquire/preemptible-thread) 

# 100. Dream programming language

 * **Highly concurrent and parallel**
 * **Compiler, interpreter and virtual machine based** I want my code to run on multiple systems. So that involves some kind of compilation step or virtual machine. When we want performance, we compile. While developing, we interpret.
 * **Zero downtime deployments and separation of release and deployment** PHP is easy to deploy - just upload files. But it's not easy to do an atomic deploy of PHP code as there is a risk that someone requests halfway between an FTP copy. We can use virtual dispatch tables to switch between versions of code. The virtual machine runtime can load new code atomically.
 * **Accelerated by GPU**
 * **Very few keywords**
 * **Concurrency control** Locking or serializable snapshot isolation
 * **Statically analysable**
 * **Powerful types**

# 101. Dream browser

 * **SQL APIs**
 * **Distributed storage** 
 * **GUI scalability** Can load trillions of records loaded in the GUI, silently paged behind the scenes.

# 102. Event sourced multiversion concurrency control and database sync and ondisk format

Event sourcing solves so many problems. We can synchronise with other nodes by simply replaying events. We can store data as an immutable log on disk as an append only log. We could overlay a CRDT over the log so that data can be merged at any time, even asychronously. The entries in the log form a CRDT with each record merging seamlessly with every other we can introduce the concept of a tree overlaying the event sourced log.

A hash identifies the lineage of the event sourced log, it represents the hash of the current item plus the hash of all the children that precede it so a hash represents the history as content addressable storage.

When machines diverge, perhaps they go offline and don't communicate, the changes shall be grafted into the log and sorted by causality. For example, if two users go offline and change a data structure the causality shall be set to the causing hash and a number.

If we have two threads that both want to modify the same data structure simultaneously, the traditional multiversion concurrency control approach is to version the lists and abort if one fails to append due to parallel edits to the same data structure then retry with the updated structure.

There's an approach that means that we don't have to abort.

Rather than keeping two versions of the lists, we can use event sourcing.

The concurrent modifications are turned into a series of partial events of appends or deletes.

If you were incrementing a number, you wouldn't store the event of the new number to store but how much to increment by.

Look at this history of events, we have two threads and they can each increment the number

1:I1 2:I1 1:I1

The value is 3. Before raising an event you getAndIncrement an atomic integer, this is your timestamp.

Incrementing a number by a number is a self committing event, if we want cross field snapshot isolation, we need an additional event, imagine we have this history of updating a doubly linked list:

1:head.next=1 2:head.next=3 1:1.previous=head 2:3.previous=head

These changes conflict with one another. As they both try modify the head.

We introduce commit events to introduce atomicity.

1:head.next=1 2:head.next=3 1:1.previous=head 1:commit 2:3.previous=head 2:commit

Then we sort and group by thread Id and operation sequence number.

This interleaving is thread safe.

1:head.next=1 1:1.previous=head 1:commit 2:head.next=3 2:3.previous=head 2:commit


We ignore events that don't have a commit yet.

The tree sort function sorts based on the timestamp, threadId and sequence Id, so items of the same threadId are next to one another in order of sequence number.

```
Sort(left, right):
 If left.cause > right.id:
  Return 1
 If left.cause < right.id:
  Return -1
 If right.cause > left.id:
  Return -1
 If right.cause < left.id:
  Return 1
 If left.threadId > right.threadId:
  Return 1
 If right.threadId > left.threadId:
  Return -1
 If left.timestamp > right.timestamp:
  Return 1
 If right.timestamp > left.timestamp:
  Return -1
 If left.sequence > right.sequence:
  Return 1
 If right.sequence > left.sequence:
  Return -1
 

```

Now the transactions are in right order we need to ignore transactions that don't have a commit.

We regenerate a new version of the linked list if there are mutations so every transaction gets an immutable snapshot of the data.

```
Committed = {}
Transaction_group = defaultdict(list)
Previous = linkedlist_root
Previous.mutable = false
For item in log:
 Transaction.group[item.timestamp].append(item)
 If item.commit:
  Previous = Reduce(apply_linked_list_patch, transaction_group[item.timedtamp], previous)

Def apply_linked_list_patch(previous, patch):
 If patch.type = "head.next":
  Previous.head.next = patch.value
 If patch.type = "value_previous":
  If patch.subtype = "head":
   Patch.value.previous = previous.head
  If patch.subtype = "subvalue":
   Previous_root = previous.value.previous
   Previous_next = patch.subvalue
   Patch.value.previous = patch.subvalue
   While previous_root.previous != None:
    New_previous = Previous_root.clone()
    New_previous.mutable = true
    New_previous.next = previous_next
    Previous_root = new_previous.previous
    Previous_next = new_previous
   Previous_root = previous.root.clone()
   Previous_root.next = previous_next
   Previous = previous_root
    
    

Return Previous
```







So even if events are raised in interleaved order:



All the append events are aggregated minus the remove events and this is the version that is iterated.

We can sort the edits with tree sort so that edits of the same transaction appear after one another this gives us serializability.

For a linked list and if there is an edit in the middle of the linked list at most three items need to be changed so we get persistent data structures.

For a tree we can create new records up to the root to create a new shared persistent data structure.

We can keep a cache of versions of event sourced read trees/linked lists/collections.

For tree we can know the new generated items up to root by keeping a cache of the old identifiers and the new ones while we build up the tree.

# 103. Dream API

 * **Cancellable APIs** 
 * **Responsive APIs**
 * **Flow Control**
 * **Parallelism and concurrency at the same time** 
 * **Multiplexing and scheduling primitives**

# 104. Autothreadpool and code movement parameterization

To use slow features you need to amortize the cost 

We can write code that finds all new Thread() code and turns them into threadpool references.

So from the user perspective the use of threads is simple.

Imagine my new Thread implementation closes over some variables in the scope where I tried to create the thread 

These can be moved to an argument being passed to the threadpool.

# 104. Multistack microservice pattern

IO is slow. RAM is slow. Network calls are slow. Microservices are slow. Linked lists are slow. The CPU is fast.

Rather than group microservices into noun services and keep data of the same kind together on different servers, group up the entire stack into vertical slices and deploy everything on every server. So every server has an order engine on it.

So each server has a database of products (small), orders (small), user events (growing endlessly), email service, 

An end to end flow can happen on one server.

For global properties such as stock levels, implement distributed concurrency control where every server is in communication with every other and does a two phase commit for any stock reservation. If any add to basket operation happens in parallel, one shall be aborted and retry. For stock levels you want strong consistency. 

# 105. Cross codebase flow analysis and Communication reducer

The perfect microservice system doesn't require back and forth with other systems.

We can analyse the code communication patterns to decide where to move each behaviour.

# 106. Expected pattern and type based optimisations

At any point in your code you're in a context. You might have interrupts disabled, or you might be executing in a particular thread. Or you could be reentrant.

This qualities should be captured by the type system but they are contextual environmental types not return types.

This fact can be used for code movement.


# 107. Distributed Continuation Passing

Rather than talk back and forth between two servers, start a server on the client, send a request and then pass the program to that server that is serving the request where the remainder of the program shall be executed this server repeats the process for the remainder of the computation.

# 108. Computing is just additions, multiplications, loops and search

Programs eventually loop over data, add it together or multiply or divide it.

The abstractions of APIs and programming languages get in the way of this simple desire to loop, add, multiply and divide.

Loop over APIs. Imagine writing a loop that says what you want to do and the computer works out the APIs and the order to call based on your loop.

So imagine I have this imaginary software that introspects a piece of software while running and has access to the sourcecode.

I can feed in some data and follow all the functions and APIs the data goes down into, for example, I can execute:

```insert into people values ('Samuel Squire', 32)```

And I can track the `struct`s that Samuel Squire goes into and follow all the method calls and loops that process this information.

I can track where this data reaches disk.

From this trace I know how to use all the APIs internal to the application.

# 109. Direct coding style, direct code style to indirect style and direct style concurrency

Direct coding style is to act on objects and determine their behaviour from a high level of saying what should happen.

For example, if I was writing a load balancer in direct style I could write my load balancer to loop on a connection object, pick a destination and write data to the destination. Then loop on new requests and pick a different destination server.

Unfortunately most programming is done in an indirect style. For example we define the behaviour of an onRequest handler and we store state between requests of our onRequest handler.

We rarely have full authority over the entire stack.

We write a small piece that has visibility of a tiny piece of the system.

We can map direct style into indirect style.

You can think of direct style code as being object oriented and dealing with the whole system at once.

For example within a web framework request handler you are in direct style while inside the request but from the perspective of the web framework it is indirect.

Direct style code is easier to reason about and easier to write concurrent programs in.

Direct style parallelism and concurrency would look like this.

```

```

# 110. Insert between curly brackets

When you have a lot of loops and nested code it's not always obvious what context you're in, when you click you should be given a list of the outer contexts of what you want to place after.

# 111. Autoparallelization and auto network parallelization

The code to parallelize via threads and via network should be the same.

Can we identify when code diverges from the data it uses and use this to parallelize?

For example, the following code diverges at mergesort() lines.

Any method call can be a future.

```
import numpy

def mergesort(items):
  return _mergesort(0, len(items), items, list(items))

def _mergesort(start, end, items, output):
  print("start", start)
  if len(items) <= 1:
    return items
  
  left = 0
  right = len(items)
  mid = int(len(items)/2)

  left_half = _mergesort(start, start + mid, items[left:mid], output[left:mid]) # can parralelize here
  right_half = _mergesort(start + mid - 1, start + right, items[mid:right], output[mid:right]) # and parallelize here
  
  
  
  left_item = None
  right_item = None
  
  
  # use the output of left_half here, so need to join thread
  if len(left_half) > 0:
    left_iter = iter(left_half)
    left_item = next(left_iter)

  # use the output of right_half here, so need to join thread
  if len(right_half) > 0:
    right_iter = iter(right_half)
    right_item = next(right_iter)

  pos = 0
  
  while (left_item != None or right_item != None):
    
    if left_item != None and right_item != None:
      if left_item >= right_item:
        output[pos] = right_item
        
        pos = pos + 1
        
        
        try:
          right_item = next(right_iter)
          
        except StopIteration:
          right_item = None
       

        
      elif right_item >= left_item:
        output[pos] = left_item
        
        pos = pos + 1
        
        try:
          left_item = next(left_iter)
        except StopIteration:
          left_item = None
        
        
    elif right_item == None:
      output[pos] = left_item
      
      pos = pos + 1
      try:
        left_item = next(left_iter)
      except StopIteration:
        left_item = None
      
    elif left_item == None:
      output[pos] = right_item
      
      pos = pos + 1
      try:
        right_item = next(right_iter)
      except StopIteration:
        right_item = None
      
  return output

print(mergesort([8, 7, 5, 4, 2, 1, 6, 10, -1]))
import math
from concurrent.futures import ThreadPoolExecutor
class Context:
  def __init__(self, items):
    self.pool = ThreadPoolExecutor(len(items) - 1)
  

def mergesort_concurrent(items):
  context = Context(items)
  return _mergesort_concurrent(context, 0, len(items), items, list(items))

def _mergesort_concurrent(context, start, end, items, output):
  
  if len(items) <= 1:
    return items
 
  left = 0
  right = len(items)
  mid = int(len(items)/2)

  left_future = context.pool.submit(_mergesort_concurrent, context, start, start + mid, items[left:mid], output[left:mid])
  right_future = context.pool.submit(_mergesort_concurrent, context, start + mid - 1, start + right, items[mid:right], output[mid:right])
  left_half = left_future.result()
  right_half = right_future.result()
  
  
  
  left_item = None
  right_item = None
  
  if len(left_half) > 0:
    left_iter = iter(left_half)
    left_item = next(left_iter)

  if len(right_half) > 0:
    right_iter = iter(right_half)
    right_item = next(right_iter)

  pos = 0
  
  while (left_item != None or right_item != None):
    
    if left_item != None and right_item != None:
      if left_item >= right_item:
        output[pos] = right_item
        
        pos = pos + 1
        
        
        try:
          right_item = next(right_iter)
          
        except StopIteration:
          right_item = None
       

        
      elif right_item >= left_item:
        output[pos] = left_item
        
        pos = pos + 1
        
        try:
          left_item = next(left_iter)
        except StopIteration:
          left_item = None
        
        
    elif right_item == None:
      output[pos] = left_item
      
      pos = pos + 1
      try:
        left_item = next(left_iter)
      except StopIteration:
        left_item = None
      
    elif left_item == None:
      output[pos] = right_item
      
      pos = pos + 1
      try:
        right_item = next(right_iter)
      except StopIteration:
        right_item = None

  return output

print(mergesort_concurrent([101, -4, -3, 8, 50, 7, 5, 4, 2, 1, 6, 10, -1, 60]))  
  
```

The second kind of parallelism I want to autoparallelize is interleavings between subsystems.

We often want to do one thing while doing another.

For example, I want to loop over files, deduplicate, archive, encrypt and upload them.

You can be doing all these tasks in a pipeline in parallel.

We can turn loops into pipelines and run them in parallel. For example:

```
Files = []
File_data_cache = FileDataCache()
For item in Io.listfiles(backup_locations):
 File_data = read(item)
 Deduplicated_data = File_data_cachd.deduplicate(file_data)
 Encrypted = Encrypt(deduplicated_data)
 For upload_destination in destinations:
   Upload(encrypted, upload_destination)
```

This can be turned into the following code.

```
ThreadPool tp = new ThreadPool();
File_list_rbp = RingBufferPool(backup_locations)
File_data_rb = RingBuffer()
DefuplicatedData_rb = RingBuffer()
Encrypted_rb = RingBuffer()
UploadDestination_rbp = File_List_rbp.newRingBufferPool(destinations)
class Pipeline:
  def __init__(self, context, data):
    self.context = context
    self.data = data
  Def set_source(self, source):
    Self.source = source
  Def set_destination(self, destination)
    Self.destination = destination
  Def set_work(self, work):
    Self.work = work
  Def run():
    While (true) {
      While (self.source.sequence > lasttaken) {
        Item = self.source.data.pop()
        Result = Self.work(self.context, item)
        Self.destination.push(Result)
        lasttaken++
      }
    }
  def push(data):
    self.data.push(data)
    
Class PipelinePool:
  Def __init__(self, data):
    self.data = data
    For item in data:
      Self.workers.append(Pipeline({}, RingBuffer())
      Self.downstream = []
      
  Def from(self, fn):
    for data, pipeline in zip(self.data, self.workers):
      fn(pipeline)
      item.push(data)
      
  Def newThreadPool(self, data):
    For item in self.workers:
       DownstreamItem = PipelinePool(data)
    
       Self.downstream.append(DownstreamItem)
  Def fromThreadPool(self, data):
    For item in self.downstream:
      item.newThreadPool(data)
      
  Def push(self, pushed):
    For item in self.workers:
      item.push(pushed)
      

     
Class PipelinePoolWorker:
  Def __init__(self, pipeline_pool, index):
    Self.pipeline_pool = pipeline_pool
    Self.index = index
  Def run():
   lasttaken = 0
   While (true) {
     
     While (self.pipeline_pool.workers[index].sequence > lasttaken) {
        Item = self.pipeline_pool.workers[self.index].pop();
        Result = Self.work(item)
        Self.destination.push(Result)
        For downstream in enumerate(self.pipeline_pool.downstream[self.index]):
          downstream.push(item)
        lasttaken++
      }
   }
Files = []
File_data_cache = FileDataCache()


def read_data(context, file_location):
  return open(item).read()
  
def deduplicate_data(context, data):
  return context.File_data_cache.deduplicate(file_data)

def encrypt_data(context, data):
  return Encrypt(data)

head = PipelinePoolWorker(Io.listfiles(backup_locations)):



def create_pipeline(file_location_pipeline)
 
 
 read_data_pipeline = Pipeline(File_data_rb)
 read_data_pipeline.start()
 file_location_pipeline.set_destination(read_data_pipeline)
 read_data_pipeline.set_work(read_data)
 
 
 Deduplicated_data = Pipeline({"file_data_cache": file_data_cache}, DefuplicatedData_rb)
 read_data_pipeline.set_destination(Deduplicated_data)
 Deduplicated_data.set_work(deduplicate_data)
 Encrypted = Pipeline({}, Encrypted_rb)
 Encrypted.start()
 Deduplicated_data.set_destination(Encrypted)
 uploads = PipelinePoolWorker(UploadDestination_rbp, destinations)
 uploads.start()
 Encrypted.set_destination(uploads)

head.from(create_pipeline)
```

# 112. Compiler as a service (Supercomputer compiler)

There's always a better approach to solving the problem that your code tries to solve.

Writing a compiler optimisation should be as simple as querying a database and inserting records for coordination of layers or introducing facts.

Or match expressions trees against patterns and more efficient patterns as replacements.

The optimisations we write can be really inefficiently described but due to Algebraic view materialisation, they can be optimised away to be fast.

I think everything can be subsumed into a compiler step: microservices, disks, database schema, clientside code, promise pipelining, ondisk/network serialisation

Even your Kubernetes config, database indexes, database queries, communication and data access patterns should be inputs to the compiler.

# 113. Direct view tracing

Render code ran in a direct fashion.

In other words if you are using tracing, you can read the logs as the actual code that executed, rather than plaintext logs.

# 114. Thread from

The compiler can generate code and weave the synchronization queues as talked of in the previous ideas

We often want to run code from the context of a thread.

Assume the thread is in a while true loop. You need to enqueue things on that thread and synchronize work.

So I should be capable of writing:

```
Min(threads.id) {
 For work in queuedWork:
  Do_work(work)
  Work.threadId {
    Work.callback()
  }
}
```

This code serializes working on data structures and would schedule callbacks between them without explicit locking.

```
Class Worker extends Thread {
 private MultiConsumerMultiProducerQueue queue;
 public AtomicInteger threadId;
 private List<Worker> workers;
 private AtomicInteger min_thread = new AtomicInteger(1);
 private AtomicInteger idGenerator;
 public int stableThreadId;
 public Worker(AtomicInteger idGenerator, int stableThreadId) {
  this.idGenerator = idGenerator;
  this.stableThreadId = stableThreadId;
 }
 
 public void run() {
  While (true) {
   threadId.set(idGenerator.getAndIncrement());
   While (queue.isEmpty()) {
     Thread.yield():
   }
   WorkItem workItem = queue.peek();
   If (workItem.stableThreadId == stableThreadId && workItem.type.equals("callback")) {
     workItem.callback();
   }
   while (threadId > min_thread.get()) {
    int min = min_thread.get();
    for (Worker worker : workers) {
      Int workerThreadId = worker.threadId.get();
      if (workerThreadId < min) {
       min = workerThreadId;
      }
    }
    Min_thread.set(min);
   }
   WorkItem workItem = queue.pop();
   If workItem.type.equals("queuedWork") {
     for (WorkItem work : workItem.items) {
       work.work();
       queue.push(new WorkItem("callback", work.callback));
     }
   }
  }
 }
}
```

# 115. While do parallelism and automatic thread pools

We want to achieve perfect use of the processor and handoff between tasks.

In [ideas3 50. Capacity planning tool](https://github.com/samsquire/ideas3#50-capacity-planning-tool) I described a timeline that you can drag work into and binpack work into time. Most web frameworks produce very inefficient binpacking of work into time, due to blocking behaviours and lack of parallelism.

We want to binpack code and tasks to run with maximum freedom of variable and shared memory usage. The computer should work out how to schedule and order the memory parallelism.

Unfortunately writing multithreaded code is clumsy. It is difficult to handoff work between threads and synchronize explicitly.

So I propose a syntax `parallel while { # blocking code } do { # multiplexed code }` for parallelism.

 * Parallel while blocks are hoisted and converted into two-level thread pools.
 * Blocking calls (syscalls and IO) are executed in a new thread. The `parallel while` syntax is a combined (a) while loop and (b) a thread pool submission.
 * The blocking thread hands off to another thread in the `do` part of the loop.
 * The while part blocks and schedules a thread to handle the do when it unblocks.

The while loop can therefore run at very fast speeds without being blocked.

A compiler can statically analyse the code to decide what thread pools to create. In effect each `do` is an independently scheduled threadpool.

The do code runs in parallel do the while. The do can be independently scaled up and down by number of threads and multiplexed over kernel threads.

The following code allows multiplexing connections over multiple threads and independent reading and writing from epoll.

```
Sockets = {}
Socket = bind("127.0.0.1:5006")
Parallel while {
 Socket, Fileno = Socket.accept();
 Metadata = {"fileno": Fileno, "socket": socket, "sendqueue": RingBuffer()}
 Connections.append(metadata)
 sockets[Fileno] = socket
 connections[Fileno] = metadata
} do {
 
 Parallel while {
  Events = Epoll()
 } Do {
  Parallel for fileno, event in events:
   If event & EPOLLIN:
    Parallel while {
     Received = sockets[Fileno].recv(buffer, 1024)
    } Do {
     Parallel for line in Received.split("\n"):
      Dispatch(line)
      connections[Fileno]["sendqueue"].push("OK")
    }
   If event & EPOLlOUT:
   Parallel while {
    Parallel for data in connections[Fileno]["sendqueue"]:
     
     Sockets[Fileno].send(data)
   }
 }
}
```

This idea is based on the philosophy that the tip of execution shoul never block and when we want to create the illusion of blocking, we use an event loop in a thread, but the progression of the program as a whole is always moving forward and progressing. The frontier of execution is always processing events.

# 116. Configuration addition search

# 117. Rules for concurrency and parallelism

* Compare and set is enough to build a safe but inefficient concurrent algorithm. Especially if you want to enforce atomicity over multiple fields. You actually want to enforce a partial order. Use nested monitor pattern and signal/condition variables or multiversion concurrency control.
* Don't iterate over a data structure from one thread while it can be modified by another thread. Use persistent data structures and immutability or multiversion concurrency control.

# 118. Cross merge

Cross merge is a construct used with `parallel while { } do { }`

To handoff behaviour when all child tasks are finished.

```
A1 = Parallel while {
 documents = Fetch("http://server/documents);
 Parallel for response in documents:
  Document = fetch(response);
} Do {
 Words = Document.split(" ");
 Set(Words)
}
A2 = Parallel while {
 Posts = Fetch("http://server/userposts")
 Parallel for post in posts:
  Post = Fetch(post)
 } Do {
  Words = Post.split(" ")
  Set(words)
}
document_words, post_words = Crossmerge A1 A2
Document_words.union(posts_words)
```

# 119. Read/write Ticks

You don't need to worry of thread safety is everybody else is reading while you're writing and everybody is writing while you're writing.

This approach uses a RingBuffer to communicate READ/WRITE tick. Threads dequeue from the RingBuffer, when every thread has dequeued from the RingBuffer, a new event is placed on the RingBuffer for the next cycle which is a READ if the last was a WRITE or WRITE if the last cycle was a READ.

Bloomlang uses a similar approach.

See my multiplexing repository for a design of a multiplexing event system that uses read/write Ticks.

# 120. Cancellation trees

IntelliJ is very laggy software. It doesn't execute processes on different threads but in the GUI rendering thread. As a result it lags while creating intellisense suggestions.

I propose a GUI framework that uses register loop to create full cancellation trees of operations, where every tree node is a parent of a child operation. Any node has a validity that can be cancelled when the user does something to invalidate the GUI state. For example, the GUI should show a pending intellisense that can be cancelled. This means you can abort any action on the computer.

# 121. Spreadgrid

# 122. Avenues of research

 * Upgrading a database is very difficult to do without downtime. I feel any new database or general software should try and solve this core problem.
 * Decoupling release and deployment. Zero downtime deployments are easy with PHP but very difficult with software that runs endlessly, as a server. How do you atomically update a system without downtime?
 * Android Google Chrome edit performance on textareas lags the larger the document gets. I edit this document on my phone most of the time.
 * Fraud prevention


# 123. Plain English pointer types

C programming pointers and arrays are subtle. And calculating size of a struct or a pointer is subtle.

Sometimes code can be obviously wrong and sometimes it's not.

I propose a plain English syntax for referring to pointers.

Referring to struct Structure name** pointers would be written as array of struct pointers.

# 124. Complexity reduction, Re-entrancy, tip of execution hierarchy, blocking

 * Re-entrancy and blocking are often invisible in the programming language syntax with the exception of async/await.
 * You want assurances that nobody can be mutating data at the same time as you. Sometimes it doesn't matter. The computer could work it out.
 * The tip of the execution is what is executed next: it is what what code is next in memory. It is often managed by stackframes. The control flow of programming and tape allows us to be Turing complete.
 * Software is slow due to being trapped by by the complexity of stackframes. To change the behaviour of a program you need to change the algorithm - of what happens when and where and how. To change a program to be fast you need to understand the problem you're trying to solve, and that often requires a completely different stack of stackframes and algorithmic approach.
 * In Haskell the idea of defining the problem as a definition is really powerful and leads to accurate powerful code. But we can implement primitives to a higher level of definition than even Haskell. Containers, methods, functions, processes, Kubernetes, threads, Cron are all approaches to arranging what should be done at the tip of execution and how it should be layed out and arranged.
 * The tip of execution is what goes on next. Many problems can be respecified at a high level of addition, subtraction, division and multiplexing and monads and application and change. The computer should work out the efficient implementation automatically based on the relations you specify.
 * Each of the previous point's categories of the tip of execution can be multiplexed and assigned a type for an idea.
 * Ideas have relations.
 * Looping forever and programs that process all events in one instant are two really powerful primitives for building systems. Bloom Lang and [my multiplexing repository](HTTPS://GitHub.com/samsquire/multiplexing) uses this design.
 * Relations can be ordered and scheduled and the tip of execution can be scheduled efficiently.
 * Relations can form a graph.
 * Graphs are trees
 * Programming syntax is a tree
 * Abstract syntax trees are relations and orderings.
 * Trees can define execution on a computer.
 * CPU Instructions define what should go on.
 * Relations can be recursive.
 * Relations can be logical.
 * Some things are faster than other things. You can define logical statements of what is more efficient. Setting up threads in advance of using them is faster than creating a thread when you need to schedule work in parallel.
 * You can separate things into different classes of things: you can run the tip of execution in a thread or in a container.
 * Things have dependencies.
 * Things can be scheduled.
 * Caches cause things to be faster
 * A process implies a thread. Kubernetes implies a container.
 * The hierarchy of the tip of execution can be generalised to have the same interface, it can be scheduled and multiplexed.
 * Scheduling the tip of execution can be at compile time, ahead of time or at runtime. There are costs are flexibilities of each.
 * Compiling and interpreting are two sides of the same problem: the tip of execution. Compiling decided what to do in relation to a program tree in advance of its execution whereas you can also decide what to do at runtime at cost.
 * We can compile as we go as we learn of our data. This is what a cost based optimiser in a database does.
 * We depend on the abstraction of tape (memory positions) and evaluation of instructions. So we suffer from concurrency and parallelism issues. Mutability and aliasing is important for safe concurrency and parallelism.
 * We can model programs as either reading or writing a location or not if critical section/regions never overlap and are partially ordered we avoid parallelism problems.
 * Parallelism and concurrency should be resolved by the computer (compiler) the autoparallelised solution is defined in the problem specification or the algebra of what you're trying to do.
 * We can overspecify a system. If there are 100 relations that you want to enforce and you know how to write instructions on how to implement each of them, you should be capable of writing an inefficient implementation and overspecify it.
 * When the computer has instructions on how to calculate something, can it merge the relations into one to create a data model that works efficiently for all relations.
 * A depth first search implementation for one thing and a division relation can be merged.
 * In one scenario you need a DFS relation and in another you want a group relation or a some pattern.
 * Instructions are statically analysable.
 * How do you satisfy all relations simultaneously?
 * If every program is a query, you can find the common elements of each query and move the tip of execution to where it is efficient.
 * Data in two different shapes can be marked as equal.
 * Equalities can be maintained with work. Or lazily generated.
 * The algorithm to turn one equality to another is generatable by a computer. As the data shape is defined by relations. Such as an object graph. Usually it shall be resolved by iteration, traversal, or storage.
 * Relations can be transformed.
 * Computers are good at storing data and data has relations. You want to maintain parallel relations: each corresponds to a query.
 * Data can be filtered.

# 125. Whole program optimisation

 * Symbolic algebraic equations can be simplified.
 * If we can represent algorithms as their algebraic foundations, we can create peephole optimisations for subproblems.
 * Malloc does clever things to manage the management of free memory. For example it stores the size of the available free memory after each chunk. This way it can do calculations as it goes. The general pattern to optimisation in this case is laying out things nearest to where you use them.
 * Data layout and data structure and algorithm are all separate problems.
 * Data structure is the relations between data layouts and an algorithm is the instructions for processing that data layout of data structure.
 * Can we represent instructions as nonfungible numbers or symbols?
 * a + b evaluates to the same as b + a. But they are not the same.
 * Factors are multiplications. What does it mean to multiply an instruction? Is it a loop?
 * Instructions execute in relation to time. There is a dimension of time and there is a different instruction being executed at each time interval or cycle and there is a position that the instruction is at in space. There is also the state of every piece of data in memory.
 * We want to optimise the production or application of functions or algebraic equations.
 * There is the mathematics of change. Such as integration and differentiation. There is also change in memory over time.
 *

# 126. Loop Invariant expressions and induction at the tip of execution

If you can refer to anything in your current expression, you have maximum expressivity.

If you can declare behaviour at your current expression and define what something is, you can always create forward progress with your program.

The question is how to optimise this approach.

A loop represents an overconstrained evaluation of a whole set. Sometimes we only want to do partial loops, from the context of an inner expression.

For example a sudoku solver could maintain list of potential numbers for each cell.

It needs to eliminate options through impossibility. It should start with the most overspecified rows and columns first.

You can either do this in one whole step, which is inefficient or do it piecemeal in an ordered fashion when you try out an answer.

I need a when operator. Rather than think of programs as serialised steps to getting to an output, we define expressions and when clauses over them.

For recursive backtracking in a sudoku solver, we can reject and return explicitly to different control paths from a different perspective.

When we detect a solution is impossible we explicitly write a reject statement which aborts control flow.

So we want to order loop subiterations. When does a loop iteration become relevant?

So I propose loops are queries and are specifications of what should be true, but they are lazily evaluated for efficiency.

You can in effect select over a loop. Or provide a when clause to a loop.

Essentially control flow is in and out of a loop at different intervals depending on what triggered the invariant.

An if statement in a loop can be transformed to two separate loops at the cost of memory.

Ahead of time compilation can speed up code if we put decision points in our code.

We want to weave control flow between specifications of expressions or invariants.


# 127. Community Idea: What's it good at: Solved problems

Each programming language, tool, system and software is good at representing and solving particular problems.

But this isn't really documented anywhere.

I can save a lot of resources by picking off the shelf solutions to problems. But it's not always clear what you can use for your problems to go away.

# 128. Loop compilation

I've sometimes wanted to generate code rather than insert a loop with an if statement. It's probably more efficient to partition a loop and generate machine code for it.

# 129. Update first software

Imagine we have a website similar to Repl.it, Jsfiddle and Jsbin.

It provides a database or file system and allows migrations to be defined.

It should be opinionated regarding handling updates. Creating a release should be a button press.

Restoring data at a previous version should also be available easily.

Updating software is painful. Usually to upgrade we bump the version number and then fix compilation errors and then run the tests.

Unfortunately for systems that store data this is not enough of a fix.

We need to migrate our data to the new approach to storing.

I propose software is shipped with a special upgrade endpoint that allows you to register network address of the server you're upgrading to.

Then the database is checkpointed at the point the upgrade began and an upgrade is started in the background, data in the database is migrated to the new server.

When old data is migrated, the data since the checkpoint is also streamed across. Then from this point the old database forwards requests to the new system.

Two sets of load balancer can be used as an alternative to the old version streaming changes across.

Timing is essential with any upgrade. I want software to be updateable from day 1 of development. Semantic versioning is a hygiene rule, not every product follows it. And when upgrading software timing is of the essence. I want to decouple upgrade from timing and cause them to be automatic and seamless.

# 130. Behaviour trees and configuration as pseudocode

Imagine if the configuration file for a system was an imaginary pseudocode for that software's primary function.

 * For example the pseudocode for Haproxy is a while loop accepting connections and then a while loop handling http requests and forwarding them to chosen backends 
 * You could add logging by adding a log line. Or enrich or conditionally change the value of variables in the pseudocode.

 * You could be restricted from changing the order of the pseudocode but you could place if statements and custom processing anywhere

 * Internally the statements between the fixed behaviour of the program would be turned into hooks at various stages of the application.

 * Kubernetes would look like a while loop that tried to get nearer to the desired state and would pick a pod and pull a container and set up networking.

A modern stack of software is files, processes, loops, threads, network buffers, containers, storage and a sequence of instructions executed by a CPU.

What if you want to overlay behaviour over existing functionality? I want to map computation to computation.

Do another thing while doing the existing computation. Or do the existing computation in a slightly different approach.

For example, you might want to loop over running loops and iterate over them only some of the time. Or load balance them or backpressure them.

Or decide what the behaviour should be.

 * For files it would be what to write to the file, what locations to look for?
 * For containers it would be pull strategy, image name, sidecar, volumes


Take Kubernetes for example, each field in the YAML causes a slightly different behaviour but YAML is arguably the wrong data structure for deciding an imperative operation.

 * What I want to see is the overall loop and customise parts of the loops.

 * Perhaps you could look at a GUI of a behavioural tree of a garbage collector or a web browser. This should look like JMX GUI.

 * You would see all the functions running and a high level perspective of what the software is doing.

 * Perhaps you would visualise it as a grid and a tree. The grid shows the various objects there are and the state's they are in.

 * Most of the state transitions shall be too fast to track by human eye. But we can turn a state transition into a list.




# 131. Concurrency tester

I want to simulate the interleaving and simultaneous execution of N Java programs and see if the program is correct.

I could use TLA+ but I want to think of a low tech solution.

# 132. Revenue scaling plan

Cloud computing changed how we think of scaling and costs in providing IT but we can go further.

Imagine if there was a function that took in a financial amount and number of concurrent users and could map to an infrastructure that scales to that many users. £5, £10, £100, £200, £1,000, £10,000, £1,000,000 all map to different amounts of users and different infrastructure to support them.

# 133. Concurrent loops - loops as lightweight threads, load balancing loops

Loops are NOT first class citizens in code.

They should be passable around similar to functions.

They can even run concurrently.

```
For letter in ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]:
 For number in range(0, 10):
  For symbol in ["÷", "×", "(", ")", "&"]:
   print(letter + number + symbol)
```

The problem with this loop is that letters and numberd are starved of resources while the inner loop for symbols is running.

What if we want this effect.
 * The Cartesian product is produced but in an evenly spread out order
 * Any part of the loops can be paused. If I pause the outer loops I get the same behaviour as the naive for loop.
 * If I pause the middle loop, we don't process so many items from that loop.
 * I can start and resume different parts of loops and switch between multiple loops. I can schedule loops

```
A1÷ 1 1 1
B2× 2 2 2
C2( 3 3 3
D3) 4 4 4
A2( 1 2 3
B3( 2 3 4
C4÷ 3 4 1
D0× 4 1 2
C2÷ 3 2 1
B1( 2 1 4
A4( 1 4 3
D3× 4 3 2
```

Here is code that represents a arbitrarily nested number of loops over collections.

It also load balanced the loops and runs them in an evenly spread out Cartesian order.



```
class Tick:
  def __init__(self, collections, func):
    self.collections = collections
    self.n = 0
    self.func = func
    
    self.current = []
    for item in range(len(self.collections)):
      
      self.current.append(0)
   
  def size(self):
    total = len(self.collections[0])
    for collection in self.collections[1:]:
      total = total * len(collection)
    return total

  def tick(self):
    
    items = []
    n = self.n
    self.indexes = []
    
    
    # reversed to match order of itertools.product
    for collection in reversed(self.collections): 
        n, r = divmod(n, len(collection))
        self.indexes.append(r)

    
    for loop in range(len(self.collections)):
      previous = 0
      for mod in range(0, len(self.collections)):
        previous = previous + self.indexes[mod]
      
      self.indexes[loop] = previous % len(self.collections[loop])
      

    for loop, item in enumerate(self.indexes):
      items.append(self.collections[loop][item])
    
    self.n = self.n + 1
    return self.func(items)
  
a = ["a", "b", "c"]      
b  = ["1", "2", "3"]
c = ["÷", "×", "("]

def printer(items):
  output = ""
  for item in items:
    output += item
  return output

ticker = Tick([a, b, c], printer)
print(ticker.size())
for index in range(ticker.size()):
  print(ticker.tick())

print("CORRECT")
for letter in a:
 for number in b:
  for symbol in c:
    print("{}{}{}".format(letter, number, symbol))
```

I propose the following methods be available on loops:

Nested loops can be visualised as a tree, so there are variations to the order we can process the loops. For a tree of 3 nested loops the trees looks like this:

```
A # Ask for As only
 B
  C

B # Ask for B's only, iterating A necessarily
 A

C # ask for C's only, iterating B and a necessarily
 B
  A
 
```

What of loops at the same level, that is, loops at the same level. It causes no difference if the 2nd and 3rd loop are iterated out of order.

```
for letter in letters:
 for number in numbers:
  print(letter + number)
 for symbol in symbols:
  print(letter + symbol)
```

The product of this looks like this:

```
a1
a÷
```

# 134. Virtual processes and scheduling

A process is a collection of loops, some nested, some independent and some dependent on eachother.

We can build a tree of loops and run all the loops concurrently. This gives us concurrent processes that can independently progress.

This is similar to Erlang but the practices of Erlang could be generalised and applied to any programming language, even those without native thread support. This is probably similar to continuation passing.

Combined with concurrent loops we can produce virtual processes.

Each process has an inbox, you essentially have two processes linked by a concurrent loop.

```
Input_work = []

A = Process()
B = Process()
C = Process()
J = JoinProcess()
D = Process()
processes = [A, B, C, D, J]
A.link(B)
A.link(C)
B.link(J)
C.link(J)
J.link(D)
s = Supervisor(processes)
```

Supervisor needs to create this nested loop:

```
for item in A:
 A_output = A.process(item)
 B.submit(A_output)
 C.submit(A_output)
 for item in B:
  B_output = B.process(item)
  J.submit(B_output)
 for item in C:
  C_output = C.process(item)
  J.submit(C_output)
for item in J:
 D.submit(item)
```

# 135. Recursive coordinations and decision portfolios and time allocation portfolio and recursive dividends

If 3 people work separately and produce the output value of 3 each time we result in 3+3+3 = 9. If 3 people coordinate and work together, the effect is multiplicative 3×3×3 = 27. Unfortunately coordination is costly. (It is also costly for parallelism performance) Think what W3C, ISO, WHATWG and every consortium and most committees suffer. They suffer from coordination problems. Standardisation efforts suffer and are delayed due to a back and forward over issues and communication. Committees are also slow and complicated. I propose to scale coordination by breaking it down. If two people can coordinate, that is good. If you add people to that coordination, the value of the coordination grows. We can build coordinations separately and isolatededly.

Imagine a system or social network where everyone announces what they are going to do before doing it. Imagine a work management system that was also a constraint solving system and scheduler. At the beginning of everybody's workday, task or project -- within a company, publicly, internationally, within families and within open source products -- people write what they are going to do. Then they do the work, then after they do the work, they check the system for what people suggested would benefit them. People are encouraged to share what would benefit them. The understanding being that this is not a light statement to add what would benefit you, this is a also a commitment for mutually beneficial exchange: you need to offer something in return. You reply to the work that someone is doing with the intention of using it and benefitting from it. You propose how you would benefit from it and how the work's deliverable should be changed to benefit you. You are also required to provide something in return for the change.

When you submit what would benefit you and agree to a commitment, your exchange is added to a portfolio. You track the returns of your portfolio. You can add more investment to the commitment. If a work is public, other people can join the commitment and add more multiplicative effects to it.

You can also add decisions to the system and you have a portfolio of decisions which you can review and analyse. We can add causes and effects to those decisions and track the results over time.

There's 8 billion people on the planet and each of those people has countless problems and potential value to provide in return for solving other people's problems. There's a solution through multidimensional space that provides profit or benefit to as many groups of people through recursive effect and recursive relationships. If you do this for me, I'll do this for you.

There's a win-win state of affairs through co-operation and coordination. Trade and profit raised through work is spent in the overall economy and ripples out to other people, if you limit this to a smaller group, everybody in the group benefits. Trade produces value in excess of its inputs. We should capitalize on all the work we do.


For maximum effect and return, if multiple individuals did not see their work as being isolated, they could coordinate and multiply their effects with other people doing the same thing or people who want to benefit from those things.



People reply with how they could see that work solve their problems.

The author decides to fulfil a coordination, the coordination is added to both of their portfolios.



A slightly different arrangement could benefit multiple parties simultaneously and improve things for everybody.

I think of this problem as numbers that are multiplied in every direction, providing a sum that is greater than all its parts. That's what proper coordination is. If you multiply one number by 1.01 you grow by 1%, if everybody adds to the whole, the multiplied product is much greater than the sum of its parts.

There is an time ordering that is an evenly spread out Cartesian product of everybody's coordinated problems. With this product, everybody gets attention but the business does not fail to operate on it's own responsibilities.

Recursive dividends means you get what you cause. You should return a fraction of that change or scheduling's return. We can use the learning function of a neural network to produce returns to people who cause things.

# 136. The Show, don't tell problem and many failed lineages problem

In every company around the world the company has a technical problem, then someone is employed by the company and that person solves the problem technically. This is repeated ad infinitum throughout time. Very few of these technical solutions escape as a lineage from the company, so the same work gets reinvented again and again.

Think how many Github projects there are and all the wasted effort from projects that go nowhere. I don't accept that technology should work in this manner and that the knowledge of the solutions go with the people that built them and do not percolate through industry or add to the knowledge of society.

Think of operating system, programming language and web browser lineage and genealogical trees, it's forward marching line of progress as each split adds something to the whole. The problem is that things don't get merged back, so we collectively lose so much untapped value in society.

The second problem is the show don't tell problem. To work on one thing is to work on the exclusion of everything else, an opportunity cost. If you tell people what you're going to do, and spend all your time designing a perfect solution you'll never finish, so nothing gets done if you tell. So ideas that people talk of don't get implemented, the people who do the work decide the future. The problem is to get investment, you need to tell others what you're going to do. So this is a stalemate and the reason why most businesses and software projects fail.

# 137. A scalable system design

Imagine a tree of load balancers, one in each availability zone and across multiple regions with GTM being programmed so every load balancer is aware of every other load balancer in every other region and availability zone.

I plan to use PowerDNS with the pipe backend. When a DNS query is resolved, it checks the remote IP address and responds with a round robin IP address of the server that is nearest the region of the requesting IP.

# 138. Code movement API

Think of the different segments or contexts that code can execute in: in a loop, in a method, in a thread, in a process, in a container, in a language virtual machine or on a hypervisor virtual machine.

Imagine you could schedule code into each of these contexts with a MV command.

# 139. Incremental scaling

When designing scalable systems we generally design the end state of how the scaled system should look.

I propose a different much harder problem to solve.

Incrementally scale a system through changes to the running system without much service interruption.

Write code that takes a system from single availability zone to multi availability zone then multi region.

# 140. Survival management

Most ideas fail when a critical person stops doing what they were doing.

If we want things to keep going, we need to invest effort into keeping them going.

Imagine a system that tracks attributes of survival and allows people to add to the whole to keep something surviving.

# 141. Algebra for shape addition

Adding YAML to existing YAML is a validation problem, I wonder if algebra can cause it to be easier?

# 142. Scale game

A virtual cloud environment that simulates problems and has a build button to build different architectures.

Simulates users using the system and simulates failures.

# 142. Dream compiler

 * **Intellisense web** At any given point in a compiler input stream there is a sequence of what is valid. I would like a GUI to show me these things.

# 143. Metaphorical programming - cars

A metaphorical observability of code. Each car is driving around on roads between components.

I can see the flow of data between components

 * I can change the width of roads, the length of roads.
 * I can introduce crossroad junctions, T junctions and roundabouts
 * I can introduce motorways/highways which are fast paths and lanes which are slow paths.

I would have lined represent the tip of execution.

# 144. Memory hierarchy and computation flow analysis

Ideally you want to be processing data while reading it from IO or the network.

We can process data in batches. The batch size needs to be large enough to be worth running in parallel.

# 145. Practices

 * **

# 146. Communication Subsumation

Represent all the communications between functions,

# 147. Intelligent shard routing and data shift

From a very high level we want data that is relevant to be stored together, so accessing it is fast.

We can route data to a shard based on efficiency.

We write web request handlers to handle and route requests.
We can also write handlers that define the destination of data.

These can be dynamic handlers if the output of any changes, we move the data.

Rather than be a system that decides where to store the data and store it, it's a regularly rerunning system that evaluates where data should be.

# 148. Function marketplace

# 149. Communication to shared memory and automated communication analysis

[Scalability but at what cost?](http://www.frankmcsherry.org/assets/COST.pdf)

Communication is extremely expensive from a CPU perspective. We shouldn't need to communicate if we can avoid it. Microservice architecture has very little mechanical sympathy.

We need to have a very good reason to export processing to another computer if the processing can all occur on a single machine. Communication is equivalent to explicit synchronization from a parallel and multithreading perspective, it slows everything down. Enforcing order is expensive from a distributed system perspective, ideally you want every machine in a network processing at maximum speed on its problems or work, when you communicate, you stop work on two machines to pass work between them. Communication represents serialization of causality. The single threaded performance of a computer is extremely fast if all the data for a task is on one computer. The reason to communicate is to scale or provide flexibility of architecture.

If data is too large for one computer, we can distribute the processing and storage for a disaggregated architecture. When data is too large, we need to shard and aggregate results. The work dispatch has a submission roundtrip time and processing time and reply time.

If every server runs every microservice as in [ideas4 # 104. Multistack Microservice Pattern](https://github.com/samsquire/ideas4/blob/main/README.md#104-multistack-microservice-pattern), then we can partition the state of a microservice's datastore across multiple machines and still scale compute and storage.

When we receive a request we can design our system so that all the data is already on the server where the request was received so no further communication is needed to fulfil the request. If the data is too large to store on one server, we could have a convention where clients know of the shards they must relay their requests to to retrieve the full dataset, and each machine fulfils its partition of the data.

If the data is spread over the network, how do you present a cohesive view of all data in one interface?

If every Microservice is on every machine with its own database, we maximize throughout at the expense of independent scalability.

Can we break processing into partitions do that each partition uses a maximum of processing on a single machine. I call this Microservice segued. We split the lifecycle of behaviour across shards and have a sunshade for each stage of the lifecycle.

Event brokers can be on a particular shard or on a separate host for communication and decoupling of microservices communication 

Can we feed in all the interactions to a system and tell us how we should binpack our servers?

 * Place communicating Microservices together on same machine with the same data
 * Load balance microservice to microservice traffic. Ideally we distribute to local machine for efficiency.

We can mapreduce load balance heavy tasks by partitioning the problem and sending them to a work pool.

# 150. System as a program and system difference evolution, overconstrained systems and software defined system

This idea:

 * extremely complicated refactorings of systems in traditionally implemented code should be trivial
 * I should be capable of mutating a system while it is running from an old design to a new design easily
 * Systems should mutate to change of design and architecture easily
 * We can use a combination of declarativeness and imperativeness to achieve this goal.
 * Statements such as "There is a load balancer in this availability zone, sharded by this user cookie" should be trivially refactorable to a different layout.
 * I want to declare my system design with imperative code and mutate a data structure from one design to another. So this is a mixture of imperative and declarative code. I want to use one language to do this. I want to create Kubernetes resources, Terraform resources, Dockerfiles, application code, CI/CD pipelines with a program. This is similar to Temporal.
 * 

If we raise the level of abstraction for how we define our system, we can create drastic changes to the system with less impacts than changing a system that is active.

The abstraction should be a definition of the system at a high level and a form of mapping from component to new component.

This should allow us to update our system dynamically.

For example, we can define what should go on to requests we can rerun the function to apply to past storage of past requests.

In other words, our system is reactive to its design.

Event handlers, workflow should be defined with a builder of the system as a whole.

This idea is an extension to how Kubernetes has an API for defining resources and Pulimi and Terraform. The system as a whole should be overconstrained. 

# 151. People circuitry

Conway's law means that software ends up looking like the communication patterns of people who create the software. If we think of a person developer as a component of the architecture, each has IO with other people, a memory buffer of recent code, and a mind that is a central processing unit capable of rapid pattern matching and general purpose problem solving. Individual contributor's are capable of mass outputs see Linux Torvalds, Varnish developer, Guido Van Rossum, Rasmus Lerdorf. Let's take individual potential into thought of the layout of software engineering teams.

Some people build software in layers.

The problem with layers is that layers form a rigid agreement of how things are seen by different layers. If you want a far reaching change you might get the expression problem and need to touch every layer for every variation.

This idea is to think of the person on a team as part of the system and to arrange them In such a way to maximise throughout.

If different people are responsible for different layers then you have a communication slowdown as you inevitably need to communicate to have successful integration.

In Google they produce new chat applications every year. There are different solutions to the same problem in Google's codebase as different teams have different problems to solve and they solve the problem slightly differently.

I see no problem with this if it causes maximum velocity. If it slows down development I would be against it.

This idea is to see the individuals developing the software as being part of the systems design and not just a body shop worker who churns out code.

Every developer is different and has solved different problems in their life. They are better at some problems over others. They have different levels of knowledge.

Some developers have machine sympathy others do not.

Let's arrange people in a circuit and optimise for code production and problem solving. Put two people on a problem and ask them to design a solution and integrate that solution everywhere.

# 152. Migratory systems

# 153. Network Stackless HTTP

Imagine writing all your communication between microservices with a HTTP client that actually uses shared memory to communicate with local microservices. You can fan out and communicate locally for performance.

# 154. Hook

Writing code with a blank slate is easier than writing code with an complicated codebase.

Writing assertions or additional facts is easier than modifying existing facts to do what you want.

# 155. Eventually consistent website - Queuing primitive

When I change a record on a website, we can have a notifications area that says your change is queued.

When the change is applied, the content is updated and the notification changes to being that your change has been accepted.

# 155. Downtimeless systems

# 156. Generalise scalability - Properties based scalability

Can scalability be generalized? Most complicated systems need to manage memory usage, storage usage, network usage and communication. Communication and indirection can be used to scale, at a fixed cost.

Systems have a fixed capacity and generally a fixed single threaded performance (4-5ghz) and a fixed number of hardware thread cores. If we have a N objects that is larger than the system can cope with, we need to divide N into segments and assign them to different machines.



# 157. Flow is how you understand programs

Unfortunately control flow in most programs is a mess. You cannot read code like a story in most codebases as the code goes everywhere. 

# 158. CI/CD REPL Editor

A web based editor that monitors files, and runs Docker builds and CI/CD pipelines on every change. So you can test your entire pipeline automatically. Should also deploy to Kubernetes.

# 159. Serverless Upgrade

Upgrade a serverless system to a server, seamlessly, downscale to functions as a service when idle.

# 160. Try before you buy cloud computing

In my experience of building servers and configuring cloud environments is that it takes a lot of attempts to get something working.

# 161. Cloud IDE

# 162. Protocol manager

In big microservice based systems or systems with lots of protocols, you often need to make a change that ripples out through the entire system. If you have X services you send a message between them you have X message schemas. Let's manage the schemas centrally

Adding a field to a message should be a simple change in a central system. The rest of the system should just adapt to the new field.

In traditional microservice architectures there's either a monorepo or a repository per microservice and each service has to be changed to add the new field.

In this design each service retrieves its schema from a central source and every area where messages are constructed there is a context area. This context area contains all known state at that point in time.

Someone can move a piece of context to the protocol schema centrally. So adding a new column to a database or to a protocol  message is as simple as changing it in one place.

# 163. System tree in IDEs and direct system management

In IntelliJ I find packages and class view in Java on the left hand side to be almost useless. In most codebasees, I find the file hierarchy of files of sourcecode to be useless.
 * People **do not** know how to organise code.
 * Not many people organise code by feature but by kind of thing. Such as controllers, views, services, marshallers etc
 * In refactored codebases, each file does very little.
 * Core logic is spread across the codebase, in different packages.
 * Every codebase organises code differently. Learning one codebase means you learn that codebase's idiosyncrasies.
 * To change behaviour, you need to change multiple classes, every call site and the parameters of lots of methods.
 * You need to pass along data to where it is needed.
 * Dependency injection registries files are incredibly useful in working out how software works.
 * The `int main(String[] argv)` file is useful.
 * Request handler methods are useful.
 * The classes where one component is driven by the context of another component is useful. Such as if you were modifying a database system, you would want to find the code that drives the physical data storage from the logical storage.
 * For a compiler, I would want obvious frontend, backend, middle end, optimisation, codegen areas of code.

What I really want is a tree that gives a list of areas of the software and allows their behaviour to be changed, a bit like an elegant GUI that was designed to edit the software.

# 164. Working with, not against the properties of the creation

I've done some reading of [Joe Duffy's retrospective of Software Transactional Memory](http://joeduffyblog.com/2010/01/03/a-brief-retrospective-on-transactional-memory/).

The reason concurrency and parallelism is hard for people to understand is due to a property of the creation that is against the intuition of how our minds **rationally** operate but our minds depend on its properties to operate. Physics tries to uncover these properties. Causality is interesting in itself. Communication, entanglement, observation, synchronization and causality are all linked together. We exist in a cause and effect creation.

Sorting or orderings are really useful from the perspective of something inside the creation. Lexicographic sorting is really useful. Time is also sorted, there's an arrow of time and it moves forward.

What's so simple that nobody explains? How can we wield how the creation works to write performant, efficient, concurrent and parallel code, correctly and everytime? With the minimal effort and resources?

Ideally computers should automatically do what they're meant to do when they're meant to do it, with the minimum communication. Unfortunately the positional 3D nature of the creation means that light and electrons travel at a speed that is not conducive to immediacy unless they are entangled.

Computers require communication to do things. Communication implies synchronization - one party needs to listen for another to send, fortunately we can listen and send at the same time, unlike speech.

Atomicity can be visualised dimensionally. From one dimension, I see this, from another dimension, I see another thing. I change my position and see different things.

# 165. Alternative parallel while

Imagine we could tell the computer to maximise doing one thing while doing another thing.

```
parallel while {
 char buf[1024];
 os.read("/bigfile", 1024, buf)
}
parallel while {
 lines = split(buf, "\n");
}
parallel while {
 do_expensive_calculation(lines);
}
```

While I'm reading files, I should be doing expensive calculations with each line. Buffers could be intelligently scaled between parts, a bit like TCP window sizes.

# 166. Buyer signal - Commit to buy

Things do not get created unless there is a market for something. The problem is that creating a market for something is expensive. There's a self-referential cycle in the creation process - a cross dependency between revenue, workers and funding. Nothing gets created without funding or bootstrapping. Many startups put up a landing page to gather interest in people who are going to build something. I find this risky. You're under pressure to deliver, to a timescale.

So I propose an imaginary market where people specify their requirements and commit to buy a product that meets their requirements.

# 167. Agreement system

The world could be far happier if everybody agreed with how they were treated.

# 168. Explicit scope and escape specification

I want to specify what is in scope and have the computer work out how it can be efficient.

I want to specify what should be visible to where when escaping things.

# 169. SAAS REPL

Create a SAAS by REPL.

# 170. Technical problem abstraction, Computers need to give people incomes

For a given state, there is a state that follows that is valid or good or useful.

If people were presented with the present state and asked what the next state should be from a selection of choices, people could solve technical problems through abstraction.

# 171. Layout engine derivative

The coordinate positions generated by a layout engine must have a pattern. Take advantage of this pattern for repeating rows or columns.

# 172. Hours app

Why is my work arrangements tied to an employer intranet? Why can't I just pick my hours I want to work on my phone calendar?

# 173. True error code

An error message on authentication is usually sanitized to prevent sharing information with attackers, but the information is profoundly useful from a security engineering perspective. We can create deny events to policies for least privilege security.

# 174. Right maps and Investment boundary app

There's a priori cause to why something went on, observable and non-observable. Businesses are exposed to market forces and the interactions of billions of people. Money movement, interest rates and other economic effects.

If I'm investing money, I want some due dilligence or say how things are to be ran. Venture capital and trusts do this.

# 175. Broadcast what you buy

Imagine a website where you are encouraged to post what you buy and you are paid to do so.

People pay a subscription for data.

You pay for access to the site and for each purchase details.

Data for everyone.

# 176. Deliberate full table scan queries

This is a low tech search. We can apply Aho Corasick and brute force a large data set distributed over many machines. 

We centralise full table scan on a timer and queries are queued up to be processed during the scan. Queries that are queued up after the full table scan starts are paused until the next cycle.

This is faster than doing multiple full time scans at the same time, it's better to saturate IO once than multiple times.

If you have 1000PB of data and it is sharded across many computers, you can scan the data set in cycles. An NVM SSD gives at least 3500 MB read performance. And RAM can be pretty large. So we can rely on sequential read performance to apply the scan to multiple records.

1000 petabytes is 1E+12 or 1,000,000,000,000 megabytes at 3500 MB on one machine, this would take 285,714,285 seconds or 9 years.

It would require 9 years to service a very large number of queries on one machine with 1000PB.

If you sharded the 1000 PB to 10,000 different machines and search each of them at 3500 MB a second it would take 28571 seconds or ~8 hours.

I don't think it's that bad.

# 177. Search absence log

Log what you didn't find in data, so you know for next time.

# incomplete ideas



Memory set to network calls

Distributed systems and parallel processes.

How to atomically update a number on the network.





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
 * Data structure
 * Traversal
 * Query
 * Correlation
 * History
 * Queue
 * Aggregation



Tree programming
Fluent system
Flow control

Things written as communication protocols are easier to program and reason about. Concurrency too (see go and occam pi)
Turn the GUI into a communication problem.
