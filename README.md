# 🚀 Terraform Azure RBAC Project

## 📌 Project Overview

This project demonstrates how to implement **Identity and Access Management (IAM)** in Azure using Terraform.

It automates:

* Azure AD (Microsoft Entra ID) user creation
* Role-based group creation
* Azure RBAC role assignment (Owner, Contributor, Reader)

---

## 🧰 Technologies Used

* Terraform
* Azure CLI
* Microsoft Entra ID (Azure AD)
* Azure Resource Manager (RBAC)
* Git & GitHub
* Visual Studio Code

---

## 🎯 Features

✔ Bulk user creation using Terraform
✔ Role-based access control (RBAC)
✔ Dynamic group assignment
✔ Azure subscription-level role assignment
✔ Infrastructure as Code (IaC) implementation

---

## 👥 Users & Roles

| User   | Role     |
| ------ | -------- |
| atique | Admin    |
| noman  | Dev      |
| aleena | Dev      |
| amaira | ReadOnly |
| addu   | ReadOnly |
| nida   | Dev      |
| sadia  | ReadOnly |
| maria  | Dev      |
| nishat | ReadOnly |
| hamza  | Admin    |
| khirad | Dev      |
| nahid  | ReadOnly |

---

## 👥 Azure AD Groups

* 🔴 Admin-Group
* 🟡 Dev-Group
* 🟢 ReadOnly-Group

---

## 🔐 Azure RBAC Roles

| Group          | Role        |
| -------------- | ----------- |
| Admin-Group    | Owner       |
| Dev-Group      | Contributor |
| ReadOnly-Group | Reader      |

---

## 📂 Project Structure

```id="pstr1"
terraform-azure-users/
│
├── main.tf
├── .gitignore
└── README.md
<img width="1536" height="1024" alt="architecture png" src="https://github.com/user-attachments/assets/779ef349-981a-47d9-9301-89e043418e23" />


```

---

## ⚙️ Prerequisites

* Terraform installed
* Azure CLI installed
* Azure account
* Logged in using:

  ```
  az login
  ```

---

## 🛠️ How to Run

### 1. Clone repository

```id="run1"
git clone https://github.com/nigarpk27/terraform-azure-users.git
cd terraform-azure-users
```

---

### 2. Initialize Terraform

```id="run2"
terraform init
```

---

### 3. Validate configuration

```id="run3"
terraform validate
```

---

### 4. Preview changes

```id="run4"
terraform plan
```

---

### 5. Apply configuration

```id="run5"
terraform apply
```

Type `yes` when prompted.

---

## 🔍 Verification

Check users:

```id="ver1"
az ad user list --output table
```

Check RBAC roles:

```id="ver2"
az role assignment list --all --output table
```

---

## ⚠️ Security Note

* Passwords are hardcoded for learning purposes
* Do NOT use this approach in production
* Use:

  * Azure Key Vault
  * Environment variables
  * Secure secrets management

---

## 🧠 Architecture Flow

```id="flow1"
Users → Azure AD Groups → RBAC Roles → Azure Subscription
```

---

## 🚀 Future Enhancements

* 🔐 Integrate Azure Key Vault
* 🔄 Add GitHub Actions CI/CD pipeline
* 📦 Store Terraform state in Azure Storage
* 📊 Add architecture diagram
* 🏢 Implement resource group-level RBAC

---

## 📧 Author

GitHub: [https://github.com/nigarpk27](https://github.com/nigarpk27)

---

## ⭐ If you found this useful

Give this repository a star ⭐
