```markdown
# Cash Register - JavaScript Algorithm & Data Structure Project

## Overview
The **Cash Register** project simulates a cash transaction system. It determines the change to return to a customer based on the purchase price, payment amount, and cash available in the register (cash-in-drawer). The system handles various scenarios, including insufficient funds, exact change, and providing change in optimal denominations.

---

## How It Works
The core function, `checkCashRegister(price, cash, cid)`, receives three parameters:
- `price`: The purchase price.
- `cash`: The payment amount.
- `cid`: Cash-in-drawer, an array representing available currency.

### The function performs the following:
1. Calculates the change due.
2. Checks if cash-in-drawer covers the change.
3. Uses a greedy algorithm to give the highest denominations first.
4. Handles special cases:
   - **INSUFFICIENT_FUNDS**: Not enough cash to give change.
   - **CLOSED**: Cash in drawer equals the change, closing the register.
   - **OPEN**: Can give change, and the register remains open.

---

## Currency Units and Values
| Currency        | Code          | Value  |
|-----------------|---------------|---------|
| Penny           | PENNY         | $0.01  |
| Nickel          | NICKEL        | $0.05  |
| Dime            | DIME          | $0.10  |
| Quarter         | QUARTER       | $0.25  |
| One             | ONE           | $1.00  |
| Five Dollars    | FIVE          | $5.00  |
| Ten Dollars     | TEN           | $10.00 |
| Twenty Dollars  | TWENTY        | $20.00 |
| Hundred Dollars | ONE HUNDRED   | $100.00|

---

## Example Data Structure for `cid`

```js
[
  ["PENNY", 1.01],
  ["NICKEL", 2.05],
  ["DIME", 3.10],
  ["QUARTER", 4.25],
  ["ONE", 90],
  ["FIVE", 55],
  ["TEN", 20],
  ["TWENTY", 60],
  ["ONE HUNDRED", 100]
]
``

---

## Usage

### Basic Example
```js
const result = checkCashRegister(19.5, 20, [
  ["PENNY", 1.01],
  ["NICKEL", 2.05],
  ["DIME", 3.10],
  ["QUARTER", 4.25],
  ["ONE", 90],
  ["FIVE", 55],
  ["TEN", 20],
  ["TWENTY", 60],
  ["ONE HUNDRED", 100]
]);

console.log(result);
``

### Expected Output
```json
{
  "status": "OPEN",
  "change": [["QUARTER", 0.5]]
}
``

---

## Implementation Details

- **Function Name:** `checkCashRegister`
- **Parameters:**
  - `price` (Number): Purchase price.
  - `cash` (Number): Payment amount.
  - `cid` (Array): Cash in drawer.

- **Returns:** An object with `status` and `change` keys.

---

## How to Run
1. Save the code in a JavaScript file, e.g., `cashRegister.js`.
2. Run in your environment or browser console.
3. Call the function with different test cases to verify.

---

## License
This project is for educational purposes. Feel free to modify and adapt the code as needed.

---

## Contact
For questions or feedback, reach out to [Your Name or Email].

---

**Happy coding!**
```

---
