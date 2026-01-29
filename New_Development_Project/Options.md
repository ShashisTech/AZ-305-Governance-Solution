
<H1>Option1: Using Dedicated Azure Subscription</H1>
<H2></H2>A dedicated subscription (i.e.) standalone container can be used to isolate projects.</H2>
<H2>Pointers:</H2>
<ol>•	New development project can be created under CFO management group with a dedicated subscription</ol>
<ol>•	Using Azure Cost Management & Billing – can track, monitor and set limits for cost.</ol>
<ol>•	Budget and thresholds can be set for the new development project scope.</ol>
<ol>•	Tagging Standard – Apply new project name as prefix to all resources. By tagging, cost incurred can be broken down to resource level.</ol>
<ol>•	Policy enforcement using Azure policy to enforce tag/resource naming standard followed.</ol>
<ol>•	Role Based Access assigned at the subscription level.</ol>
<ol>•	Quota management can be applied if needed for PLT testing.</ol>
<ol>•	Use Azure policy with Audit effect to evaluate and validate compliance.</ol>
<ol>•	In testing phase, use spot instances Or B series for hosting the workload.</ol>
<img width="779" height="582" alt="image" src="https://github.com/user-attachments/assets/32ee3d40-e71a-420e-b841-50aa7fb5985a" />


<H1>Option 2: Using Resource Groups </H1>
<ol>•	Project team roles are assigned only at Resource group level. Ensure roles assigned at subscription level are not assigned to new development team members.</ol>
<ol>•	Mandatory and disciplined usage of tags – new resource group must have a unique tag and each resource under it should have it as prefix (Apply Tag inheritance policy).</ol>
<ol>•	Budget can be scoped specifically to a resource group.</ol>
<ol>•	Using Azure Cost Management apply Resource Group or tag as filter to get cost incurred.</ol>
<ol>•	Policy enforcement using Azure policy to enforce tag/resource naming standard followed.</ol>
<ol>•	Use Azure policy with Audit effect to evaluate and validate compliance.</ol>
<img width="825" height="549" alt="image" src="https://github.com/user-attachments/assets/3d21485d-397e-4243-acee-798e20887a95" />
