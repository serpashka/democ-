# Simple Bank Account Demo

A small C# console example for creating accounts, depositing funds, withdrawing
funds, and listing account balances. The source code is stored in [`bank`](bank).

## Available operations

- Create an account with a holder name and an initial balance.
- Deposit an amount into an existing account.
- Withdraw an amount when the current balance is sufficient.
- Print all accounts, including their numbers and balances.
- Exit the console menu.

## Example calculations

The [account examples](docs/account-examples.md) show expected results for a
deposit followed by a withdrawal. They cover partial withdrawals, insufficient
funds, full withdrawals, zero amounts, and decimal balances.

These are calculation examples, not an automated test suite. Amounts are shown
as plain decimal values; the console application formats balances using the
current culture's currency format.

## Scope

Accounts are kept in memory for the current process. The example does not save
data between runs. Console input is parsed directly, so invalid numeric input
can terminate the program. This repository contains a source example rather
than a complete C# project with a build configuration.
