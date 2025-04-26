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

# Create a Salesforce DX Project
1. In Visual Studio Code, open the Command Palette by pressing Ctrl+Shift+P (Windows) or Cmd+Shift+P (macOS).
2. Type <small>SFDX</small>.
3. Select SFDX: Create Project.
4. Press Enter to accept the standard option.
5. Enter HelloWorldLightningWebComponent as the project name.
6. Press Enter.
7. Select a folder to store the project.
8. Click Create Project. You should see something like this as your base setup.