---
title: "How NEAT Basically Works"
date: 2022-10-13T09:46:05-04:00
draft: false
author: "Samuel Jones"
showFullContent: false
readingTime: false
hideComments: false
katex: false
---
# What is NEAT
NEAT, originally developed by Kenneth Stanley and Risto Miikkulainen, stands for NeuroEvolution of Augmenting Topologies. Essentially, this is a genetic evolution model that implements an evolving topology. This means that the amount of nodes and the way they are connected evolves over time. To do this, a population of neural networks is generated. After a fitness function is used to determine the viability of each individual, high-viability individuals are used to generate a new population, which are then mutated. This process is then repeated until an end-condition, such as a target fitness or a number of generations. In addition to this, populations are speciated. This means that individuals within in a generation are grouped into species to potentially protect useful mutations.

# How a Model is Encoded
A genotype is an organism's set of genes and a phenotype is the manifestation of an organism's genotype. In this case, the model's genotype is comprised of 2 sets of genes: node genes and connection genes. Node genes contain information about a node, being a node's ID and type. Connection genes contain information about a connection, being the input node, output node, weight, if it's enabled or not, innovation number. While most are self-explanatory, an innovation number is ID associated with an input and output node pair.

# Population Selection
When generating a generation, only certain portions of the population are utilized to create new individuals. This is done by running phenotypes through fitness functions, functions designed to evaluate a model. Then, the top models are used for genotype crossover and mutation.

# Genotype Crossover
To perform genotype crossover, the innovation number are utilized. By aligning each genotype by innovation number, competing connections can be avoided. Then, genes not found in the other genotype are categorized into disjoint and excess genes. All genes are then randomly inherited between the two parents.

# Mutating Models
NEAT has two categories of mutations: connection mutation and topology mutation. When mutating a connection, the connection can be toggled or the weight mutated. When mutating topology, a new connection can be made or a new node added. If a new connection is made between an input and output node, a random weight is assigned. If a new node is added between two other nodes, the previous connection is disabled, and 2 new connections are created - one with a weight of 1 and the other with a weight equal to the disabled connection.

# Speciation
Population is divided into species, a process called speciation. By doing this, traits being lost during population generation is inhibited. This is done by giving a species a shared fitness, increasing selection probability.

[__Reprint File__](/about/reprint)