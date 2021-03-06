# Classic-API-Postman-Collection

## Overview
This collection is provided to assist Jamf Pro users of the Classic API. It provides a quick method to interact with all non-deprecated endpoints.

This article describes the recommended Postman configuration and setup process to import the collection, configure variables to connect it to your Jamf Pro environment and begin testing API calls and interacting with your Jamf Pro environment via the Classic API.

The following expectations were used when designing this collection:
* All POST operations include a pre-populated request body.
  - This request body may not include all fields supported by the body of the given object, however it will include those required to successfully create the object.
  - Pull requests or issue submissions are encouraged to enhance or update this data.
* All GET operations include at least one example response.
  - Endpoints that have conditional inputs in the form of parameters or request bodies should include multiple examples (e.g. `computercommmands` and `mobiledevicecommands`).
* All query parameters that have a defined list of acceptable values denote the allowed values in the description of the parameter.

## Import the Collection
Use the following options to import the collection into Postman:
* Click the [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/3f5cc9fc4978cdae78fc) button to automatically import the collection into your Postman app.
* In Postman, click File >> Import.
  - Download the JSON included in this repo and select the .json file.

## Define Environment Variables
This collection utilizes the following variables which should be defined within one of the scopes in Postman. Jamf recommends using environments instead of global or collection variables simply for the ease of use and potential for defining different Jamf Pro environments or users. Follow Postman's documentation to [Manage Environments](https://learning.getpostman.com/docs/postman/environments_and_globals/manage_environments).

| Variable     | Description                                     | Example                   |
|--------------|-------------------------------------------------|---------------------------|
| {{url}}      | Hostname and port of the Jamf Pro environment   | company.jamfcloud.com:443 |
| {{username}} | Username to authenticate to Jamf Pro with       | administrator             |
| {{password}} | Password of the user authenticating to Jamf Pro | pa$$word                  |

## Getting Started
After the collection has been imported and valid values have been defined for the variables, all calls should be supported with minimal input required. Additional data will be required either in the form of a parameter value and/or a request body.
