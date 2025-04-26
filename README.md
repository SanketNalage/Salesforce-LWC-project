# Salesforce LWC Project( Lightning Web Component)

Now that you’ve created a Salesforce DX and LWC project, what’s next? Here are some documentation resources to get you started.


# Setup need to do on the local system:
## Export the the path of Salesforce cli
```sh
export PATH=~/sfcli/bin:$PATH
PATH=~/sfcli/bin:$PATH
```

## Open the default project in default org of your System:
```sh
sfdx force:auth:web:login --setalias myOrgAlias --instanceurl https://login.salesforce.com --setdefaultusername --dev-debug
```
## 📁 Creating a Salesforce DX Project
1. Open **Visual Studio Code**.
2. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS) to open the **Command Palette**.
3. Type and select **`SFDX: Create Project`**.
4. Press **Enter** to accept the **standard** project template.
5. Enter `HelloWorldLightningWebComponent` as the **project name**.
6. Press **Enter**.
7. Choose a folder to store your project files.
8. Click **Create Project**.