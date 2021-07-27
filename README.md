# Queue-Teller-System

![pexels-croberin-photography-1422408-min](https://user-images.githubusercontent.com/86560575/127117871-05973ece-4ae7-438d-bda7-c018486fdc16.jpg)

Our user from banking company given us the job to develop a program to manage the customers queue in a Bank. The management want you to create a system that ables to divides the right amount of queue length for each bank teller, so that there is no one teller that get a longer queue than other tellers.

However, not like the usual Bank Teller Queue Management System you found at your local bank where the system only calls the queue number, the management want the program to also be able to calls the customer's name.  Assume that there are 5 tellers available at the Bank: Angel, Mellysa, David, Thom, and Monica.

our user also wanted to know names of the first and the last customer from the program which we develop

![lisanto-pT4gB7T6tog-unsplash-min](https://user-images.githubusercontent.com/86560575/127120731-85153467-e574-4caa-89ad-8c9fdc3fd437.jpg)

We use python to develop this project as below
```python
import numpy as np #import package first
```

```python
# teller name
queue_dict = {'Angel':[],
              'Mellysa':[],
              'David':[],
              'Thom':[],
              'Monica':[]
              }
```

```python
#customer queue
customer_name_list = []
queue_no = 0
while True:
    queue_no += 1

#print Queue Number and input queue number
    print(f"Queue No {len(customer_name_list)+1}")
    customer_name = input("Enter Customer Name: ")
    if customer_name == '':
        break

#Find the teller that has lowest number of queue
    lowest_queue = np.inf
    for teller_name, customers_queue in queue_dict.items():
        if len(customers_queue)<lowest_queue:
            lowest_queue = len(customers_queue)
            chosen_teller = teller_name

# Get the customer on the queue of the chosen teller
    queue_dict[chosen_teller].append(customer_name)

# List to store customer name and get the order of the customer
    customer_name_list.append(customer_name)

# print customer which go to the teller name
    print(f"{customer_name}, please go the teller {chosen_teller}")
    print()
```

![teller](https://user-images.githubusercontent.com/86560575/127119103-9c927bef-faa4-41a0-abca-4fa60b0198b2.JPG)

then we get the first and the last customer queue as below

```python
#get to Know the first customer
print(f"The First Customers today is {customer_name_list[0]}")

#atau bisa juga menggunakan
print(f"The first customer in this day is {customer_name_list[0]}")
```
![teller1](https://user-images.githubusercontent.com/86560575/127119478-6c0c59a6-5ab0-40ce-8aaf-76baaf139e28.JPG)


```python
#get to know the last customer
print(f"The Last Customers today is {customer_name_list[-1]}")

#atau bisa juga menggunakan
print(f"The last customer in this day is {customer_name_list[-1]}")
```
![teller2](https://user-images.githubusercontent.com/86560575/127119735-68782f8e-f0e9-4b81-8cea-220850d83dd6.JPG)

please see the complete python in our ipynb at our folder colaboratory
