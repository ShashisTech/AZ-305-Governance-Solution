*   **Cost Tracking Approaches**

1.  **Dedicated Subscription for the Project**
    *   All resources for the customer feedback project live in one subscription.
    *   Simplifies cost tracking and reporting.
2.  **Resource Tagging**
    *   Apply tags like Project=CustomerFeedback, Environment=Testing.
    *   Enables granular cost analysis across shared subscriptions.

**Final Decision:** Use **tags** for flexibility (especially if project resources span multiple subscriptions) but also consider a **dedicated subscription** if the CFO wants strict isolation.

*   **Compliance for VM Sizing & Naming**

1.  **Azure Policy**
    *   Enforce allowed VM SKUs (e.g., only B-series or D-series for testing).
    *   Enforce naming convention (e.g., CFB-Test-VM01).
    *   Automatically flag non-compliance.
2.  **Azure Blueprints**
    *   Bundle policies, RBAC, and resource templates for consistent deployment.
    *   Ensures compliance from the start.

**Final Decision:** Use **Azure Policy** for enforcement + **Blueprints** for deployment consistency. This ensures both proactive and reactive compliance.

*   **Well-Architected Framework Pillars**

| Pillar | Implementation |
| --- | --- |
| Cost Optimization | Subscription hierarchy, tagging, low-cost VM SKUs, cost alerts. |
| Operational Excellence | Azure Policy, Blueprints, automated compliance checks. |
| Performance Efficiency | Right-sized VMs, scaling rules for production workloads. |
| Reliability | Resource consistency rules, monitoring, backup policies. |
| Security | RBAC at management group level, Azure Defender, secure naming conventions. |