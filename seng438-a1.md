# *Lab. Report \#1 – Introduction to Testing and Defect Tracking*

| Group: 17|
|-----------------|
| Mirza Hassan Baig|
| Mohamad Hammoud|
| Masroor Posh|
| Mohamad Hussein|

## Comparison Between Exploratory and Manual Scripted Testing

  - **Manual Scripted Testing** was more effective at identifying the critical system functionalities since it followed predefined test cases and ensured that all core features were tested. This method helped us most in cathing major defects related to incorrect balance updates and authentication too.
  - **Exploratory Testing** was effective in identifying unexpected edge cases  and usability issues. Since there was more freedom allowed with exploratory testing, behaviours that were not explicityly covered in manaul scripted test cases were discovered. Exploratory testing was more efficient in uncovering surface-level issues as well.

Overall, combining both methods provided us with comprehensive defects detection with scripted testing ensuring consistency and core functionality and exploratory testing revealing hidden bugs.
# Manual Scripted Testing 

High-Level Description of our Manual Scripted Testing Approach

In this phase, my teammate and I targeted the most critical features of the ATM system to ensure that they functioned as expected. We identified these features based on their impact on user experience and system integrity. Our primary focus included the following:

• Deposit Transactions: To verify that funds are correctly added to the user’s account and accurately reflected in the balance. 

• Fund Transfers: To confirm that transfers between accounts are accurate and do not result in discrepancies. 

• Error Handling for Invalid Inputs(primarily regarding User Auth): To check that the system properly rejects invalid inputs and provides appropriate feedback to the user. 

We systematically followed the test cases provided in the test suite from Appendix C, while also expanding on them with other test cases in the Appendix where necessary to uncover edge cases and hidden bugs. 

## Test Execution Process

During the manual Scripted Testing phase, 1 person acted as the test operator, executing the test steps and interacting with the ATM system while the other teammate in the pair recorded the actual outcomes and document any defects found. We handpicked the tests that were relevant to the core functionality of the ATM and explored other test cases from the Appendix that were similar to some of the failing test cases. 

We began with the tests that were related to the user authentication, followed by deposit and transfer transactions tests, along side these tests we also did the test cases surrounding the error handling mechanisms. 

Test Cases and Observations 


| Feature  | Test Description  | Expected Outcome  | Actual Outcome  |
| -- | -- | -- | -- |
| Deposit Transactions  | Incorrect Balance Update After Deposit Transaction to Checking Account   | The deposited amount should be correctly added to the total and available balances.  | The total and available balances do not reflect the deposited amount accurately, leading to incorrect account information (Ten dollars less than expected.  |
| Deposit Transactions  | Incorrect Balance Update After Deposit Transaction to Savings Account  | The deposited amount should be correctly added to the total and available balances.  | The total and available balances do not reflect the deposited amount accurately, leading to incorrect account information.  |
| Money Transfers  | Incorrect Balance Update After Transfer from Checking to Savings  | The transferred amount should be deducted from the checking account and added to the savings account correctly.  | The total and available balances are miscalculated, leading to incorrect financial records for the user.  |
| Error Handling  | Re-entry of correct pin fails after an invalid pin entry  | The system should accept the correct PIN and proceed to display the transaction menu.  | The system incorrectly prompts the user to re-enter the PIN again, preventing the user from continuing to the transaction menu.  |
| Error Handling  | Invalid Card Exception Not Triggered Immediately  | The system should immediately throw an "Invalid Card" exception after entering an invalid card number.  | The system prompts for a PIN entry after entering an invalid card number.  |


## Conclusion

Our Manual Testing focused on the verification of the critical functionalities in the ATM system to help ensure that the core features such as deposit transactions, transfers, and error handling worked as expected. This structured approach and systematically executing the more relevant test cases we were able to identify multiple defects around the core 

functionality of the ATM. Despite one of the bugs being resolved in version 1.1 most of the

bugs were largely still unresolved highlighting the importance of regression testing.

# Exploratory Testing 

Test plan

Exploratory Testing Plan for ATM Software

### 1. Card Insertion & PIN Entry 

• Test Steps: 

o Test valid and invalid card insertion. 

o Enter correct/incorrect PIN, including 3 failed attempts.

o Verify card retention after 3 failed PIN attempts.

### 2. Transaction Testing 

## • Withdrawal: 

o Test various withdrawal amounts (valid and invalid).

o Test insufficient funds scenario.

o Verify bank approval before dispensing cash.

## • Deposit: 

o Test envelope deposit with cash/checks.

o Test timeout and cancel scenarios.

o Verify bank approval and envelope collection process.

## • Transfer: 

o Test fund transfer between accounts. 

o Test invalid amount/account scenarios. 

## • Balance Inquiry: 

o Test balance inquiry for different account types.

o Verify correct balance display. 

## • Cancel Transaction: 

o Test aborting transactions at various stages.

o Verify proper transaction rollback and cancellation.

## 3. Error Handling 

## • Test Steps: 

 Simulate communication failures with the bank.

o Test for invalid deposit entries and insufficient funds scenarios.

o Ensure appropriate error messages are displayed.

o Verify system recovery after failure. 

## 4. Security Testing 

## • Test Steps: 

o Ensure PIN input is masked and secure.

o Test session timeout (idle for an extended period).

o Verify card retention and correct handling of failed PIN attempts.

## 5. Operator Controls

### • Test Steps: 

o Verify the operator can start and stop the ATM. 

o Test cash reload functionality.

o Verify proper handling of deposit envelopes by the operator.

## 6. Receipt & Log Verification

• Test Steps: 

o Verify that receipts contain the correct information (account, transaction, balance). 

o Ensure logs capture events without storing sensitive data like the PIN.

o Test that logs include bank communication and transaction statuses.

## Conclusion 

This exploratory testing plan covers key functional, security, and usability areas. It aims to uncover issues in the ATM software by testing various transaction flows, error handling, and the overall user experience. `` 



