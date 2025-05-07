# 02 - Role-Based Access Control (RBAC)

**Purpose:**
Document how to explore and assign Entra ID directory roles, and how to assign Azure RBAC roles on resources.

---

## Prerequisites
- Completed **01 - Entra ID (Azure AD) Setup**, with portal access and a 'lab-test-user' created.

---

## 1. Explore & Assign Entra ID Directory Roles
1. In the Azure portal, go to **Microsoft Entra ID** (**Azure Active Directory**) -> ***Roles and administrators** (under Manage).
![image](https://github.com/user-attachments/assets/fd17a6a6-315e-4726-9541-146d1fe7e754)
2. Browse the built-in roles (e.g., **Global Adminstrators**, **User Administrator**, **Security Reader**).
3. Click **User Administrator** -> **+ Add assignments**.
4. Locate and select **lab-test-user** (search if needed), then click **Add**.
   
---

## 2. Create a Resource Group
1. Using the main search bar, search for **Resource groups** (navigate to the portal if needed).
2. Click **+ Create**.
3. Enter:
   - **Subscription**: Your subscription (e.g., Azure subscription 1)
   - **Resource group name**: 'lab-rbac-rg'
   - **Region**: Select region right for you (e.g., **East US**)
4. Click **Review + Create** -> **Create**
![image](https://github.com/user-attachments/assets/eaa83413-1c67-4221-b58a-a8ecd12a223b)

---

## 3. Assign an Azure RBAC Role
1. Navigate to **lab-rbac-rg** -> **Access control (IAM)**. <br>
![image](https://github.com/user-attachments/assets/68afa9e5-97eb-4701-9d51-64316c44c06a)
3. Click **+ Add** -> **Add role assignment**.
4. Select **Role**: **Reader**.
![image](https://github.com/user-attachments/assets/6f9c81e2-a684-4285-ba39-55b946a20712)
5. Under **Assign access to**, choose **User, group, or service principal** (default)
6. Click **Select members**, choose **lab-test-user**, then **Select**.
7. Click **Review + assign** -> **Assign**.
![image](https://github.com/user-attachments/assets/f9a1eb50-0561-4ac5-b78d-7d6f0eddec1e)

## 4. Observations & Next Steps
- ✔️ **lab-test-user** now has **User Administrator** in Entra ID and **Reader** on the 'lab-rbac-rg' resource group.
- ❓ Experiment: Try signing in as **lab-test-user** and verify you can view (but not modify) resources in 'lab-rbac-rg'.

## Finished!
**Next up:**
- Multi-Factor Authentication (MFA) setup and Conditional Access policies (documented in '03-mfa.md'
