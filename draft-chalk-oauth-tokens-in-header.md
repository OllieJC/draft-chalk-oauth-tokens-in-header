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

OAuth deployments vary widely, from simple bearer-only systems to distributed architectures with separate authorisation servers and resource servers.

In some of these environments, a resource server may have enough context to provide updated token information or indicate a more appropriate token for future use.

However, existing OAuth flows require separate interactions with the authorisation server to obtain updated tokens or metadata.

Some deployments may not have an authorisation server at all, yet still benefit from a way to signal preferred or refreshed token state to clients.

This specification introduces a lightweight mechanism for conveying inline token updates using the `Authentication-Info` header originally defined in {{RFC7615}} and now in {{RFC9110}}.

It operates entirely within the existing HTTP response, without modifying the client's request or diverting it into an alternative token retrieval process.

Clients interpret the conveyed values as hints rather than strict directives, maintaining compatibility with current OAuth behaviour.

The result is an optional optimisation that improves efficiency and flexibility across diverse deployment models.


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
