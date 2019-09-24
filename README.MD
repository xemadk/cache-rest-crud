# Cache Object Script REST API

## Configuration Steps
* Creat Web Application
    - Name = Ruta base del servicio '/csp/conn/rest'
    - Select Namespace 'CONN'
    - Enabled: Application, CSP/ZEN, Inbound Web Service
    - Security; Unauthenticated, Password, Delegated
    - Dispatch: rest.Router
	- Set session cookie path value to a specific value to share cookies between applications.

* CACHE Session consumption
    - Add ZAUTHENTICATE.mac routine to %SYS namespace
    - This Routine implements the method GetCredentials that redirects the authentication to the main Router "rest.Router->AuthenticateCSP"

## Cars Router - Crud
The Cars router crud exposes a basic crud. With the next methods:
* GetList
* Get
* Create
* Update
* Delete

## Example Router
This example router is created to show different examples with Cache and REST services.
