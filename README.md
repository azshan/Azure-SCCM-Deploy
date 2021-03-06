# Azure-SCCM-Deploy
 Deployment Template for SCCM under Student Subscription

---

## Designed for NSCC Students
Derived from - [azure-quickstart-templates](https://github.com/Azure/azure-quickstart-templates/tree/master/sccm-currentbranch)

## Get your Subscription
1. Activate [HERE](https://azure.microsoft.com/en-us/free/students/)
2. Login with your w#@campus.nscc.ca
3. After activating, confirm your subscription.
    - Login to Azure
    - Open Subscriptions
    - confirm subscription name "Azure For Students"
       - ![Verify Subscription](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/subscription.PNG)

---

## Create the Template
1. Copy the json from  [sccm-deploy-template.json](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/sccm-deploy-template.json)
2. Login to Azure
3. Open Templates>Add
4. Assign a name and description
5. Paste in the entire contents of [sccm-deploy-template.json](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/sccm-deploy-template.json)
   - ![Verify Subscription](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/template-create.PNG)
6. Click ok to validate. (if errors... check license)
7. Click Add to create license
---

## Run the Deployment
1. Navigate to templates
2. Click on the new template
3. Click "Deploy"
   - ![Verify Subscription](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/start-deployment.PNG)
4. Create a new resource group
5. Enter a prefix (this will prepend to VM hostnames) i.e. nscctr- will be nscctr-dc01
6. Provide Administrator credentials
7. Do not modify _artifacts or Location
8. Click Purchase!
---

## Check Deployment

1. Navigate to Resource Groups
2. Open your newly created resource group
3. Select Deployments
4. Review the status of your deployment
   - ![Verify Subscription](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/deployment-status.PNG)

---

## Check SCCM Install
Be Patient... this may take hours!
1. Navigate to Home>Resource groups>your-group>nscctr-ps01
2. Connect via RDP
3. Launch file explorer and browse to C:\Windows\Temp\ProvisionScript\PS1.json
4. Check the status of your installation
    - ![Verify Subscription](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/install-status.PNG)
5. Remain patient, until these show "Complete"

## Launch Configuration Manager
1. RDP to PS01
2. Open Configuration Manager Console

---
## Monitor Your Usage!!!
1. Visit [microsoftazuresponsorships.com](https://www.microsoftazuresponsorships.com)
2. Click "Check your Balance"
3. You may want to shut down you VM's when not in use in order to reduce "costs".
4. Expect $13-15 usage for this complete resource group per day. So only run VM's when you need them!

## Shut 'er Down
1. Turn off your VM's when not in use!
2. Navigate to Virtual Machines
3. Click to check each VM
4. Click Stop.
    - ![Stop Virtual Machine](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/stopping.JPG)

## Configure Auto-Shutdown
1. Play it safe and set each VM to shut down automatically.
2. Navigate to Vitrual MAchines and click on a VM to edit.
3. Click Auto-Shutdown and configure.
    - ![Auto Shutdown](https://github.com/redmondmj/Azure-SCCM-Deploy/blob/master/images/auto-stop.JPG)