# RPIA_answer
Use your best judgement to determine what are the tenor buckets that should be considered in this case.
1. the tensor buckets can be determined: less than 3 years as short-term, 3-7 years as intermediate term, and larger than 7 years as long-term

Design a mechnism to reallocate the IR exposure into these tenors.
1. we can use duration matching method to rellocate the IR exposure in each tenor, so that the duration in each tenor is in line with the index

the client is concerned about underperformance vs the index, but not outperformance.
1. we ganrantee this by setting the contraint condition that tracking error >=0, where tracking error = return of portfolio - return of index.

Any other ideas you can think of to improve the optimizer? It can be only theoretical.
1. we may also need to consider the transaction fees and bond liquidity
2. we can use machine learning techniques,such as neural network, random forest tree to enhance the optmizer capability
