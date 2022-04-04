---
layout: post
title:  "Paper Summary: On a Measure of Intelligence (F.Chollet)"
date:   2021-12-28 15:08:54 +0000

---
A summary of the paper "On a Measure of Intelligence" by Francois Chollet.

<https://arxiv.org/pdf/1911.01547.pdf>

## Overview

Chollet begins by surveying and critically evaluating current methods of measuring intelligence. He notes that the AI community as a whole often measures systems based on *skill* rather than on *skill acquisition efficiency*, and fails to control for system priors and experience. Using algorithmic information theory, he provides mathematical formulations for control factors such as task difficulty and prior experience, then uses these to define an objective measure of intelligence. The paper concludes with the proposal of the ARC benchmark, for measuring system intelligence under the paper's novel definition.

Chollet writes his paper in three parts: 
- Part 1: Context and History
- Part 2: Taking a new perspective
- Part 3: A new benchmark for AI evaluation - the ARC dataset

We will begin by surveying the history of intelligence measures, and the need for a new, more rigorous approach.
<br><br>

#### **Part I: Context and History**

**Motivation** - Chollet cites two key reasons for the importance of objective measures of intelligence. The first is simply to benchmark progress and evaluate promising paths to developing more intelligent systems. 
The second makes clear the *risks* in not possessing such a metric. Chollet states that, at present, the field of AI is being shaped by *implicit definitions* and *biases*, which do not accurately represent intelligent behaviour. A key theme that is explored in this paper is the current trend in measuring intelligence based on a system's *skill*, rather than it's *efficiency in acquiring skill*. This, Chollet believes, will lead to systems with superhuman capability in relatively narrow domains, as supposed to human-level general intelligence - the "holy grail" of artificial intelligence.

<span style="color:gray">
From an alignment/safety perspective, there is another reason to strive for more objective measures of system intelligence. At present, we are pleasantly suprised when AI systems suprise us with their capability [1]. However, as machines become more capable, I think this is something to be increasingly wary of. A concrete measure of intelligence, applicable to any system, may allow us to understand the **bounds** of a system's capability which will be invaluable for AI alignment and policy efforts.
</span>

**Nature of Human Intelligence** - 
How do we currently view the nature of general intelligence? Based on Legg and Hutter's survey of definitions in 2007 [2], as well as the widely accepted Cattell-Horn-Caroll (CHC) theory on human cognitive ability, Chollet argues that there are two common schools of thought:

1.) Intelligence as a collection of task-specific skills - This views the human brain as implementing a number of routines that in ensemble produce intelligent behaviour. In building an artificial intelligence, one may look to provide it with a natural language program, a logical reasoning program, a math program and more. The goal, as Chollet puts it, was to *encode human skills into formal rules and knowledge into databases*. This paradigm flourished in the early days of AI research (1950s - 1980s), but lost popularity following the failure of such "hard coded" systems to handle combinatorial explosions as operating environments became more complex.

2.) The second outlook on the nature of general/human general intelligence is as a *general learning ability*; viewing minds as being initialised with no skills and deriving them all from the surrounding environment. This is the framework that shapes AI research at present, but Chollet says that even this approach of viewing human intelligence as a "*randomly* initialised neural network" is not accurate. The issues with the current approach will be explored in Part II.



**Current measures of intelligence** 

In this section we see Chollet begin to hone in on the idea that present-day research in AI is evaluating the *wrong* thing - skill rather than skill acquisition efficiency. Let us start by distinguishing two different types of generalisation metrics. 

**System-Centric (SC) generalisation** - When evaluating the performance of a learning system after training it on some distribution, we look to see how well it generalises to an unseen test distribution. The ability for a system to generalise to unseen data is it's system-centric generalisation power. An example is the test accuracy of a machine learning classification algorithm. 

**Developer-Aware (DA) generalisation** - In many cases however, SC generalisation metrics do not prove to be a true reflection of the generalisation power of the system itself. Let's illustrate this with an example. Consider two image classification algorithms, A and B, training on a dataset T<sub>0</sub>, which features images with unusually high levels of fine detail. Say algorithm A incorporates a hard-coded routine that is developed to efficiently extract information present in regions of fine detail (by means of Fourier methods etc). Thus, from a purely system-centric point of view and all else equal, it will appear as if A generalises better, when in fact we have no indication if it is a *better learner*, just that it is particularly adapted to this test dataset (has a prior). Developer-aware generalisation metrics aim to account for any prior ability/knowledge of a system with respect to a test dataset.

DA generalisation is another *key theme* in this paper. Chollet makes the case that many current AI evaluation metrics measure SC generalisation and ignore system priors. 

In the following pages, the trend to evaluate AI based on board/video games is discussed, as well as the current measures of human intelligence via psychometric tests. The psychometric approach offers several methods to control for system priors, and therefore measure DA rather than SC generalisation. In particular, psychometric tests: 

- Aim to measure *abilities* rather than narrow skills. Tests measure verbal reasoning ability through a range of different tests (writing, comprehension, encoding and decoding challenges), which make it harder to develop priors for. 

- Psychometric tests evaluate human intelligence through test batteries that are often *unseen* by test participants. The abstract pattern exercises seen in IQ tests are rarely encountered in everyday life. 
  

#### **Part II: Context and History**












<br><br><br><br><br>
#### References

[1] - https://www.scientificamerican.com/article/ai-designs-quantum-physics-experiments-beyond-what-any-human-has-conceived/

[2] - https://arxiv.org/pdf/0706.3639.pdf 
