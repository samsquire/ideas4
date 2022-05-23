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

 * **Errors** become things Errors become a thing in my desktop. They appear in the system tray and don’t go away so easily and they can be re-tried easily. They appear in an error viewer. You can then try solutions against the error to see if it works, it it works, the error will go away. You can see comments about the error and try known solutions to the error. Known solutions are gathered online.

 * **Shared desktop sessions** It should be possible for multiple users to join a desktop session. The session is not single player, reserved for one person but possible for multiple people to join the same session.

 * **Cloud designer** Advertise cloud features to me and let me use cloud features in my home network such as S3.

 * **Advertising features to me** My desktop computer has installed various services and APIs. My desktop should advertise what features are available to me


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
