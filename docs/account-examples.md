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
| 19 | 190.00 | 0.19 | 57.09 | true | 133.10 |
| 20 | 200.00 | 0.20 | 60.00 | true | 140.20 |
| 21 | 210.00 | 0.21 | 63.01 | true | 147.20 |
| 22 | 220.00 | 0.22 | 66.02 | true | 154.20 |
| 23 | 230.00 | 0.23 | 69.03 | true | 161.20 |
| 24 | 240.00 | 0.24 | 72.04 | true | 168.20 |
| 25 | 250.00 | 0.25 | 75.05 | true | 175.20 |
| 26 | 260.00 | 0.26 | 78.06 | true | 182.20 |
| 27 | 270.00 | 0.27 | 81.07 | true | 189.20 |
| 28 | 280.00 | 0.28 | 84.08 | true | 196.20 |
| 29 | 290.00 | 0.29 | 87.09 | true | 203.20 |
| 30 | 300.00 | 0.30 | 90.00 | true | 210.30 |
| 31 | 310.00 | 0.31 | 93.01 | true | 217.30 |
| 32 | 320.00 | 0.32 | 96.02 | true | 224.30 |
| 33 | 330.00 | 0.33 | 99.03 | true | 231.30 |
| 34 | 170.00 | 3.40 | 173.74 | false | 173.40 |
| 35 | 175.00 | 3.50 | 178.85 | false | 178.50 |
| 36 | 180.00 | 3.60 | 183.96 | false | 183.60 |
| 37 | 185.00 | 3.70 | 189.07 | false | 188.70 |
| 38 | 190.00 | 3.80 | 194.18 | false | 193.80 |
| 39 | 195.00 | 3.90 | 199.29 | false | 198.90 |
| 40 | 200.00 | 4.00 | 204.40 | false | 204.00 |
| 41 | 205.00 | 4.10 | 209.51 | false | 209.10 |
| 42 | 210.00 | 4.20 | 214.62 | false | 214.20 |
| 43 | 215.00 | 4.30 | 219.73 | false | 219.30 |
| 44 | 220.00 | 4.40 | 224.84 | false | 224.40 |
| 45 | 225.00 | 4.50 | 229.95 | false | 229.50 |
| 46 | 230.00 | 4.60 | 235.06 | false | 234.60 |
| 47 | 235.00 | 4.70 | 240.17 | false | 239.70 |
| 48 | 240.00 | 4.80 | 245.28 | false | 244.80 |
| 49 | 245.00 | 4.90 | 250.39 | false | 249.90 |
| 50 | 250.00 | 5.00 | 255.50 | false | 255.00 |
| 51 | 255.00 | 5.10 | 260.61 | false | 260.10 |
| 52 | 260.00 | 5.20 | 265.72 | false | 265.20 |
| 53 | 265.00 | 5.30 | 270.83 | false | 270.30 |
| 54 | 270.00 | 5.40 | 275.94 | false | 275.40 |
| 55 | 275.00 | 5.50 | 281.05 | false | 280.50 |
| 56 | 280.00 | 5.60 | 286.16 | false | 285.60 |
| 57 | 285.00 | 5.70 | 291.27 | false | 290.70 |
| 58 | 290.00 | 5.80 | 296.38 | false | 295.80 |
| 59 | 295.00 | 5.90 | 301.49 | false | 300.90 |
