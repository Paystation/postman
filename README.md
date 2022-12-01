## Paystation API Postman collection

This is a postman collection of our [Paystation API](https://docs.paystation.co.nz/api/index.html)

### Requirements

You'll need to supply your own Paystation gateway and oauth credentials, if you don't have these please [contact us](https://www2.paystation.co.nz/contact-us)

Requires the installation of [Postman](https://www.getpostman.com/).

[Postman guide to environment management](https://learning.getpostman.com/docs/postman/environments_and_globals/manage_environments)

### How to import

- Open Postman
- Go to _File_ → _Import_ → _Folder_
- Choose project folder (where you've saved the files `Paystation API.postman_collection.json` and `Paystation Settings.postman_environment.json`)
- Confirm what you want to import (environment and/or collection).

### Environment variables

Add your Paystation ID, Gateway ID and OAuth Credentials in the `Paystation Settings` environment

- PAYSTATION_ID - Test Paystation Account ID - (e.g 600000)
- GATEWAY_ID - Test Paystation Gateway ID - (e.g PAYSTATION)
- OAUTH_CLIENT_ID - OAuth client id
- OAUTH_CLIENT_SECRET - OAuth client secret

### OAuth Authentication

All of the requests inherit a _Pre-request_ script from the parent folder, and this script will add the _Authorization_ header automatically for you.

`2Party`, `3Party` and `Token Management` folder, inherits the Authorization from `Paystation API`. Click on the folder and check the script under _Pre-request_ and the setting under _Authorization_.

`Search & Reporting` folder has it's own _Pre-request_ script because it will only need an OAuth read scope.
