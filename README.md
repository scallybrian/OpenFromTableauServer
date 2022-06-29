# Open From Tableau Server

This tool will read a published Tableau hyper extract from Tableau Server/Tableau Online into Alteryx Designer. The tool requires Alteryx Designer 2020.2 or later, and Tableau Server 2018.1 or later.

The tool is a packaged Alteryx tool installer (.yxi) file. Double clicking this file will open Alteryx Designer and prompt you to install the tool. Once installed, the tool will appear in the "Connectors" tool pane.

# Important
This tool makes use of the Python library *tableauhyperio*. In order for the tool to run correctly, it must first be run as Administrator so that the library can be installed. It can be run by non-Admin at any time after the initial run.

# Interface configuration:

#### API Version

- The version of the Tableau Server REST API to use. This must be compatible with your Tableau Server version. For more information see `https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_concepts_versions.htm`

#### Server URL

- The Server URL should begin with `https://` or `http://`
  - Example: `https://tableauserver.mysite.co.uk/`
- For Tableau Online, the server address in the URI must contain the pod name, such as 10az, 10ay, or us-east-1. For example, the URI to sign in to a site in the eu-west-1a pod would be: `https://eu-west-1a.online.tableau.com/`

#### Site

- The name of the site containing the datasource you want to read. This should be taken from the URL, rather than the dropdown menu on the Tableau Server.
  - Example: `https://tableauserver.mysite.co.uk/#/site/**mysitename**/`
- Leave this box blank for the *default* site
- For Tableau Online, this should be the name of the site
  - Example: `https://eu-west-1a.online.tableau.com/#/site/**mysitename**/workbooks`

#### Datasource

- The name of the datasource you want to open

## PAT Authentication

To use a Personal Access Token (PAT) for authentication, fill out the fields below. PAT tokens can be generated only once - if you misplace the PAT secret value, you will need to generate another token.

#### PAT Name

- The name given to the PAT token generated on Tableau Server/Online

#### PAT Secret

- The secret value of the PAT token generated on Tableau Server/Online

## Username/Password Authentication

To use username/password authentication, fill out the fields below. PAT authentication is preferable to username/password authentication, as it prevents user passwords from being stored in Alteryx workflows. If MFA is enabled on the Tableau platform, PAT authentication is the only viable authentication method.

#### Username

- The username you normally use to log into Tableau Server/Online

#### Password

- The password you normally use to log into Tableau Server/Online
