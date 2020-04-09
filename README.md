## Open From Tableau Server

Interface configuration:

#### Server URL

- The Server URL should begin with `https://` or `http://`
  - Example: `https://tableauserver.mysite.co.uk/`
- For Tableau Online, this should be set to `https://sso.online.tableau.com/`

#### Username

- The username you normally use to log into the Tableau Server

#### Password

- The password you normally use to log into the Tableau Server

#### Site

- The name of the site containing the datasource you want to read. This should be taken from the URL, rather than the dropdown menu on the Tableau Server.
  - Example: `https://tableauserver.mysite.co.uk/#/site/**mysitename**/`
- Leave this box blank for the default folder

#### Datasource

- The name of the datasource you want to read
