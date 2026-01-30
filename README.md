# Azure Identity and Access Management (IAM) Project

## Overview
This project demonstrates the implementation of Identity and Access Management (IAM) in Microsoft Azure using Microsoft Entra ID. The goal of this project is to manage users, groups, and role-based access control (RBAC) following the principle of least privilege.

---

## Objectives
- Create and manage users in Microsoft Entra ID
- Implement group-based access control
- Assign Azure RBAC roles at the resource group level
- Validate access permissions for different users

---

## Azure Services Used
- Microsoft Entra ID (Azure Active Directory)
- Azure Resource Groups
- Azure Role-Based Access Control (RBAC)

---

## Architecture / Design
- Users are created in Microsoft Entra ID
- Security groups are used to manage access
- RBAC roles are assigned to groups instead of individual users
- Access is scoped at the resource group level

---

## Implementation Steps

### 1. Resource Group Creation
A dedicated resource group was created to act as the scope for role assignments.

### 2. User Creation
Two test users were created in Microsoft Entra ID:
- IAM Admin user
- IAM Reader user

### 3. Security Groups
Two security groups were created:
- **RG-Admins**: Assigned Contributor role
- **RG-Readers**: Assigned Reader role

Users were added to their respective groups.

### 4. RBAC Role Assignment
- Contributor role assigned to RG-Admins group
- Reader role assigned to RG-Readers group
- Role assignments were scoped at the resource group level

### 5. Access Validation
- Reader user was able to view resources but not create or modify them
- Admin user was able to create and manage resources successfully

---

## Security Best Practices Applied
- Group-based RBAC instead of direct user assignment
- Least privilege access model
- Clear separation of administrative and read-only roles

---

## Key Learnings
- Understanding of Microsoft Entra ID user and group management
- Hands-on experience with Azure RBAC
- Importance of access validation and security governance

---

## Cleanup
All test resources and identities were reviewed and cleaned up to avoid unnecessary cost and security risks.

---

## Conclusion
This project demonstrates practical IAM implementation in Azure and aligns with Azure Administrator (AZ-104) responsibilities related to identity, access control, and governance.

