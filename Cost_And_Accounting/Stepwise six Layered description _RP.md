**Managed Group 6-Layered Architecture Diagram**

**Managed Group 6-Layered Architecture details step-by-step:**

1.  **Enterprise Root Management Group**
    *   Centralized control by Enterprise IT.
    *   Provides company-wide cost reporting and governance.
2.  **Business Unit Management Groups**
    *   Apparel
    *   Sporting Goods
    *   Each unit has its own management group for accountability.
3.  **Department Subscriptions**
    *   Product Development, Marketing, Sales under each business unit.
    *   Enables granular cost tracking and reporting.
4.  **Project Subscription / Tagged Resources**
    *   Dedicated subscription or tagged resource groups for the **Customer Feedback Project**.
    *   Ensures CFO visibility into project-specific costs.
5.  **Azure Policy & Blueprints**
    *   Enforce VM sizing (low-cost SKUs for testing).
    *   Enforce naming conventions (CFB-Test-VM01).
    *   Automatically flag non-compliance.
6.  **Enterprise IT Cost Reporting & Monitoring**
    *   Roll-up reporting across all subscriptions.
    *   Dashboards for spend analysis, compliance, and performance monitoring.

*   **Cost Optimization:** Clear accountability per unit + project tagging (lableing).
*   **Operational Excellence:** Policies and blueprints enforce standards.
*   **Security & Reliability:** RBAC and monitoring at management group level.
*   **Performance Efficiency:** Right-sized resources for testing and scaling.

This layered approach ensures **clarity, compliance, and efficiency** while aligning with the **Azure Well-Architected Framework pillars**.