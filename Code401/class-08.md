#  Access Control (ACL)

## 5 steps to RBAC

<https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html>

**What is Role Based Access Control (RBAC) and why do we care?**

The idea of assigning system access to users based on their role within an organization.

It limits who and what type of data a person has access to within a system. Which limits vulnerabilty within an organization.

**Describe a Role/Permission heirarchy that you might implement using RBAC.**

**Access control lists (ACL)** — An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document.

**Attribute-based access control (ABAC)** — ABAC, sometimes known as policy-based access control, can use a variety of attributes, including user department, time of day, location of access, type of access required, etc. to determine whether a user’s access request should be granted.

**What approach might you take to implement RBAC?**

1. Inventory your systems-
Figure out what resources you have for which you need to control access, if you don't already have them listed.

2. Analyze your workforce and create roles-
group your workforce members into roles with common access needs.  Avoid the temptation to have too many roles defined. Keep them as simple and stratified as possible.

3. Assign people to roles-
Now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.

4. Never make one-off changes-
esist any temptation to make a one-off change for an employee with unusual needs. If you begin doing this, your RBAC system will quickly begin to unravel. Change the roles as required or add new ones when really necessary.

5. Audit-
Periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role.

## wiki - RBAC

<https://en.wikipedia.org/wiki/Role-based_access_control>

**If Authentication is “you are who you say you are,” what is Authorization?**

Authorization is the level of access to information you're given. 

**Name three primary rules defined for RBAC.**

Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.

Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.

Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.

**Describe RBAC to a non-technical friend.**

RBAC is an approach to security as it relates to access of company systems and documents. It controls who needs to see what based on thier role within an organization.

## RBAC tutorial

<https://www.youtube.com/watch?v=C4NP8Eon3cA>

**What Are access rights Associated with? The User? or The Role? Explain.**

The Role-It determines which type of access to files and types based on thier role.

User only has access once they are assigned to a role.

**Access Rights, or Authorization, is activated after a user successfully does what?**

Has been authenticated and assigned a role.

**Explain how RBAC might benefit a business.**

It limits who has access to sensitive data. 
It provides only the access to files needed within a role.
It provides a preset policy for what level of access is needed based on role and when.

### Things I want to know more about

Tool to aid in RBAC set-up:

identity management <https://www.csoonline.com/article/2120384/identity-management/what-is-iam-identity-and-access-management-explained.html>