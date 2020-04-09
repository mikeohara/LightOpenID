# LightOpenID

Lightweight PHP library for easy OpenID authentication.

* `Version....:` [**1.3.4** :arrow_double_down:][1]
                 ( *see [the change log][2] for details* )
* `Released on:` April 09, 2020
* `Source code:` [Official GitHub Repo :octocat:][3]
* `Homepage...:` https://github.com/Satariall/LightOpenID
* `Authors....:` [Mewp][4], [iignatov][5], [Satariall][3]

[1]: https://github.com/iignatov/LightOpenID/archive/master.zip
[2]: https://github.com/iignatov/LightOpenID/blob/master/CHANGELOG.md
[3]: https://github.com/Satariall/LightOpenID
[4]: https://github.com/Mewp
[5]: https://github.com/iignatov/LightOpenID

## Quick start

### Add to composer.json

```bash
composer require satariall/lightopenid
```

### Sign-on with OpenID in just 2 steps:
  
  1. Authentication with the provider:

     ```php
     $openid = new LightOpenID('my-host.example.org');
     
     $openid->identity = 'ID supplied by user';
     
     header('Location: ' . $openid->authUrl());
     ```
  2. Verification:

     ```php
     $openid = new LightOpenID('my-host.example.org');
     
     if ($openid->mode) {
       echo $openid->validate() ? 'Logged in.' : 'Failed!';
     }
     ```

### Support for AX and SREG extensions:
  
  To use the AX and SREG extensions, specify `$openid->required` and/or `$openid->optional` 
  before calling `$openid->authUrl()`. These are arrays, with values being AX schema paths 
  (the 'path' part of the URL). For example:

  ```php
  $openid->required = array('namePerson/friendly', 'contact/email');
  $openid->optional = array('namePerson/first');
  ```

  Note that if the server supports only SREG or OpenID 1.1, these are automaticaly mapped 
  to SREG names. To get the values use:

  ```php  
  $openid->getAttributes();
  ```

  For more information see [USAGE.md](https://github.com/Satariall/LightOpenID/blob/master/USAGE.md).


## Requirements

This library requires PHP >= 7.0 with cURL or HTTP/HTTPS stream wrappers enabled.


## Features

* Easy to use - you can code a functional client in less than ten lines of code.
* Uses cURL if avaiable, PHP-streams otherwise.
* Supports both OpenID 1.1 and 2.0.
* Supports Yadis discovery.
* Supports only stateless/dumb protocol.
* Works with PHP >= 7.
* Generates no errors with `error_reporting(E_ALL | E_STRICT)`.


## Links

* [JavaScript OpenID Selector](http://code.google.com/p/openid-selector/) -
  simple user interface that can be used with LightOpenID.
* [HybridAuth](http://hybridauth.sourceforge.net/) -
  easy to install and use social sign on PHP library, which uses LightOpenID.
* [OpenID Dev Specifications](http://openid.net/developers/specs/) -
  documentation for the OpenID extensions and related topics.


## License

[LightOpenID](https://github.com/Satariall/LightOpenID)
is an open source software available under the
[MIT License](http://opensource.org/licenses/mit-license.php).
