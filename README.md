# National Housing Registry

Final project for the Building AI course

## Summary

Describe briefly in 2-3 sentences what your project is about. About 250 characters is a nice length! 
1.	Universal registration: every residential property intended for lease must be recorded in the NHR. The system assigns a Unique Property ID (UPID)to each home. No person can legally occupy or rent property without a system-generated Lease Authorization Code.
2.	The digital trust score: the NHR tracks the financial performance of every tenant.
. Active status: granted to citizens with a history of on-time payments
. Suspended status: triggered automatically the moment a payment is missed or a lease is breached.
3.	National lockout Protocol the “Suspended” status acts as a national digital barrier. Once a individual is marked as “Untrusted” due to non-payment:
. They are electronically blocked from signing any new lease in the country
. the system notifies all current and future landlords that the individual has failed the National Reliability Standard. 
. this status remains until all debts are cleared and the penalty period is served.


## Background

Which problems does your idea solve? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?

This is how you make a list, if you need one:
* problem 1
* problem 2
* etc.
  The current rental market suffers from a “trust deficit” caused by a lack of centralized data.
Currently, landlords take a massive financial risk every time they rent to a stranger because:
•	Information Asymmetry: landlords cannot see a tenant’s real-time payment history across previous properties.
•	The “Sovereign Default” of Tenants: when a tenant stops paying, the legal process to remove them is slow and expensive, leading to “professional squatters” who move from house to house, repeating the same behavior.
•	Lack of consequence: in the current manual system, a tenant can fail to pay at one house and move to another nearby without any systemic barrier stopping them.
How common or frequent is this problem? What is your personal motivation?
•	This leads to billions in lost revenue for property owners and prevents them from reinvesting in their properties.
•	Because the problem is so common, landlords are forced to charge higher deposits and higher rent to cover the risk of bad tenants, which unfairly punishes honest people.



## How is it used?

Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?
The NHR acts as a Digital Gatekeeper.
•	Landlords use it to vet applicants instantly.
•	Tenants maintain a "Housing Passport."
•	The System automatically monitors monthly payments. If a payment is missed, the tenant's status turns "Red" nationwide.

Images will make your README look nice!
Once you upload an image to your repository, you can link link to it like this (replace the URL with file path, if you've uploaded an image to Github.)
https://unsplash.com/photos/a-house-with-a-coin-sitting-on-top-of-it-Ui4cy_D5oZ8

If you need to resize images, you have to use an HTML tag, like this:


This is how you create code examples:
```
# A simplified look at the "Eligibility Logic"
def check_tenant_status(payment_history, current_date):
    for payment in payment_history:
        if payment['status'] == 'Overdue' and payment['days_late'] > 3:
            return "RED: SUSPENDED" # National Lockout Triggered
        
    return "GREEN: CERTIFIED"

# Example Tenant Data
tenant_01 = {
    "name": "John Doe",
    "history": [{"month": "Jan", "status": "Paid", "days_late": 0},
                {"month": "Feb", "status": "Overdue", "days_late": 5}]
}

print(f"Status for {tenant_01['name']}: {check_tenant_status(tenant_01['history'], 'March')}")
```


## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
AI Techniques for “Small Data”
When i don’t have millions of records, you use specific AI techniques designed for low-data environments:
•	Expert-based Heuristics (Rule-Based AI): at the start, I don’t need a complex “black box” AI. I use Hard-Coded Logic: if payment>3 days late, status red. As data grows, you switch to machine learning to find deeper patterns.
•	Synthetic Data Generation: i can use AI to create “fake” but realistic tenant profiles to train your models. This allows me to test how the system reacts to “untrusted” behavior before the first real bad tenant even signs a lease.
•	 Transfer Learning: i can use AI models already trained on banking or Credit Card Data. These models already “understand” what a risky person looks like financially, and I simply “fine-tune” them for the housing market.


## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?
The NHR can only track what happens within its digital walls. It does not solve:
•	Cash-in-Hand Rentals: If a landlord and tenant agree to a "hidden" deal without registering on the NHR, the system has no visibility.
•	Informal Housing: It cannot easily regulate "slum" housing or informal settlements where no formal addresses exist.
•	The "Friends and Family" Loophole: The system cannot prevent someone from staying with a relative or friend for free, even if they are marked as "Untrusted" in the registry.
2. The Root Cause of Poverty
The NHR is a financial tracking tool, not a social safety net.
•	Job Loss: If a tenant loses their job due to a national economic crisis, the AI will still mark them as "Untrusted" because it only sees the missed payment, not the "why."
•	Inability to Pay: The system punishes the behavior (non-payment), but it cannot provide the tenant with the money they need. It solves the landlord's risk, but it may increase the homelessness risk for the poor.


## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 
The NHR will evolve into a National Reliability Passport. A high score could eventually grant citizens lower interest rates on bank loans, no-deposit utility connections, and better employment opportunities, turning "good renting" into a foundation for a better life.

## Acknowledgments

This is an original concept developed to fix gaps in the housing market. While Gemini (Google AI) assisted in structuring the proposal and refining the professional language, the core logic of the national "lockout" and payment-tracking registry is a unique idea created from scratch.
* etc
