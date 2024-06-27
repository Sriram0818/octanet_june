# octanet_june
ATM INTERFACE
=============================================================================================================================================================SOURCECODE:
=============================================================================================================================================================
import time
print("welcome to ICICI BANK")
print("INSERT YOUR CARD")
time.sleep(1)
pin=3089
password=int(input("please enter the password:"))
choice=0
balance=18000
if pin==password:
    while choice!=4:
        print(""" 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit""")
        choice=int(input("enter your choice:"))
        if choice==1:
            withdraw=int(input("enter the withdrawal amount:"))
            if balance<withdraw:
                print("Insufficient balance")
            else:
                balance=balance-withdraw
                print(f"your current balance is {balance}")
        elif choice==2:
            deposit=int(input("enter the deposit amount:"))
            balance=balance+deposit
            print(f"your current balance is {balance}")
        elif choice==3:
            transfer=int(input("enter the amount you want to transfer:"))
            recipient_name=input("enter the recipient name:")
            recipient_acc_no=int(input("enter the recipient account no:"))
            if balance<transfer:
                print("Insufficient balance")
            else:
                balance=balance-transfer
                print(f"an amount of {transfer} is transferred to {recipient_name}")
                print(f"remaining amount is{balance}")
        else:
            print("QUIT")
else:
    print("Wrong pin try Again")


OUTPUT:

Python 3.11.5 (tags/v3.11.5:cce6ba9, Aug 24 2023, 14:38:34) [MSC v.1936 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.

= RESTART: C:/Users/Srira/AppData/Local/Programs/Python/Python311/oc_task.py
welcome to ICICI BANK
INSERT YOUR CARD
please enter the password:3089
 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit
enter your choice:1
enter the withdrawal amount:5000
your current balance is 13000
 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit
enter your choice:1
enter the withdrawal amount:15000
Insufficient balance
 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit
enter your choice:2
enter the deposit amount:4000
your current balance is 17000
 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit
enter your choice:3
enter the amount you want to transfer:9000
enter the recipient name:dripthi
enter the recipient account no:4569
an amount of 9000 is transferred to dripthi
remaining amount is8000
 1==Withdraw
        2==Deposit
        3==transfer
        4==Quit
enter your choice:4
QUIT


