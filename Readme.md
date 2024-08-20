# An Evluation Benchmark for Truncation Sampling Decoding Strategies of LLMs

# Data preparation
### Step 1: Gather the context-preserving prefix tree of any existing dataset
```
python collect_prefix_tree.py
```
Main features:
  - Efficient implementation via multi-processing. For example, given 2 sockets (24 cores per socket) of AMD EPYC 7402 processor, the script can process roughly 120k articles in 1 hour to build a context-preserving tree with sentence-level context. Then the total 6458670 articles of English Wikipedia dataset will be transformed into a context-preserving tree in around 2 days.
