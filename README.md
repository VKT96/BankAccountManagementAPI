# BankAccountManagementAPI
This is a C#/.NET API Project Created Using Entity Framework Code First Approach

The sample requests and responses are as listed below.
http://localhost:23848/BankAccountManager/LoanApplication
Request:
{
"customerName": "Jim",
"Term":3,
"LoanAmount":500
}
Response:
{
    "loanApplicationStaus": "Approved",
    "loanAccountNumber": 6,
    "message": "Account created sucessfuly. New account balance is - 10400"
}

http://localhost:23848/BankAccountManager/MoneyTransfer
Request:
{
"FromAccountId": 1,
"ToAccountId":2,
"Amount":600
}
Response:
{
    "moneyTransferStatus": "Transaction Successful.",
    "message": "New Account balance is From Account - 5000, To Account Balance - 11000"
}


http://localhost:23848/BankAccountManager/Customer
Response:
[
    {
        "id": 1,
        "userName": "Bob",
        "creditRating": 15,
        "accounts": null
    },
    {
        "id": 2,
        "userName": "Jim",
        "creditRating": 45,
        "accounts": null
    },
    {
        "id": 3,
        "userName": "Anne",
        "creditRating": 80,
        "accounts": null
    }
]


http://localhost:23848/BankAccountManager/Details/Bob
Response:
{
    "id": 1,
    "userName": "Bob",
    "creditRating": 15,
    "accounts": [
        {
            "id": 1,
            "customerId": 1,
            "balance": 5600,
            "accountType": 1,
            "term": null,
            "interestRate": null,
            "loanAmount": null
        }
    ]
}
