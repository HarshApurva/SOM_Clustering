# SOM_Clustering
This repository contains a Python script that applies a Self-Organizing Map (SOM) to cluster significantly differentially expressed genes from RNA-seq or other high-throughput expression data. The goal is to visually and analytically group genes based on similar expression profiles and significance levels.

The script performs the following steps:
Data Loading: Reads in a CSV file containing gene expression analysis results, including log2 fold changes and p-values.
Significant Gene Filtering: Filters genes based on an adjusted p-value threshold (default: < 0.05).
Feature Selection and Normalization: Selects relevant features (Log2 fold change, Pvalue, Adjusted p-Value) and normalizes them using MinMaxScaler.
SOM Initialization and Training: Sets up a 6x6 SOM grid using the MiniSom package and trains it using the normalized features.
Gene-to-Cluster Mapping: Assigns each gene to a cluster based on the neuron (grid position) it is closest to on the trained SOM.

Visualization:
Scatter Plot: Visualizes the clustered genes using Seaborn, colored by SOM cluster.
U-Matrix Plot: Shows the SOM distance map to reveal the density and separation of clusters.

Output:
Saves a list of top 10 genes per SOM cluster to a text file SOM_clustered_genes_1.txt.

Requirements
pandas
numpy
matplotlib
seaborn
sklearn
minisom
