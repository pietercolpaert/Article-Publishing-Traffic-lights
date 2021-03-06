##  Background
{:#sota}

### Preservation

Digital content can be preserved on tape or on disk storage. In general, tape is used by TV broadcasters or audiovisual archives, because of its [low pricing](https://searchdatabackup.techtarget.com/news/1507559/Choosing-a-data-archiving-strategy-Disk-archiving-vs-tape-archiving) for big volumes (>50 terabytes), especially on the long-term. A tape drive is cost-effective when writing or reading large files, because the position of the tape drive reader does not need to be moved frequently contrary to small files. This deficit is solved by either bundling small files together (e.g. zip, tar) or saving them on disk storage. The latter benefits over tape with faster search and retrievable times and the ability to preserve small files more efficiently.

To archive a document, this is traditionally done by generating a hash (e.g. [MD5](https://en.wikipedia.org/wiki/MD5)) from the document, copying the document together with a metadata file containing the hash (cfr. [sidecar](https://en.wikipedia.org/wiki/Sidecar_file)) to the archive system and verify the content by regenerating the hash on the archive.

### RDF isomorphism

The Resource Description Framework ([RDF](https://en.wikipedia.org/wiki/Resource_Description_Framework)) is a graph-based model to describe statements. Every RDF statement corresponds with a triple (subject-predicate-object): the _subject_ is a resource that something is said about. The subject is related to an _object_ through a _predicate_. For example, 'the traffic light is lighted green': 'the traffic light' is the subject, 'green' is the object and 'is lighted' is the predicate that expresses the relation. A RDF statement is actually a small graph. Two graphs are isomorph when a bijection is possible as described in the algorithm by [Carrol J.](cite:cites carroll2002matching). This algorithm generates a hash for every blank node to allow equivalence checking and attempts to create a bijection between the graphs. If a bijection is created, the graphs are isomorph.

### Linked Data Fragments

[Linked Data Fragments](cite:cites tpf) is a framework that allows to describe the fragmentation of a Linked Data dataset. Fragments are defined with three parts:

* a **selector** defines which parts of the dataset belong to a fragment. For example: only sensor observations that are generated between a certain time interval.
* **metadata** about the fragment. For example: the license that is applied.
* **controls** help clients to retrieve more relevant data. For example: where a previous page of a paged collection can be found.

[Comunica](cite:cites comunica) is a framework to query over the various Web interfaces in the Linked Data Fragments axis.
It interprets the metadata and controls to evaluate a query.
[Finding a fragmentation strategy](cite:cites opendataflanders) for web archives and time series data than can be consumed [by generic clients](cite:cites realtimequery) is still a challenge.
In this paper we try to suggest a solution in which generic clients can still query over the data.

