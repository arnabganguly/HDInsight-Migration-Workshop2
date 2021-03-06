## Create the user assigned managed identity

1. Go to the Azure Home page and select **Create a resource**.

1. On the **New** page, in the **Search the Marketplace** box, type **user assigned**, and then select **User Assigned Managed Identity** from the list that appears.

1. On the **User Assigned Managed Identity** page, select **Create**.

1. On the **Basics** tab of the **Create User Assigned Managed Identity** page, enter the following settings, and then select **Review + create**:

    | Field | Value|
    |-|-|
    | Subscription | Select your subscription |
    | Resource group | workshoprg*9999* |
    | Region | Select the same region used by the Cloudera or MapR virtual machine and the **workshoprg*9999*** resource group |
    | Name | clustermanagedid |

1. On the validation page, select **Create**, and wait while the user assigned managed identity is created.

1. On the Home page in the Azure portal, select **Resource Groups**, and then select the **workshoprg*9999*** resource group. 

1. On the **workshoprg*9999*** resource group page, select  **clusterstorage*9999***, where **9999** is the id you specified when you created the storage account earlier.

1. On the **clusterstorage*9999*** page, select **Access Control (IAM)**:

    ![The **clusterstorage*9999*** page in the Azure portal. The user has selected **Access Control (IAM)**](../ClouderaMigration/Images/1-Storage-Account.png)

1. On the **clusterstorage*9999* | Access Control (IAM)** page, select **Add**, and then select **Add role assignment**:


    ![The **clusterstorage*9999* | Access Control (IAM)** page in the Azure portal. The user has selected **Add role assignment**](../ClouderaMigration/Images/1-Add-Role-Assignment.png)

1. In the **Add role assignment** pane, enter the following settings, and then select **Save**:

    | Field | Value|
    |-|-|
    | Role | Storage Blob Data Owner |
    | Assign access to | User assigned managed identity |
    | Subscription | Select your subscription |
    | Select | Specify the clustermanagedid managed identity in the workshoprg*9999* resource group |

1. Wait while the role is assigned, and then click **Role assignments** to verify that it has been assigned successfully:

    ![The **Role assignments** page in the Azure portal. The **clustermanagedid** identity has been assigned the **Storage BlobData Owner** role in the storage account](../ClouderaMigration/Images/1-Verify-Role-Assignment.png)
