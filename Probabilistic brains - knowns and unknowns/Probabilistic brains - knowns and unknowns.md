# Probabilistic brains: knowns and unknowns
* **Authors:** Alexandre Pouget, Jeffrey M. Beck, Wei Ji Ma, Peter E. Latham.
* **Journal:** Nature Reviews Neuroscience
* **Date:** September 2013

## Big Idea
* This review article discusses whether the brain represents probability distributions and thus performs probabilistic inference. The paper discusses why probabilistic inference is desirable and briefly describes how it can be implemented in neural circuitry. Lastly, it discusses future challenges for extending these theories to synaptic weights, structural learning, and real-world problems. 

## Introduction
* Uncertainty is important in neural computation, and estimates of variability are prevalent in the sensory, motor, and cognitive domains.
* One way to handle uncertainty is to represent knowledge with probability distributions; i.e. a Bayesian approach. Do neural systems do this?
* There's evidence that humans use probabilistic inference in the sensory, motor, and cognitive domains. 
* Big idea: **Okay, so we use some probabilistic inference in neural processing. But how important is it, and how is it implemented in neural circuitry?**

## Probabilistic inference for multisensory integration
* We can use probabilistic inference to combine information about a stimulus across modalities. Probability comes into play by weighing each modality by some uncertainty rather than just giving each modality the same weight.
* Ernst and Banks visuo-haptic experiment with a bar had humans using multisensory integration on a bar. They found that human behavior (in this context) is consistent with Bayes' rule and thus probabilistic inference. 

## A unified framework
* We need a generative model for probabilistic inference; thus we need some likelihood $p(I|s)$ and prior $p(s)$ where $I$ is the data and $s$ is the latent variable. 
* Probabilistic inference is then summarized by Bayes' rule. The upside to this is that it can be written generally, independent of modality. A lot has been abstracted out and the hope is that this leads to general theories of neural computation. 

## Encoding probabilities with neurons
* Classical assumption is that neurons don't encode probabilities; instead they encode some value. 
* More likely that neurons encode functions of latent variables.
* Possibilities proposed: neurons encode probabilities, log-probabilities of whether a feature is present OR the value a feature takes on. The distinction is important as it has consequences for inference: through linear combinations, adding probabilities is easy while multiplying log-probabilities is easy. 
* Other proposal: neural responses represent coefficients of a basis expansion for log-probability. This is supported by the fact that $p(\mathbf{r}|s)$ is generally found to follow the exponential family with linear sufficient statistics. 
* Last proposal: sampling hypothesis. The neural responses represent samples from the posterior distribution $p(s|\mathbf{r})$. 

## Neural implementation of probabilistic inference
* Pretty simple ideas here: mainly linear combinations of neural responses across neurons as well as across time. For the second one, a neuron needs to linearly integrate its responses over time which has been observed in intraparietal cortex (for accumulating information about direction of motion).
* Make a reference to divisive normalization as used in marginalization.
* Estimation: either performing MAP or ML estimation. 

## Future challenge: learning a posterior distribution over weights
* Rather than learning exact weights (for example, synaptic weights), neurons learn prior distributions over weights. Then, they can take averages that are more robust than just a point estimate of the weights. 

## Future challenge: structural learning
* We need to learn the structure of a task given data, e.g. what variables matter for computing some quantity or performing a task?
* Can be akin to determining the graphical model for the problem, then the problem reduces to model selection. How do populations of neurons do model selection for new tasks? Probabilistic inference could be helpful.
* Also connections to building representations on short timescales, such as for speech.

## Future challenge: dealing with intractable real-world problems
* How do we move beyond modeling simple problems such as direction selectivity where behavior is near optimal (i.e. uncertainty is low)? Perhaps probabilistic inference will be less useful in complicated, real-world problems.
* Since real world problems are more difficult, does the brain use heuristics rather than probabilistic inference? The authors hint that instead, the brain might use approximations to probabilistic inference which decrease optimality. 

## Discussion
* Pouget at al. argue: because neural circuitry has similarities across the brain, it is possible that these areas share similar computational principles. Probabilistic inference can be applied to make general principles about the brain. 
* In some fashion, neurons definitely represent probability distributions. But are knowledge of these distributions useful for neural computation?