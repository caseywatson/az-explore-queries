# Azure VM Exploration Queries

Welcome to **Azure VM Exploration Queries**, a collection of flexible Azure Resource Graph (ARG) queries designed to help IT professionals rapidly "size up" and analyze VM-based Azure environments based on specific workloads. This repository includes a series of Kusto Query Language (KQL) scripts that let you group virtual machines (VMs) according to naming conventions, tags, resource groups, and more, giving you insights into VM inventory, SKU usage, VM Scale Sets (VMSS), and availability zone distribution.

## Overview

Each query in this repository is structured to support easy and customizable VM grouping. Simply read the **commented "Grouping Options" section** in each script, select the option that best fits your environment, and uncomment the relevant line(s). This flexible approach makes it easy to tailor analyses to your specific needs, whether you’re working with small applications or complex, multi-tier workloads.

## Queries Included

| Query File                 | Description                                                                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**vm_group_inventory.kql**](vm_group_inventory.kql) | Provides a full inventory of VMs grouped by your chosen method. This query helps you understand how VMs are distributed across your environment, giving you an overview of each group’s VM count and resource allocation. |
| [**vm_group_sku_analysis.kql**](vm_group_sku_analysis.kql) | Analyzes the VM SKUs within each group, allowing you to assess resource allocation, identify cost implications, and optimize SKU usage based on workload requirements. |
| [**vm_group_vmss_analysis.kql**](vm_group_vmss_analysis.kql) | Examines VM Scale Sets (VMSS) associated with each group, offering insights into scalability and deployment configurations for each workload. |
| [**vm_group_zone_analysis.kql**](vm_group_zone_analysis.kql) | Evaluates the distribution of VMs across availability zones within each group, providing insights into redundancy, fault tolerance, and geographic placement. |

## How to Use

1. **Choose Your Grouping Option**: Each query includes a "Grouping Options" section with multiple methods for grouping VMs (e.g., by name prefix, custom regex pattern, resource group, or tag). Review the comments in this section, choose the option that best matches your environment, and uncomment the relevant line(s).
  
2. **Customize If Needed**: For some options, such as regex patterns or specific tags, you may need to adjust values to fit your organization’s conventions. Use Copilot or other tools to build regex patterns quickly if needed.

3. **Run the Query**: Once you’ve configured the grouping, run the query in Azure Resource Graph Explorer to get a detailed view of VM distribution, SKU usage, or zone alignment based on your configuration.

## License

This project is licensed under the MIT License, allowing free use, modification, and distribution. See [LICENSE](./LICENSE) for details.

---

These queries are designed to be as simple and adaptable as possible, empowering you to quickly assess and manage Azure VM environments. For questions or contributions, feel free to open an issue or submit a pull request. Happy querying!
