# Wake_Word_Detection_with_Alignment_Free_Lattice_Free_MMI
## Questions
- How to design filler-model ?
- How to understand numerator-graphs ?
## Abstract
- we remove the prerequisite of frame-level alignments in the LF-MMI training algorithm permitting the use of un-transcribed training examples that are annotated only for the presence/absence of the wake word
- we show that the classical keyword/filler model must be supplemented with an explicit non-speech (silence) model for good performance
- we present an FST-based decoder to perform online detection
## Key Concepts
- Alignment-Free Lattice-Free
- HMM-based keyword-filler models
- Pure neural models
- phone-HMM vs. word-HMM
- TDNN-F with skip connections
- hybrid DNN/HMM
- sequence-level training criteria
## HMM Topology
- wake word HMM
- freetext HMM
- silence HMM
## Alignment-Free Lattice-Free MMI
- In the regular LF-MMI the **numerator graph(分子图)** used to compute the truth sequence is an **acyclic graph(非循环图)** generated from an existing GMM model
- For ASR, the competing hypotheses in the **denominator graph(分母图)** are constructed from a phone LM trained from the training transcripts
## Acoustic Model
- TDNN-F with skip connections
- ???
## Data Preprocessing and Augmentation
- To tackle this problem, before training we segment all negative recordings into several chunks so that the chunk lengths are draw from the empirical distribution of the positive recordings.
## Decoding
- The **immortal token** is the common ancestor of all active tokens