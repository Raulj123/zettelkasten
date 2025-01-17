
## What it is?
Single Sign-On (SSO) is an ==authentication process== in which a ==user is provided access to multiple applications or websites by using only a single set of login credentials.== This prevents the need for the user to log separately into the different applications.

==Identity Provider== 
* user credentials and other identifying information are stored and managed by a centralized system
* The Identity Provider authenticates the user and provides access to the service provider.
==Service Provider==
*  provides services to the end-user. They rely on identity providers to assert the identity of a user, and typically certain attributes about the user are managed by the identity provider
==Identity Broker==
*  intermediary that connects multiple service providers with various different identity providers

Two common protocols for this authentication process:
* SAML(Security assertion markup language)
	* XML-based open standard for exchanging identity information between services 
* OpenID Connect
	* JWT (JSON web token) to share identity information between services

# How it works
1. The user requests a resource from their desired application.
2. The application redirects the user to the Identity Provider (IdP) for authentication.
3. The user signs in with their credentials (usually, username and password).
4. Identity Provider (IdP) sends a Single Sign-On response back to the client application.
5. The application grants access to the user

# SAML vs OAuth 2.0 and OpenID Connect (OIDC)
 * SAML
	 * uses XML to pass messages 
	 * geared towards enterprise 
	 * session cookie in a browser that allows users to access certain web pages, great for short-lived workloads
* OAuth/OIDC
	* use JSON to pass messages
	* simpler experience 
	* RESTful communication

# Examples 
common used IdP
* Okta
* Google
* Auth0
* OneLogin