# Automatic-IRM-LGC-with-deep-features

![Sample](./image.png "Sample")

Accurate object segmentation is a fundamental challenge in computer vision, conventionally addressed by either pure deep
learning models or classical optimization algorithms. The Iterated Region Merging with Localized Graph Cuts (IRM-LGC) algorithm is a
powerful classical method; however, it suffers from two major drawbacks: heavy reliance on manual user interactions for initialization,
and susceptibility to failure in complex textural backgrounds due to its reliance on basic color metrics. In this paper, we propose a fully
automated, hybrid neuro-symbolic pipeline. We integrate a pre-trained DeepLabV3 network to automatically generate high-confidence
foreground and background seeds, eliminating the need for human intervention. Furthermore, we replace standard superpixels with a
grid-based compact watershed algorithm to ensure strict adherence to object boundaries while maintaining geometric consistency.
Most importantly, we introduce a novel energy formulation in the graph cut by fusing Euclidean color distance with deep textural
features extracted from the intermediate layers of a VGG16 network. Experimental results on the Oxford-IIIT Pet dataset demonstrate
that our automated pipeline successfully captures fine boundaries (such as animal fur) and boosts the Intersection over Union (IoU)
significantly in complex scenes, showcasing the robustness of combining neural semantic priors with symbolic graph optimization.
