# 🔐 Authentication and Authorization in Azure

## ✅ Authentication (Who are you?)

Authentication is the process of **verifying the identity** of a user, application, or device.

### How Azure handles Authentication:

- Managed by **Azure Active Directory (Azure AD / Entra ID)**
- Common methods include:
  - Username & Password
  - Multi-Factor Authentication (MFA)
  - Certificates and Tokens
  - Single Sign-On (SSO)

> **Example:** A user logs into the Azure Portal using their Microsoft account credentials.

---

## 🔓 Authorization (What can you do?)

Authorization determines **what actions** the authenticated identity is allowed to perform in Azure.

### How Azure handles Authorization:

- Managed using **Role-Based Access Control (RBAC)**
- Access is granted through:
  - **Roles** (e.g., Reader, Contributor, Owner)
  - **Scopes** (e.g., subscription, resource group, specific resource)

> **Example:** A user may be able to log in (authenticated), but only have "Reader" access to a resource (authorized to view but not modify).

---

# 👥 Grouping Users and Granting Access in Azure

## 🧑‍🤝‍🧑 1. Grouping Users

Azure uses **Azure Active Directory (Azure AD)** to organize users into **groups** for easier management.

### Benefits of Using Groups:

- Assign permissions to multiple users at once
- Simplify access control and policy management
- Reduce administrative effort

### Types of Groups:

- **Security groups** – Used to manage access to Azure resources
- **Microsoft 365 groups** – Used for collaboration (email, Teams, SharePoint, etc.)

---

## 🔐 2. Granting Access via RBAC

Azure uses **Role-Based Access Control (RBAC)** to manage permissions.

### Steps to Grant Access:

1. **Create a security group** in Azure AD
2. **Add users** to the group
3. **Assign a role** (e.g., Reader, Contributor, Owner) to the group
4. **Set the scope** (e.g., Subscription, Resource Group, or Resource)

### Example:

> Assign the "Reader" role to a security group at the resource group level to let all members view resources without making changes.

---

## 1️⃣ Managed Identity

A **Managed Identity** is used by **Azure resources** to authenticate securely without storing credentials.

### Types:

- **System-assigned** – Tied to a single resource; auto-deletes with it.
- **User-assigned** – Standalone; reusable across resources.

### Example Use Case:

An Azure vm accesses an Azure storage files without hardcoding secrets.
