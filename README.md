Steps to Deploy and Use the whereUsedPlugin in POD Designer:

1. Clone the project from GitHub.

2. (Optional) Modify the namespace if desired, or leave it as is.

3. Download the PPD file and import it into the Design Production Process (password: Rits@123).

4. Build the mta.yaml file.

5. Deploy the mta_archives file to Cloud Foundry.

6. Get Deployment Details
   
    Once deployment is complete:
   
    Copy the deployed application URL from Cloud Foundry.
   
    From index.html, retrieve the plugin path (e.g., /whereUsedPlugin) and namespace (e.g., huka.custom.plugin.whereUsedPlugin) and replace dots(.) with forward slashes(/).

7. Register the Plugin
   
    In the Manage Service Registry application:
   
    Go to the UI Extensions tab.
   
    Create a new UIExtension entry using the url, path and namespace and enable the status from the previous step.

8. Access the Plugin in POD Designer
    
    After registration, the plugin will appear in POD Designer.

9. Deploy and Publish the PPD
    
    Deploy and publish the imported PPD to the Service Registry.
    
    Retrieve the Key Value
    
        After publishing: A URL/path will be generated. Copy only the key value from it.

10. Add Plugin to a Custom POD
    
        Create a custom POD.
    
        Drag and drop the whereUsedPlugin into the plugin container.
    
        Paste the copied key value into the custom_whereUsedPPD field in the property editor.
    
        Save the POD.

11. View the Plugin
    
        Copy the custom POD's URL and open it in a new browser tab.

        The plugin view should now be visible.
    
        Search Inventory: Use the search bar to enter an inventory.
    
        If found, associated SFC details will appear in the results table.
