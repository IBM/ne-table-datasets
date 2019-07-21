Extended versions of bAbI dialog tasks
======================================================

Please refer to the paper "NE-Table: A Neural key-value table for Named Entities" and its Appendix for task and dataset details.

Candidate file:
-------------------------
A list of responses that the agent can retrieve from
extended-dialog-babi-candidates.txt

DB file:
-------------------------
extended-dialog-babi-db-table.txt


Task1
===============================
Get required information from the user. Make API-call and retrieve relevant restaurants(rows) from the DB table

Dialog data:
-------------------------
extended-dialog-babi-task1-API-calls-trn.txt
extended-dialog-babi-task1-API-calls-dev.txt
extended-dialog-babi-task1-API-calls-tst.txt
extended-dialog-babi-task1-API-calls-tst-OOV.txt

Retrieval labels:
-------------------------
ACR
This is always cuisine, location, range and number of people, which corresponds to columns 1, 2, 3 and 7

ARR
The files contain the row numbers in the DB table which should be retrieved for the corresponding dialog. For example if line number 545 in the file has content 1164, 1167, it means that restaurants at row numbers 1164 and 1167 in the DB table are the restaurants that should be retrieved for the dialog number 545. All numbers are zero indexed.
extended-dialog-babi-task1-API-calls-db-arr-trn.txt
extended-dialog-babi-task1-API-calls-db-arr-dev.txt
extended-dialog-babi-task1-API-calls-db-arr-tst.txt
extended-dialog-babi-task1-API-calls-db-arr-tst-OOV.txt

For more details refer to Appendix.


Task2
===============================
Get required information from the user. Make API-call and retrieve relevant restuarants(rows from the DB table. Refine according to user needs. Make an API-call again and retrieve relevant restaurants(rows) from the DB table.

Dialog data:
-------------------------
extended-dialog-babi-task2-API-refine-trn.txt
extended-dialog-babi-task2-API-refine-dev.txt
extended-dialog-babi-task2-API-refine-tst.txt
extended-dialog-babi-task2-API-refine-tst-OOV.txt

Retrieval labels:
-------------------------
ACR
This is always cuisine, location, range and number of people, which corresponds to columns 1, 2, 3 and 7

ARR
The files contain the row numbers in the DB table which should be retrieved for the corresponding dialog and API call. Each dialog has exactly 2 API calls. For example, if line number 545 in the file has content 1164, 1167, it means that restaurants at row numbers 1164 and 1167 in the DB table are the restaurants that should be retrieved for the dialog number 275's (544/2 + 1) first API call. Note that in task 2 unlike task 1 each dialog has exactly two API calls associated with them.  All numbers are zero indexed.
extended-dialog-babi-task2-API-refine-db-arr-trn.txt
extended-dialog-babi-task2-API-refine-db-arr-dev.txt
extended-dialog-babi-task2-API-refine-db-arr-tst.txt
extended-dialog-babi-task2-API-refine-db-arr-tst-OOV.txt

For more details refer to Appendix.


Task4
===============================
Retrieve the address and/or phone number of a restaurant requested by the user. This involves retrieving a particular cell from the DB table.

Dialog data:
-------------------------
extended-dialog-babi-task4-phone-address-trn.txt
extended-dialog-babi-task4-phone-address-dev.txt
extended-dialog-babi-task4-phone-address-tst.txt
extended-dialog-babi-task4-phone-address-tst-OOV.txt

Retrieval labels:
-------------------------
ACC
When the value in the file is a number, it represents the column index in the DB table. 5- phone number and 6- address.
When the value is "N", it means there is no retrieval required there. A dialog can either have only phone number retrieval or only address retrieval or sometimes both.
Each line in the file corresponds to one line in the dialog. If there are two dialogs of length 4 and 7, then line number 6 in the file corresponds to the second line in the second dialog (the blank line between two dialogs in the dialog data is not considered).
extended-dialog-babi-task4-phone-address-db-acc-trn.txt
extended-dialog-babi-task4-phone-address-db-acc-dev.txt
extended-dialog-babi-task4-phone-address-db-acc-tst.txt
extended-dialog-babi-task4-phone-address-db-acc-tst-OOV.txt

ACR
This is always 0. The column corresponding to the restaurant name.

ARR
Each line in the file corresponds to a line in the dialog. If the value is "N", that means, there is no retrieval corresponding to that line in the dialog. If the value has a number, then that value represents the row number in the DB table for the retrieval.
extended-dialog-babi-task4-phone-address-db-arr-trn.txt
extended-dialog-babi-task4-phone-address-db-arr-dev.txt
extended-dialog-babi-task4-phone-address-db-arr-tst.txt
extended-dialog-babi-task4-phone-address-db-arr-tst-OOV.txt

For more details refer to Appendix.
