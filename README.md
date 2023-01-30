# BiBC_degree_calculator
Calculates BiBC and degree of nodes from a pickled networkx file

Bipartite Betweenness Centrality (BiBC) is a node property that is an extension of betweenness centrality. In BiBC, the betweenness centrality is calculated between
two distinct groups of nodes, and each node is scored based on the number of times it appears on the shortest path between each pair of nodes in both node groups. Thus,
it is a measure of the 'bottleneck-ness' of a node. A node with a high BiBC indicates the node could play a key mediatory role between the interaction of the two groups.

Required (positional) arguments:
- pickle: The pickle file created with import_network_data.py

Optional arguments:
- --bibc_groups: What to compute BiBC on, either distinct groups or on the two most modular regions of the network
- --bibc_calc_type: Would you like to normalize based on amount of nodes in each group (rbc) or not (bibc)?
- --node_map: Required if node_types is specified for --bibc_groups. CSV of nodes and their types (i.e. otu, pheno, gene, etc.)
- --node_groups: Required if node_types is specified for --bibc_groups. Its the two groups of nodes to calculate BiBC/RBC on
- --log", action = 'store_true', help = 'Optional log file for progress of BiBC calculation
