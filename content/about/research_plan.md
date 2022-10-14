---
title: "Research Plan"
date: 2022-10-13T09:04:30-04:00
draft: false
---

|                  |                                     |
| :--------------: | :---------------------------------: |
|       Name       |            Samuel Jones             |
|      School      |        Satellite High School        |
|     Category     | Mathematics & Computational Science |
| Research Teacher |            Mrs. Molledo             |

| ISEF Form |    Link     |
| :-------: | :---------: |
|     1     | Placeholder |
|    1A     | Placeholder |
|    1B     | Placeholder |

# NeuralNetwork Implementing Mutating Topology
__Question or Problem Being Addressed__: Reducing inefficiency during training of NEAT (NeuroEvolution of Augmenting Topologies) models and reducing complexity of NEAT models after training for better performance without sacrificing accuracy.  
 __Engineering Goals__: Create a machine learning model that implements some traits of neural networks, such as optimization procedures, while also utilizing the mutable topology found in NEAT.  
__Rationale__: While NEAT has heavy influence on machine learning, inefficiencies are posed by its optimization methodology. As an alternative, by implementing traits found in neural networks, the algorithm could potentially be optimized during the training period. In addition, by introducing post-training efficiency optimization, the overall efficiency of the model can be improved.  
 __Materials__:
   1. OMEN by HP Laptop 16-c0xxx  

__Procedures__:
1. Create an implementation of the NEAT algorithm
2. Create augmented versions of the algorithm that utilize traits found in more traditional neural networks. As an example, this could mean augmenting mutations found in NEAT to use neural network loss/optimization.
3. Train multiple iterations of each algorithm to fit the following cases to create a benchmark:
   1. XOR
   2. Pole Balancing
   3. Double Pole Balancing With Velocities
   4. Double Pole Balancing Without Velocities
4. Compare performance and efficiency of new algorithms to NEAT implementation
   1. Compare training time of each algorithm to NEAT
   2. Compare runtime of each algorithm to NEAT
   3. Compare ratio of training time to runtime of each algorithm to NEAT

[__Reprint File__](/about/reprint)