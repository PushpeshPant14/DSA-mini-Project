# Loan Processing Automation System

## Project Title
Loan Processing Automation System

## Group Members (Group J)
- Satyam Sharma – 25/SCA/MCAN/055  
- Pushpesh Pant – 25/SCA/MCAN/052  
- Maniya – 25/SCA/MCAN/054  
- Kashish Kaushik – 25/SCA/MCAN/056  

## Project Description
This project implements a Loan Processing System in C language that automates key loan-related tasks such as:  
- Loan Eligibility Checking  
- EMI Calculation  
- Total Interest Estimation  
- Month-by-month Repayment Schedule  

It uses structures, functions, and mathematical calculations to simulate a real-world loan approval workflow.

## Technology & Libraries Used
- Programming Language: C  
- Libraries:  
  - <stdio.h> for input/output  
  - <math.h> for power function used in EMI calculation  

## Features
1. Automated Eligibility Check  
   - Loan approved only if:  
     - Credit Score ≥ 650  
     - Debt-to-Income Ratio ≤ 50%  
   - Uses a function comparing income, current debt, and EMI.  

2. EMI Calculator  
   - EMI calculated using formula:  
     \[
     EMI = \frac{P \times R \times (1+R)^N}{(1+R)^N - 1}
     \]
     where P = Principal, R = Monthly Interest Rate, N = Tenure (Months)  

3. Financial Summary  
   - Displays loan amount, monthly EMI, total repayment, and total interest cost.  

4. Amortization Schedule  
   - Month-wise breakdown of EMI, interest, principal, remaining balance.  
   - Ensures last balance is correctly adjusted to zero.  

5. Clean Input & Output  
   - User-friendly prompts with formatted output tables.

## Project File Structure
LoanProject/
│
├── loan_processing.c
├── README.md
└── (optional) output_screenshot.png

text

## How It Works
- Uses two structures:  
  - Applicant (Income, Debt, Credit Score)  
  - LoanRequest (Principal, Rate, Tenure)  
- EMI calculated with pow() function  
- checkEligibility() function:  
  - Returns 1 (Approved) if credit score ≥ 650 and obligations < 50% income  
  - Otherwise returns 0 (Rejected)  
- If approved: summary printed, user can view full repayment schedule  
- Monthly loop calculates:  
  - Interest = RemainingBalance × MonthlyRate  
  - Principal = EMI – Interest  
  - New Balance = OldBalance – Principal

## How to Run
On Windows (GCC / CodeBlocks):  
gcc loan_processing.c -o loan
./loan

text
On Linux:  
gcc loan_processing.c -lm -o loan
./loan

text

## Conclusion
This project models a real-life loan approval system combining data structures, mathematical logic, and financial calculations providing a structured workflow used in financial software.
