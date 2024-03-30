---
link: https://www.keycloak.org
tags:
  - identity
  - SSO
  - opensource
  - app
  - OIDC
  - OAuth
  - CNCF
  - Java
github: https://github.com/keycloak/keycloak
---
Open Source Identity and Access Management

[[CNCF]] project

## Single-Sign On

Users authenticate with Keycloak rather than individual applications. This means that your applications don't have to deal with login forms, authenticating users, and storing users. Once logged-in to Keycloak, users don't have to login again to access a different application.

## Identity Brokering and Social Login

Enabling login with social networks is easy to add through the admin console. It's just a matter of selecting the social network you want to add. No code or changes to your application is required.

Keycloak can also authenticate users with existing OpenID Connect or SAML 2.0 Identity Providers. Again, this is just a matter of configuring the Identity Provider through the admin console.

## User Federation

Keycloak has built-in support to connect to existing LDAP or Active Directory servers. You can also implement your own provider if you have users in other stores, such as a relational database.

## Standard Protocols

Keycloak is based on standard protocols and provides support for OpenID Connect, OAuth 2.0, and SAML.