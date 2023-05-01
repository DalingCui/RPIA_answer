# RPIA_answer
Use your best judgement to determine what are the tenor buckets that should be considered in this case.
1. the tensor buckets are determined as: less than 3 years as short-term, 3-7 years as intermediate term, and longer than 7 years as long-term

Design a mechnism to reallocate the IR exposure into these tenors.
1. we use duration matching method to rellocate the IR exposure in each tenor. I use the duration difference between portfolio and index in each tenor as penalty in the optimizer function. In a same tenor, this method guarantee that the portfolio duration is in line with index duration.

the client is concerned about underperformance vs the index, but not outperformance.
1. we ganrantee this by setting the contraint condition tracking error >=0, where tracking error = return of portfolio - return of index.

Any other ideas you can think of to improve the optimizer? It can be only theoretical.
1. we may also need to consider the transaction fees and bond liquidity
2. we can use machine learning techniques,such as neural network, random forest tree to enhance the optmizer capability to identify optimal portfolios or select bonds.

Describe on a high level how you would improve the code structure and workflow if you have more time, for example, data pipeline, testing, etc.
1. I would like to encapsulate the determination of tenor buckets and the calculation based on tenor buckets ,such as df_tenor_bucket, into a function. Similar encapsulation process can also be applied to calculate the metrics of portfolio after optimization for each day and following test.
2. I would like also to create data pipline to clean and preprocess the extracted data to ensure that it is ready for the following calculations.


