# Stochastic Processes Disease Modelling
 Presented new mathematical models that extend methodology which incorporates relationships (edges) between indivduals (nodes) to create a network graph on which a disease outbreak.

This code is an implementation of an epidemiological model called the "Probabilistic House of Edges (PHE)" model. The model simulates the spread of a disease through a network of individuals, represented as nodes in a graph.

The code uses several libraries including copy, pathlib, random, dataclasses, itertools (aliased as it), numpy (aliased as np), pandas (aliased as pd), networkx (aliased as nx), matplotlib.pyplot (aliased as plt), bokeh, and ipywidgets. bokeh.io.output_notebook() is also called to output the visualization of the simulation in the notebook.

The main class defined in this code is called PHE, which stands for "Probabilistic House of Edges". The class has several attributes such as degree, steps, beta, edge_creation, nodes, and seed. There is also a __post_init__ function that is automatically called after the class is initialized, that sets a random number generator and creates the graph.

The simulate function updates the state of each node in the graph for a certain number of steps. The analyze function computes statistics on the history of the simulation, and the make_graph creates the graph with either watts_strogatz_graph or erdos_renyi_graph or barabasi_albert_graph. The draw_graph function uses the bokeh library to create an interactive visualization of the graph.

In this class also contain

'degree' : degree of a node
'beta' : probability of a node getting infected
'medication': status of medication a node is taking
'death_prob': probability of a node dying of the disease.
It also uses classes nx.watts_strogatz_graph, nx.erdos_renyi_graph, nx.barabasi_albert_graph for building the graph and also uses spring_layout for positioning the nodes of the graph.
