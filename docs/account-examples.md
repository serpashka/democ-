# Account calculation examples

Each row starts with a new account. Apply the deposit first, then call
`Withdraw` with the requested amount. The return value is `true` when the
withdrawal is accepted and `false` when the balance is insufficient.

For an accepted withdrawal, the ending balance is the opening balance plus the
deposit minus the withdrawal. A rejected withdrawal leaves the balance after
the deposit unchanged. These expectations follow the `Account` methods in
[`bank`](../bank); they do not represent executed tests of the console program.

All amounts are nonnegative decimal values. Rows 1-33 cover accepted partial or
zero withdrawals, rows 34-66 cover insufficient funds, and rows 67-99 cover
withdrawals of the full available balance. The numbers in the first column are
example identifiers.

| Example | Opening balance | Deposit | Withdrawal | Accepted | Ending balance |
| --- | --- | --- | --- | --- | --- |
| 1 | 0.00 | 0.00 | 0.00 | true | 0.00 |
| 2 | 20.00 | 0.00 | 6.02 | true | 13.98 |
| 3 | 30.00 | 0.03 | 9.03 | true | 21.00 |
| 4 | 40.00 | 0.04 | 12.04 | true | 28.00 |
| 5 | 50.00 | 0.05 | 15.05 | true | 35.00 |
| 6 | 60.00 | 0.06 | 18.06 | true | 42.00 |
| 7 | 70.00 | 0.07 | 21.07 | true | 49.00 |
| 8 | 80.00 | 0.08 | 24.08 | true | 56.00 |
| 9 | 90.00 | 0.09 | 27.09 | true | 63.00 |
| 10 | 100.00 | 0.10 | 30.00 | true | 70.10 |
| 11 | 110.00 | 0.11 | 33.01 | true | 77.10 |
| 12 | 120.00 | 0.12 | 36.02 | true | 84.10 |
| 13 | 130.00 | 0.13 | 39.03 | true | 91.10 |
| 14 | 140.00 | 0.14 | 42.04 | true | 98.10 |
| 15 | 150.00 | 0.15 | 45.05 | true | 105.10 |
| 16 | 160.00 | 0.16 | 48.06 | true | 112.10 |
| 17 | 170.00 | 0.17 | 51.07 | true | 119.10 |
| 18 | 180.00 | 0.18 | 54.08 | true | 126.10 |
