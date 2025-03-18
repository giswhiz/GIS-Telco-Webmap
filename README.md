# GIS-Telco-Webmap

The result of the work is the published webmap “aktualisierte_Kommunen.html” 
This guide describes how to use the automated workflow and update the telecommunication application areas on the web map directly from the database, and it ensures that all stakeholders have consistent access to the data and scripts.
Alteryx Workflow is located in: Z:\General - Telco_Database\TKU_Web_Map\Alteryx_Workflow
![image](https://github.com/user-attachments/assets/c5dcba4c-0f68-4e2e-a230-605dd71cd030)
****

Steps to use the automated workflow in Alteryx. 

**1. Setting up a dynamic storage location:
To ensure versioned and accessible data storage for everyone, use a dynamic local path that accesses your shared SharePoint via OneDrive. To do this, follow these steps:
a. Folder link: Link the folder containing the VBA automations (e.g., "01_VBA_Automatizations") to your OneDrive. Changes will then be automatically synchronized with your SharePoint.
b. Creating a virtual drive: To simplify access to the OneDrive folder, create a virtual drive:
1. Right-click on "This PC" in Windows Explorer.
2. Select "Map Network Drive".
3. In the "Folder" field, enter the following text: \localhost\c$\Users%USERNAME%\OneDrive.
4. Replace "%USERNAME%" with your employee number (found under Windows Settings -> Accounts -> Your info; begins with "DExxx").
5. Confirm your entry. Windows will now create a virtual drive (e.g., "Z:") that accesses your shared OneDrive folders.
c. Adjust the file path: Adjust the file path of the data source in the Excel file. To do this, navigate to your OneDrive via the newly created virtual drive, select the relevant subfolder, and select the data source (example: "Z:\01_VBA_Automatisierungen\04_PV_WFP_Infra MAoZN\Input").
2. Setting up quick access to the TKU web map files:
a. In Microsoft Teams, navigate to the relevant team and then to the "Telco_Database -> General" folder.
b. Right-click on the "General" folder and select "Add Shortcut to OneDrive."
c. In File Explorer, you will now find a shortcut to the "General" folder under "OneDrive." This will take you directly to the TKU web map files. The path should look like this: "Z:\General - Telco_Database\TKU_Web_Map."

3. Updating the web map:
Before execution:
• Ensure that there is a connection to the storage location on the virtual drive.
• For archiving purposes, move the old JavaScript files in the "data" folder to a new folder with the current date within the "data" folder.
Workflow in Alteryx:
• In the Python script, ensure that the storage location in the path is correctly assigned.
• The JavaScript files with the administrative boundaries are located in the "data/boundaries" folder. Add new boundaries as needed.
After execution:
• Check the updated web map for functionality and accuracy.
• Move the old HTML file to the "Archive" folder. ![image](https://github.com/user-attachments/assets/41787ddd-da81-4107-bf13-ea57f651492d)

**
****
