# A pacer example - Enron emails

Looking for the answers to the fraud, or just looking to leverage the
graph?  This repo provides some example use of pacer, from traversing
the graph, creating vertices + edges, and doing some analytics.

## The Dataset
Thanks to [Chris Diehl](http://www.cpdiehl.org/), we have access to a
large and simple graphml version of the Enron Email dataset, which is
comprised of containing approximately 250,000 unique email messages 
mainly occurring in the 2000-2002 time frame.

See the [Data Model](https://github.com/diehl/Enron-GraphML-Data-Documentation/blob/master/Enron_GraphML_ER_Diagram.jpg)
and 
[Attribute diagram](https://github.com/diehl/Enron-GraphML-Data-Documentation/blob/master/Enron_GraphML_Attributes.jpg)
for details.

Also, read more about the dataset in [Relationship Identification for Social Network Discovery][cpdiehl-paper]

What we plan to do with this dataset is combine it with some [Natural
Language
Processing](http://en.wikipedia.org/wiki/Natural_language_processing)
and will add metadata to the graph to support answering questions like:

* Who is the angriest communicator
* Which groups of people are deceiptive in their communications
* ??

## What is covered
We cover using pacer to:

1. Load GraphML into TinkerGraph and Neo4J
2. Perform graph traversals, filtering on properties and edge-labels
   using "Routes"
3. Use "Look-Aheads" to branch off the graph
4. Showing the "Paths" we took to traverse somewhere
5. Basic graph analysis using "group_count" 
6. Creating sub-graphs
7. Moving data from one graphDB to another

[cpdiehl-paper] 
### Relationship Identification for Social Network Discovery
Chris' paper [Relationship Identiﬁcation for Social Network Discovery](http://www.cpdiehl.org/PDF/aaai07-final.pdf)
offers an approach to calculate nontrivial ego networks from
correspondance, and couples this with the reporting relationships
outlined in an org chart.

From his Results section:
> Using an internal Enron document specifying the direct reports for 
> Enron employees over 2000-2001, we identiﬁed 43 individuals in the 
> collection with observable managersubordinate relationships and 
> nontrivial ego networks. We constructed the ego networks 
> corresponding to each employee over this time frame and retained 
> only those relationships where a minimum of 5 emails were sent in each
> direction. The resulting ego networks range in size from 2 to 107 
> relationships.

