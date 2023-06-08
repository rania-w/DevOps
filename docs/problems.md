# Phase 1 - issues

The AWS calculator was very confusing, and we were forced to find our own methods to estimate the cost.

# Phase 2 - issues

## Task 1 - Creating VPC

- When creating security groups, we overlooked our security group inbound and outbound rules, which led to debugging.

## Task 2 - Launching VM
- We were not sure which given role we should have used, so we used the EC2 role, and attached a policy which allows us to access the session manager
- There was an assumption that we were supposed to paste the given script "UserdataScript-phase-2.sh" in the *User data* section, which was wrong.
- The title *Amazon machine image* was slightly misleading, so when we finally created the script using the session manager on the EC2 instance, there was an error indicating that we chose an incompatible OS for the given script.

# Phase 3

## Task 6
- Generally, migrating the database is prone to many errors and obstacles. For instance we had to use root priviliges on the instance to gain access to the database at all.

# Phase 4 
