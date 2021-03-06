Graph measures
===================

Using SparklingGraph you can utilize multiple well-known measures for graphs. 


Graph measures API
------------------


Graph measures
+++++++++++++++++

Each graph mesure extends `GraphMeasure <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.measures.GraphMeasure>`_ trait, defining what kind of value will be returned for whole graph.


Vertex measures
+++++++++++++++++

Each vertex mesure extends `VertexMeasure <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.measures.VertexMeasure>`_ trait, defining what kind of value will be returned for each vertex. For main part of measures that will be a single number (like Double) but for some of them a tupple (or other data type) can be returned (like (Double,Double)). Each measure defines also implicit methods for graph, thanks to what your code will be more readable, and you will develop your experiments faster.

Measures accepts `VertexMeasureConfiguration <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.measures.VertexMeasureConfiguration>`_ in order to configure computation process. You can set following parameters:

* `BucketSizeProvider <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.IterativeComputation$>`_ - used in more complex computations in order to divide data into buckets
* ``treatAsUndirected:Boolean`` - graph will be treated as undirected during computations

Edges measures
+++++++++++++++++

Each edge mesure extends `EdgeMeasure <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.measures.EdgeMeasure>`_ trait, defining what kind of value will be returned for each edge, and what kind of data is expected for each vertex. Each measure defines also implicit methods for graph, thanks to what your code will be more readable, and you will develop your experiments faster.

Measures accepts parameters:

* ``treatAsUndirected:Boolean`` - graph will be treated as undirected during computations

Beside defining methods for computing measure for whole graph, method (`computeValues <http://sparkling-graph.github.io/sparkling-graph/latest/api/#ml.sparkling.graph.api.operators.measures.EdgeMeasure>`_) for single edge is also present. 



Measures
------------------

Curretnly you can use following measures:


*	Vertex measures:
	
	.. toctree::
	   :maxdepth: 2
	   
	   closeness
	   eigenvector
	   hits
	   degree
	   neighborhoodConnectivity
	   vertexEmbeddedness
	   localClustering


*	Graph measures:
	
	.. toctree::
	   :maxdepth: 2
	   
	   freeman
	   modularity

*	Edges measures:
	
	.. toctree::
	   :maxdepth: 2
	   
	   adamic
	   commonneighbours
