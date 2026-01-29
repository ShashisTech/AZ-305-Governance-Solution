**What are the different ways Tailwind Traders could track costs for the new development project?**

**1\. Resource Tagging**

Tagging is the most flexible way to track costs, especially if project resources are spread across different regions or services.

*   **Implementation:** Apply a mandatory tag like Project: Customer Feedback to every resource created for the project.
*   **Advantage:** In **Azure Cost Analysis**, you can filter the entire company's spend by this specific tag to see a consolidated project bill.
*   **Enforcement:** Use **Azure Policy** with the "Deny" effect to prevent any resource from being created in the project's scope if it lacks the required tag.

**2\. Dedicated Resource Group**

Since this is a new development project, keeping all its components (VMs, Databases, App Services) in a single **Resource Group (RG)** is the simplest administrative method.

*   **Implementation:** Create an Resource Group named rg-customer-feedback-dev.
*   **Advantage:** You can view costs directly at the Resource Group level in the Azure Portal without needing complex filters. It also simplifies cleanup once the testing phase is over.

**3\. Azure Budgets and Alerts**

To satisfy the CFO’s need for "captured costs" and proactive management, budgets are essential.

*   **Implementation:** Set a monthly budget at the Resource Group or Subscription level.
*   **Alerting:** Configure alerts to trigger at 50%, 75%, and 90% of the budget. These alerts can send emails to the CFO or trigger a **Logic App** to pause non-essential resources if the budget is exceeded.

**4\. Dedicated Subscription (Isolation)**

If the project is expected to scale significantly or requires completely different billing terms, a dedicated subscription is an option.

*   **Advantage:** This provides a "hard" billing boundary. The invoice from Microsoft will show this subscription as a separate line item, leaving zero room for accounting errors.

**5\. Automated Identification (Azure Policy)**

The requirement mentions that "non-compliance should be automatically identified."

*   **Audit Policies:** Use Azure Policy to audit any resources that do not follow the naming convention (e.g., resources that don't start with CFP-).
*   **Compliance Dashboard:** The **Azure Policy Compliance** dashboard will provide a real-time list of "off-budget" or improperly named resources that need remediation.

NOTE: For Tailwind Traders, the best approach is **Method 2 (Dedicated Resource Group)** combined with **Method 1 (Resource Tagging)**. Using a dedicated Resource Group makes management easy, while enforced Tagging ensures that even if a developer accidentally puts a resource elsewhere, it still shows up in the project's cost report.