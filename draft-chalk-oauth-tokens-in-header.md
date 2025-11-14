---
title: "OAuth Tokens in HTTP Header"
category: std

docname: draft-chalk-oauth-tokens-in-header-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Web Authorization Protocol"
keyword:
 - HTTP header
 - Authentication-Info
 - inline updates
 - bearer tokens
venue:
  group: "Web Authorization Protocol"
  type: "Working Group"
  mail: "oauth@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/oauth/"
  github: "OllieJC/draft-chalk-oauth-tokens-in-header"
  latest: "https://OllieJC.github.io/draft-chalk-oauth-tokens-in-header/draft-chalk-oauth-tokens-in-header.html"

author:
 -
    fullname: "Ollie Chalk"
    organization: "Government Digital Service, UK"
    email: "ollie.chalk@dsit.gov.uk"

normative:
  RFC6749:

informative:

...

--- abstract

This specification extends OAuth 2.0 {{RFC6749}} by defining a mechanism for resource servers or authorisation servers to convey inline token updates and related metadata to clients using the `Authentication-Info` HTTP header.


--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
