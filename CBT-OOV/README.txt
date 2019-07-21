The Children's Book Test (CBT) - Out of Vocabulary (OOV) test sets
===============================

Test sets (Word type NE)
-------------------------
The original CBT test set ( word type NE ) does not have any OOV named entities.

To further evaluate how OOV NEs impact the baseline models and our proposed idea of handling named entities, we created additional OOV test sets as follows.
There are 422 unique NEs (answers) from 2500 samples in the test set.
We generate new test datasets by replacing these NEs with new NEs not present in the train and validation sets.

This dataset provides 5 new OOV test sets with varying percetages of OOV named entities ( 20%, 40%, 60%, 80% and 100% ).
The varying percentage of OOV named entities helps showcase how a neural architecture copes with OOV named entities as they increase.

Data is in the included "data" folder. There are 5 files:

0.2-OOV-cbtest_NE_test_2500ex.txt: 84 new NEs
0.4-OOV-cbtest_NE_test_2500ex.txt: 168 new NEs
0.6-OOV-cbtest_NE_test_2500ex.txt: 253 new NEs
0.8-OOV-cbtest_NE_test_2500ex.txt: 337 new NEs
1.0-OOV-cbtest_NE_test_2500ex.txt: 422 new NEs
