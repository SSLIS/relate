# Instructions

## Step 1. Describing your Individual Document in RDF Statements

Have a look at the vinyl record your institution is asked to describe, and try to decide which aspects might be of interest to your visitors.
Once you have a better idea of what you are dealing with, you can start describing the document in RDF.
Open your preferred text editor (see []'Before we start'](https://www.ldf.fi/service/rdf-grapher)), and start writing relevant RDF statements.
You can find an example of how to describe an album and its artists [in the Appendix](appendix/turtle-example.md).

Start by describing the most obvious relations, such as: Which album is it?
Who is it by?
Who are the band members?
Which tracks are on there?
Which record label produced it?
These are also the relations you will find an example for in the Appendix.

Specifically, we ask you to pay special attention whether the following identifiers are relevant to your record:

* 'The Crystal Ship' (song): `https://www.wikidata.org/wiki/Q1931442`
* Jim Morrison (musician): `https://www.wikidata.org/wiki/Q44301`
* Olle Schedin (musician): `https://www.wikidata.org/wiki/Q6096644`
* Martin Rössel (musician): `https://www.wikidata.org/wiki/Q6087173`
* Mare Kandre (writer): `https://www.wikidata.org/wiki/Q3743817`
* Global Infantilists (band): `https://www.wikidata.org/wiki/Q10505546`
* MNW (record label): `https://www.wikidata.org/wiki/Q4574886`

If they are, you **must** describe them.
This will become important at a later stage in this workshop.
So start with these.

We suggest you use [WikiData Links](https://www.wikidata.org/)to reference known entities (albums, record labels, artists), and the following ontologies to describe the relations between those entities:

* [MO](http://musicontology.com/specification/) (Music Ontology) to describe relations specific to music production
* [FOAF](http://xmlns.com/foaf/0.1/) (Friend of a Friend) to describe personal relations
* [DCMI](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/) (Dublin Core Metadata Initiative) to describe digital collections

We would also ask you to make your RDF statements as readable as possible, by using a @prefix to shorten your URIs into CURIEs (Compact URIs), as explained in the video lecture.
If you need to refresh your memory, [this link will take you to the exact spot in the lecture that talks about using @prefix in Turtle](https://play.hb.se/media/Linked+%28Open%29+Data+for+Digital+Libraries/0_ol5tnwn3?st=2960).

If any questions come up during this task, raise your hand, and your tutors will come to your aid.
If you're ready describing the most obvious relations and there's still time, have a look at the Music Ontology, and see what else you might convert to RDF statements.
Maybe you can find the lyrics or a video of one or more of the tracks on the album to link to?

# Step 2. Visualize your relations as graph (and troubleshoot)

When everyone is done with Step 1, we'll try to visualize our RDF statements as a graph.
To make this visualization, we will be using [RDF Grapher](https://www.ldf.fi/service/rdf-grapher), a web service for parsing RDF data and visualizing it as a graph, developed by the [Linked Data Finland](https://www.ldf.fi/index.html)project.

Visualizing your RDF is a great way to troubleshoot your code.
Firstly, because parsers such as RDF Graphers require your RDF statements to be well-formed.
So if you've made any 'syntactical' mistakes in your code (e.g.: forgotten a full stop at the end of an RDF statement), the parser will refuse to visualize your data, and instead point you in the right direction to fix your mistake.
Secondly, a visualized graph of your coded relations also makes them much easier to read.
So you can use the visualization to check whether you used the right identifiers.

To visualize your descriptions follow these steps:

1. Visit [https://www.ldf.fi/service/rdf-grapher](https://www.ldf.fi/service/rdf-grapher)
2. Under the heading Try the service, you will find a text input field, with some sample text in it. Replace that sample text with your own (copy pasting in your RDF statements).
3. Double-check that the From format option is set to Turtle in the drop-down menu.
4. For the best looking results, select SVG in the drop-down menu for the To format option.
5. Click on the Visualize button.

If there are any errors in your RDF, RDF Grapher will tell you where to find them, and what the problem might be.
Fix the error, have a quick look at your document to see if you find any similar mistakes, and try again.

If there are no errors, RDF Grapher will output a graph to visualize your statements, where the subjects and objects are visualized as 'nodes' (ellipses for URIs, and rectangles for literals), and the predicates are visualized as 'edges' (the lines between the nodes).
Have a good look at your visualization.
Did it visualize your data in a way you expected?
If you notice anything off, have another look at your data, and see if you need to fix any mistakes.

# Step 3. Merge the RDF statements of all the institutions

Now that we all have working, well-formed RDF statements, it's time to join them together!
To do so, follow these steps:

1. Visit [this workshop's github repository](https://github.com/SSLIS/relate).
2. Navigate down to [the `data` folder inside the repository](https://github.com/SSLIS/relate/tree/main/data).
3. Near the top-right of the page, you will find an `Add files` button. Click on it, and choose the `Upload files` option.
4. Find your `.ttl` file, and opload it, following the instructions on the screen.

Your tutor will then review and accept your upload.

**Note** that Step 4 will only work if Step 2 is completed correctly, so make sure to test your `.ttl` file before uploading!


# Step 4. Visualize the relations between documents (and institutions) as a graph

Once everyone has uploaded their materials, and they have been accepted by the tutor, they will be used to automatically generate a composite graph with RDF-Grapher. 
Follow along as your tutor shows you this (and troubleshoots any rising issues).

Done!