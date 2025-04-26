# Salesforce LWC Project( Lightning Web Component)

Now that you’ve created a Salesforce DX and LWC project, what’s next? Here are some documentation resources to get you started.

## 📁 Creating a Salesforce DX Project
1. Open **Visual Studio Code**.
2. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS) to open the **Command Palette**.
3. Type and select **`SFDX: Create Project`**.
4. Press **Enter** to accept the **standard** project template.
5. Enter `HelloWorldLightningWebComponent` as the **project name**.
6. Press **Enter**.
7. Choose a folder to store your project files.
8. Click **Create Project**.

## 🔑 Authorizing an Org using Salesforce CLI
1. Open **Visual Studio Code**.
2. Press `Ctrl+Shift+P` (Windows) or `Cmd+Shift+P` (macOS) to open the **Command Palette**.
3. Type **`SFDX`** and select **`SFDX: Authorize an Org`**.
4. Press **Enter** to accept the **Project Default login URL** option.

### Setup need to do on the local system:
### Export the the path of Salesforce cli
```sh
export PATH=~/sfcli/bin:$PATH
PATH=~/sfcli/bin:$PATH
```
### Open the default project in default org of your System:
```sh
sfdx force:auth:web:login --setalias myOrgAlias --instanceurl https://login.salesforce.com --setdefaultusername --dev-debug
```

5. Press **Enter** to accept the **default alias** for the org.
6. A new browser window will open. Log in using your **Saleforce Playground** or **Salesforce Org** credentials.
7. If prompted, click **Allow** to grant access.

## ✨ Creating a Lightning Web Component (LWC)

To create a new Lightning Web Component using Visual Studio Code:
1. Open **Visual Studio Code**.
2. Press `Ctrl+Shift+P` (Windows) or `Cmd+Shift+P` (macOS) to open the **Command Palette**.
3. Type **`SFDX`** and select **`SFDX: Create Lightning Web Component`**.
4. Enter `helloWorld` as the **name** of the new component.
5. Press **Enter** to accept the default directory: `force-app/main/default/lwc`.
6. Press **Enter** again to confirm.
7. View the newly created component files (`helloWorld.js`, `helloWorld.html`, and `helloWorld.js-meta.xml`) inside the `lwc` folder.

## 🧩 Sample LWC: helloWorld.html

In the `helloWorld.html` file, paste the following code:

```html
<template>
    <lightning-card title="HelloWorld" icon-name="custom:custom14">
      <div class="slds-m-around_medium">
        <p>Hello, {greeting}!</p>
        <lightning-input label="Name" value={greeting} onchange={changeHandler}></lightning-input>
      </div>
    </lightning-card>
  </template>
```

## 🧠 Add Logic to helloWorld.js

In the `helloWorld.js` file, paste the following code:

```javascript
import { LightningElement } from 'lwc';
export default class HelloWorld extends LightningElement {
        greeting = 'World';
        changeHandler(event) {
        this.greeting = event.target.value;
        }
}
```

## ⚙️ Configure Component Metadata (helloWorld.js-meta.xml)

In the `helloWorld.js-meta.xml` file, paste the following code:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata" fqn="helloWorld">
    <apiVersion>63.0</apiVersion>
    <isExposed>true</isExposed>
    <targets>
    <target>lightning__AppPage</target>
    <target>lightning__RecordPage</target>
    <target>lightning__HomePage</target>
    </targets>
</LightningComponentBundle>
```

## 🚀 Deploy Your Component to Salesforce

### ✅ Deploy to Your Trailhead Playground

1. In **Visual Studio Code**, navigate to `force-app/main`.
2. **Right-click** the `default` folder and select **SFDX: Deploy Source to Org**.
3. Check the **Output** tab in the terminal to confirm successful deployment.
   - You should see a message like: `Deployed Source` listing the `.html`, `.js`, and `.xml` files.

---

## 📲 Add Component to a Lightning App Page

### Step-by-step in Lightning Experience:

1. Open the **Command Palette** (`Ctrl+Shift+P` / `Cmd+Shift+P`) in VS Code.
2. Select **SFDX: Open Default Org** — this will launch your org in a browser.
3. In Salesforce, click on **Setup (⚙️)**, then choose **Setup**.
4. In the **Quick Find** box, type **Home** and select **Home** under **Feature Settings**.
5. For **Advanced Seller Home**, toggle the setting to **Inactive**.
6. From the **App Launcher (grid icon)**, find and open **Sales**.
7. Click on **Setup (⚙️)** again and choose **Edit Page**.
8. In the **Lightning App Builder**, find the `helloWorld` component under **Custom** components.
9. **Drag & drop** the `helloWorld` component to the top of the **Page Canvas**.
10. Click **Save**.
11. Click **Activate** → choose **Assign as Org Default**.
12. Click **Save** → then **Save** again → then **Back** to return to the page.
13. **Refresh the page** — your component should now be visible!


  

