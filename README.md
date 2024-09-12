# OCI OKE Cluster quickstart

To Deploy a OKE Cluster ( VCN-native pod networking for OKE CNI ) as a new Dev Platform, follow next steps:

1 Click the 'Next' button

[![Open in Code Editor](https://raw.githubusercontent.com/oracle-devrel/oci-code-editor-samples/main/images/open-in-code-editor.png)](https://cloud.oracle.com/?region=home&cs_repo_url=https://github.com/paolajuarezgomez/oke_cluster.git&cs_branch=main&cs_readme_path=INIT.md&cs_open_ce=false)

2. Cloud shell will be open. Change the **KEYS values** for the respective **OCIDs** in oke_cluster/oke/oke.tf file 

  * **vcn_id**="\<CMP-PLATFORM-DEV-KEY>"

  * **network_compartment_id** = "\<CMP-LZP-D-NETWORK-KEY>"

  * **subnets** = {
  cp       = { id = "\<SN-DEV-CP-KEY>" }
  int_lb   = { id = "\<SN-DEV-PRIV-LB-KEY>" }
  workers  = { id = "\<SN-DEV-WORKERS-KEY>" }
  pods     = { id = "\<SN-DEV-PODS-KEY>"}
  }

  * **nsgs** = {
  cp       = { id = "\<NSG-DEV-CP-KEY>" }
  int_lb   = { id = "\<NSG-DEV-PRIV-LB-KEY>" }
  workers  = { id = "\<NSG-DEV-WORKERS-KEY>" }
  pods     = { id = "\<NSG-DEV-PODS-KEY>" }
  }

> [!NOTE]
> Make any additional changes needed to customize your cluster. If you have any questions, please refer to the documentation.

3. run **chmod +x init.sh**
4. run **./init.sh -c compartment_ocid**


