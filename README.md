# PlugAuth::Client::Tiny::Apache2AuthenHandler [![Build Status](https://secure.travis-ci.org/plicease/PlugAuth-Client-Tiny-Apache2AuthenHandler.png)](http://travis-ci.org/plicease/PlugAuth-Client-Tiny-Apache2AuthenHandler)

Apache authentication handler for PlugAuth

# SYNOPSIS

In your httpd.conf:

    <Location /protected>
      PerlAuthenHandler PlugAuth::Client::Tiny::Apache2AuthenHandler
      AuthType Basic
      AuthName "My Protected Documents"
      Require valid-user
      PerlSetEnv PLUGAUTH_URL http://localhost:3001
    </Location>

# DESCRIPTION

This module provides PlugAuth authentication (via [PlugAuth::Tiny](https://metacpan.org/pod/PlugAuth::Tiny)) for your legacy Apache2
application.

# ENVIRONMENT

## PLUGAUTH\_URL

    PerlSetEnv PLUGAUTH_URL http://localhost:3001

Specifies the URL for the PlugAuth server to authenticate against.

# SEE ALSO

- [PlugAuth::Client::Tiny::Apache2AuthzHandler](https://metacpan.org/pod/PlugAuth::Client::Tiny::Apache2AuthzHandler)

    For authorization.

- [PlugAuth](https://metacpan.org/pod/PlugAuth)

    Server to authenticate against.

- [PlugAuth::Client::Tiny](https://metacpan.org/pod/PlugAuth::Client::Tiny)

    Simplified PlugAuth client.

- [Alien::Apache24](https://github.com/plicease/Alien-Apache24)

    For testing

# AUTHOR

Graham Ollis &lt;plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2015 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
