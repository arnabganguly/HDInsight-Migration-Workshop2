## Create the storage account

1. Go to the Azure Home page and select **Create a resource**.

1. On the **New** page, in the **Search the Marketplace** box, type **storage account**, and then select **Storage account** from the list that appears.

1. On the **Storage account** page, select **Create**.

1. On the **Basics** tab of the **Create storage account** page, enter the following settings, and then select **Next : Networking**:

    | Field | Value|
    |-|-|
    | Subscription | Select your subscription |
    | Resource group | workshoprg*9999* |
    | Storage account name | clusterstorage*9999*, where *9999* is your unique suffix |
    | Location | Select the same region used by the Cloudera or MapR virtual machine and the **workshoprg*9999*** resource group |
    | Performance | Standard |
    | Account Kind | StorageV2 (general purpose v2) |
    | Replication | Zone-redundant storage (ZRS) |

1. On the **Networking** tab, accept the default settings, and then select **Next : Data protection**.

1. On the **Data protection** tab, accept the default settings, and then select **Next : Advanced**.

1. On **Advanced** tab, under **Data Lake Storage Gen2**, select **Enabled** for **Hierarchical namespace**. Leave all other settings at their default values, and then select **Review + create**.

1. On the validation page, select **Create**, and wait while the storage account is created.
