# Nested GNNs for gene ontology prediction

## Sources

### DeepRank GNN
Framework that converts protein–protein interfaces from PDB 3D coordinates files into graphs
https://academic.oup.com/bioinformatics/article/39/1/btac759/6845451

### Structure-based protein function prediction using graph convolutional networks (DeepFRI)
Use GNN on graph based on proximity of amino acids in 3D space to generate embedding of protein for protein function prediction
https://www.nature.com/articles/s41467-021-23303-9

### Hierarchical graph transformer with contrastive learning for protein function prediction (HEAL)
Similar approach to DeepFRI to produce GNN based on amino acid proximity (contact map). They also use a residue embedding model (ESM-1b) to produce a node feature matrix for each amino acid residue. Then, after a few message passing layers, they add a hierarchical graph transformer which is a fancy way to say that they added super nodes that explore long-distance correlations followed by an attention pooling layer that extracts the relevant information from the super nodes. Finally, they pass the transformed graph representation into an MLP with sigmoid output function to predict go terms.
https://academic.oup.com/bioinformatics/article/39/7/btad410/7208864

### Integrating unsupervised language model with triplet neural networks for protein gene ontology prediction (ATGO)
I don't know how this works, but it's probably worth a read given that it is a recent publication with self-reported SOTA performance.

### Transformer-based protein function annotation with joint sequence-label embedding (TALE)
This model won the previous cafa competition.
