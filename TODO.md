# TODO

- do not hardcode cuda version in cudarc feature
- do not harcode the number of cuda threads / blocks
- avoid repeated access to global memory in cuda sumcheck when there are enough registers (in the extension field, this is already done for the prime field)
- cuda sumcheck: first round, if n_batching_scalars = 0 => sums are actually in F, not EF
- Avoid variable reversing for whir sumchecks
- improve serialization / deserialization of field elements, improve fiat shamir
- https://eprint.iacr.org/2024/108.pdf section 3
- We can probably send less data in the first AIR sumcheck, with univariate skip, and the "current row" / "next row" reductions
- matrix_up_folded / matrix_down_folded in cuda
- AIR inner sumcheck can bee accelerated (some factors have not all the variables + it's sparse -> avoid "dummy variables")
- Neg in ArithmeticCircuitComposed
- use cuda constant memory (can speed up a big number of kernels)
- sparse preprocessed columns
- MaybeUninit instead of allocating zeros when it's rewritten just after
- refactor the disgusting multilinear_evaluations.cu
- avoid launching 64 kernels in test_cuda_eval_mixed_tensor (and avoid using the auxialry eq_mle kernel)

- Add ZK?
