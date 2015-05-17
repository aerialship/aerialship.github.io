---
    title: SamlSpBundle
---


SamlSpBundle implements support for SAML v2.0 Service Provider in Symfony2 by implementing security listener that authenticates against one or more defined Identity Providers in the symfony firewall configuration.

Download source code at Github [SamlSpBundle](https://github.com/aerialship/SamlSpBundle) page.

Included features
-----------------

**Federation Metadata XML**

Each SAML participant declares supported features in the federation metadata xml. SamlSpBundle automatically builds metadata xml that is available on a web route.

**Discovery Service**

If more then one IDP is specified, for SSO login AuthnRequests discovery service route is opened where user can pick IDP. By overriding that twig template you can make your own discovery page.

**AuthnRequest / Single Sign On Login**

The login route builds SAML AuthRequest and sends user to IDP to authenticate

**Assertion Consumer Service**

When user is authenticated on IDP side, it’s sent back to your SP app on the Assertion Consumer Service that reads SAML NamdeID and attributes and logs the user to your application.

**LogoutRequest / Single Logout**

The SamlSpBundle logout route sends LogoutRequest to IDP which calls all other SPs and responds with LogoutResponse, after which receival SamlSpBundle redirects to standard Symfony logout route for the local logout handling.

**Http Post and Http Redirect Bindings**

At the current version SamlSpBundle supports Http Post and Http Redirect bindings.


Installation
------------

To add SamlSpBundle to your project, you would need to add it to your composer.json and after update to your AppKernel. After that you would need to make your own SSO state entity class and it’s ORM mappings, specify that class in the bundle configuration, and update database schema. Finally you should configure symfony security firewall to use SamlSpBundle specifying SAML details, and import the routing.

Detailed installation steps are described in this SamlSpBundle getting started document in the source code.
