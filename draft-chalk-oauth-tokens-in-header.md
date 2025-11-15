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
  RFC7615:
  RFC9110:

informative:

...

--- abstract

This specification extends OAuth 2.0 {{RFC6749}} by defining a mechanism for resource servers or authorisation servers to convey inline token updates and related metadata to clients using the `Authentication-Info` HTTP header.


--- middle

# Introduction

OAuth deployments range from simple bearer‑only configurations to complex ecosystems with distinct authorisation and resource servers. In some scenarios a resource server holds enough contextual information to advise the client of a refreshed or more suitable token for future use. Existing OAuth flows, however, obligate the client to perform a separate interaction with the authorisation server to obtain such updates, and certain deployments may lack an authorisation server altogether.

This document defines a lightweight mechanism that leverages the `Authentication‑Info` header (originally specified in {{RFC7615}} and incorporated into {{RFC9110}}) to convey inline token updates and associated metadata within a normal HTTP response. The header can be processed transparently by HTTP implementations, potentially even at a proxy or edge service, and does not alter the client's request semantics. Recipients treat the conveyed values as hints - they may adopt the suggested token but are not required to do so - thereby preserving compatibility with existing OAuth behaviour while offering an optional optimisation for efficiency and flexibility.


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
