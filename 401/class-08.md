# Class-08 Reading Notes

It's pretty self-evident that security is extremely relevant to the design, development and deployment of web apps.

## [5 steps to RBAC](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)

1. What is Role Based Access Control (RBAC) and why do we care?
    * RBAC is the idea of assigning system access to users based on their role within an organization.
    * The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs.
    * Access is then assigned to each person based strictly on their role assignment.
    * With tight adherence to access requirements established for each role, access management becomes much easier.
2. Describe a Role/Permission heirarchy that you might implement using RBAC.
    * As an example, many healthcare organizations, given the need for regulatory compliance in controlling access to medical records, use RBAC to define exactly what access to medical records each type of clinician may need.  
    * While a doctor might have almost unlimited access to the records of patients he/she manages, a receptionist might be limited to basic contact information needed to manage appointments.  
3. What approach might you take to implement RBAC?
    * Inventory your systems.
      * e.g. email system, customer database, contact management system, major folders on a file server, etc.
    * Analyze your workforce and create roles.
      * e.g. you might have a basic user role, which includes the access any employee would need, such as email and the intranet site. Another role might be a customer service rep, that would have read/write access to the customer database, and a customer database administrator, that would have full control of the customer database.
    * Assign people to roles.
      * Now that you have a list of roles and their access rights, figure out which role(s) each employee belongs in, and set their access accordingly.
    * Never make one-off changes.
      * Resist any temptation to make a one-off change for an employee with unusual needs. If you begin doing this, your RBAC system will quickly begin to unravel. Change the roles as required or add new ones when really necessary.
    * Audit.
      * Periodically review your roles, the employees assigned to them, and the access permitted for each. If you discover, for example, that a role has unnecessary access to a particular system, change the role and adjust the access level for all employees in that role.

## [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

1. If Authentication is “you are who you say you are,” what is Authorization?
    * Authorization follows authentication -- once you are identified by subject and role, you are only authorized to do certain activities as defined by the role(s) you have, e.g. an intern is not allowed change credit limits for a customer, whereas a CFO can do do.
2. Name three primary rules defined for RBAC.
    * Role assignment: A subject can exercise a permission only if the subject has selected or been assigned a role.
    * Role authorization: A subject's active role must be authorized for the subject. With rule 1 above, this rule ensures that users can take on only roles for which they are authorized.
    * Permission authorization: A subject can exercise a permission only if the permission is authorized for the subject's active role. With rules 1 and 2, this rule ensures that users can exercise only permissions for which they are authorized.
3. Describe RBAC to a non-technical friend.
    * When I was a child, I was not allowed to go into my parents' bedroom, but my parents were certainly allowed to go into my bedroom, and now that I am a parent, similar roles apply in my house -- when I was young, I had a different role in the family than I do now, and consequently have different permissions in the family.  This is the essence of RBAC -- assigning roles (e.g. parent, child, CFO, accountant) to subjects (e.g. myself, my actual children and parents) and permissions (e.g. entering parents' bedroom, changing credit lines for customer accounts) to roles.

## [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

1. What Are access rights Associated with? The User? or The Role? Explain.
    * The role -- users are assigned roles, and roles are assigned permissions.
2. Access Rights, or Authorization, is activated after a user successfully does what?
    * Authenticates to the system, and then activates their respective roles.
3. Explain how RBAC might benefit a business.
    * Policy need not be updated when a certain person with a role leaves the organization.
    * New employee should be able to activate the desired role (easy on-boarding, audit trail, general easier management)
    * Damage containment via concept of *least privilege*
      * Basically, that you should always provide the smallest amount of access rights required for the job, e.g. a user in one role has access only to a subset of the files, i.e. an intern (or bad actor who gains intern's access to system) is not capable of taking down the system.
    * SELinux (Security-Enhanced Linux) supports RBAC, i.e. widely available, relatively inexpensive to implement.

## Things I want to know more about

1. Web security is a pretty complex realm, and would be good to learn how to navigate that world and understand what best practices are.