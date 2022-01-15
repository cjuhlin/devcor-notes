# OAuth2

## Resource owner

The end user.

## Clients

Is often the application that is requesting access on the behalf of the [resource owner](OAuth2.md#resource-owner). 

### Confidential Client

Like web-application,  is more safer to store the client_key and client_secret

### Public Clients

Like Mobile phone , webbrowser.  They can't be trusted with the secret , easier to hijack the client secrets.

## Authorization server

The server that handle the authorization 

## Two-legged authorization

More likely to be used by machine to machine. The flow is only between the [ authorization server](OAuth2.md#authorization-server) and the [client](OAuth2.md#clients)  without the [resource owner](OAuth2.md#resource-owner).

### Grant types

### Client credentials

"The Client Credentials grant type is used by clients to obtain an access token outside of the context of a user.

This is typically used by clients to access resources about themselves rather than to access a user's resources."

### Resource Owner Credential

Providing username and password for the resource owner

### Implicit

## Three-legged authorization

Use All three blocks :

[Resource owner](OAuth2.md#resource-owner) 

[Clients](OAuth2.md#clients)

[Authorization server](OAuth2.md#authorization-server)

### Grant types

#### Authorization code

"The Authorization Code grant type is used by confidential and public clients to exchange an authorization code for an access token.

After the user returns to the client via the redirect URL, the application will get the authorization code from the URL and use it to request an access token."

# Resource

https://oauth.net/2/grant-types/
