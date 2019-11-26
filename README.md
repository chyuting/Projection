# Projection
-----------------------
Yuting: 05/24/2019
chyuting@umich.edu
-----------------------

Python3 code Projection on subspace.ipynb.

This code can illustrate how a test case deviate from a normal one, and aims to predict abnormity before failure happens.
It is a different method compared with regression methods for it only process with the problematic sensors.
The idea comes from EECS551 @ umich. Based on Yuting's hypothethis that only problematic sensors result in failure of a truck.

Flow of the code:
1.Construct a subspace and projection matrix of training data with 40 problematic sensors, by singular value decomposition and compact reconstruction singular vectors.
2.By projecting a vector onto a subspace, we can calculate the Euclidean distance between a vector(one sample) and the subspace in high dimension.
3.Display mean/variance statistics for each case(contains about 10 days). Save figure in res_projection directory.(displayed distance is summation of all samples' distance in one day)
4.The larger the distance, the larger is the deviation from normal cases. If we detect high deviation, we can predict failure will happen in recent future.

-----------------------
Yuting: 06/03/2019
chyuting@umich.edu
-----------------------

Python3 code Projection on subspace_sparse svd.ipynb.

This code can illustrate how a test case deviate from a normal one, and aims to predict abnormity before failure happens.
It is a different method compared with regression methods for it only process with the problematic sensors.
The idea comes from EECS551 @ umich. Based on Yuting's hypothethis that only problematic sensors result in failure of a truck.

Flow of the code:
1.Construct a subspace and projection matrix of training data with 40 problematic sensors, by singular value decomposition and compact reconstruction singular vectors.
2.By projecting a vector onto a subspace, we can calculate the Euclidean distance between a vector(one sample) and the subspace in high dimension.
3.Display mean/variance statistics for each case(contains about 10 days). Save figure in res_normal_projection and res_test_projection.
4.Display distance of each sample every day. Save figure in res_normal_projection_day and res_test_projection_day.
5.The larger the distance, the larger is the deviation from normal cases. If we detect high deviation, we can predict failure will happen in recent future.

Analysis of result:
In normal result, no deviation.
In res_test_projection_day, obvious deviation at 616_31.png, 714_19.png, 714_26.png, 722_21.png.

Detect 3 failure cases among 10 failure cases. 
