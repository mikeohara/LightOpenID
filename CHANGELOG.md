# LightOpenID Change Log

## v1.3.4 (April 20, 2020)
`add` Added supporting for custom AX schema domains.
`add` Tag bump for packagist.org with an auto-update webhook installed.
`fix` Change README.md, USAGE.md and CHANGELOG.md to the latest updates.

## v1.3.3 (April 6, 2020)
`fix` Remove deprecated gmp functions.
`fix` Improve set_realm method to use modern way to build uri.
`fix` Add `CURLOPT_SSL_VERIFYHOST` option to curl for make verify_peer option workable.
`fix` Removed deprecated function `get_magic_quotes_gpc` using.

## v1.3.2 (April 3, 2020)
`fix` Change $identity and $claimed_id variables to public property.

## v1.3.1 (March 04, 2016)

`fix` Fixed an incorrect function call to get_provider_name().  

## v1.3.0 (February 20, 2016)

`fix` Fixed a probable endless redirection.  
`add` Added support for IBM WSSC (a WebSphere product that acts as a reverse proxy).  
`add` Added cURL timeouts for OpenID.  

## v1.2.0 (January 14, 2014)

`fix` Yahoo OpenID not working on newer versions of PHP/cURL.  
`fix` A warning when the realm is shorter than 8 chars.  
`fix` Use cURL when 'allow_url_fopen' is disabled.  
`fix` Different POST-behavior when using cURL and streams.  
`fix` Avoid hiding the real presence/absence of fields.  
`add` Added User-Agent header for better compatibility.  
`add` Added 'text/html' to the discovery content-types.  
`add` Added support for Composer (dependency manager).  
`add` Added ability to set the 'CN_match' SSL option.  


## v1.1.2 (January 15, 2013)

`fix` Fixed a bug in the proxy configuration.  


## v1.1.1 (December 21, 2012)

`add` Added support for overriding the initial URL XRDS lookup.  


## v1.1.0 (December 02, 2012)

`add` Added support for connecting through a proxy.  
`add` Added support for an OpenID+OAuth hybrid protocol.  
`add` Added SSL-validation support for HEAD-requests.  
`fix` Fixed a bug in the attribute exchange implementation.  
`fix` Fixed a bug in stream defaults after a HEAD request.  


## v1.0.0 (June 08, 2012)
`fix` Fixed a bug causing validation failure when using streams.
