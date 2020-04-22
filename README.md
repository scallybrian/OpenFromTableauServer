## Open From Tableau Server

Interface configuration:

#### Server URL

- The Server URL should begin with `https://` or `http://`
  - Example: `https://tableauserver.mysite.co.uk/`
- For Tableau Online, the server address in the URI must contain the pod name, such as 10az, 10ay, or us-east-1. For example, the URI to sign in to a site in the eu-west-1a pod would be: `https://eu-west-1a.online.tableau.com/`

#### Username

- The username you normally use to log into the Tableau Server

#### Password

- The password you normally use to log into the Tableau Server

#### Site

- The name of the site containing the datasource you want to read. This should be taken from the URL, rather than the dropdown menu on the Tableau Server.
  - Example: `https://tableauserver.mysite.co.uk/#/site/**mysitename**/`
- Leave this box blank for the default folder
- For Tableau Online, this should be the name of the site
  - Example: `https://eu-west-1a.online.tableau.com/#/site/**mysitename**/workbooks`

#### Datasource

- The name of the datasource you want to read

## Important

If your Tableau Server environment uses SAML/SSO authentication, you can perform the workaround described in this video by Jonothan MacDonald to enable use of this tool: https://youtu.be/woNVLSPxWzI
