
# Efficient Incremental Verification of Neural Networks Guided by Counterexample Potentiality
OLIVE: **O**rder **L**eading **I**ncremental **Ve**rification 

[This aims to provide supplementary materials for the paper (OOPSLA2025) titled:"Efficient Incremental Verification of Neural Networks Guided by Counterexample Potentiality" with more details and discussion, which could be fully included in the original submission due to the page limits. ]

（Implementation is ready soon, please stay tuned!)


------


#### OLIVE is an abstract execution tool for deep neural networks verification. Olive can accelerate the verification of a new neural network $`N^*`$ by leveraging existing verification results (templates) from a similar network $`N_0`$. 



- In particular, these materials includes:
- 15 DNN-based alternations [benchmark](https://sites.google.com/view/olive-nnv/benchmarks) models and additional discussion on benchmarks;
- A running [demonstration](https://sites.google.com/view/olive-nnv/demo). 
- Detailed and additional [experimental results](https://sites.google.com/view/olive-nnv/experiments) for each research question;
- Comprehensive discussion for experimental results with nice visualization (e.g., figures, plots, tables);



-------

<img src="https://i.postimg.cc/m2kq66nM/IVAN4.png" alt="incremental" width="450"/>

**Olive** can accelerate the verification of a new neural network $`N^*`$ by leveraging existing verification results (templates) from a similar network $`N_0`$. Branch and Bound technique first verifies an original network $`N_0`$ through AppVerifier to generate templates T, then uses the templates to speed up the verification process when checking a modified network N*, achieving faster verification while maintaining correctness.

-------

#### Key features of Olive:
1. Addresses a gap in current approaches: While existing methods focus on identifying whether each sub-problem should be reassessed, Olive introduces a novel prioritization strategy based on how necessary each reassessment is.
2. Eager to Falsification-Driven exploration: The approach explores sub-problems of verifying $`N^*`$ based on $`N_0`$, which rechecks the most suspicious historical sub-problems first.
3. **Olive** reuses information across different subtrees of the template (represented previous verification subproblem space). Rather than treating each subtree independently, as in verification from scratch,  **Olive** leverages insights and refinements from templates, which reduces redundant exploration with similar subproblems. Olive achieves greater efficiency in robustness verification. 





## License and Copyright

Licensed under the [Apache License](https://www.apache.org/licenses/LICENSE-2.0)
- Our implementation is built on top of 
    - [IVAN] https://github.com/uiuc-arc/Incremental-DNN-Verification 
