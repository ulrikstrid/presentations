---
marp: true
theme: uncover
class: invert
---

# OpenID Connect

## OCaml and ReasonML native

---

<!--
class: uncover
-->

![bg](background_white.jpg)

# Ulrik Strid

@ulrikstrid - Github, Twitter and Discord

DevOps @ Xenit AB
Building OIDC providers and other fun stuff

-

We're hiring!

---

<!--
class: invert
-->

# Why OIDC?

Open standard
easy to integrate

![bg right fit](undraw_social_thinking_7ule.svg)

---

<!--
class: uncover
-->

![bg right fit](undraw_User_flow_re_bvfx.svg)

# How does it work?

Providers and Clients

---

<!--
class: uncover
-->

### Authentication flows

![bg right width:600px](./implicit_flow.png)

---

<!--
class: uncover
-->

### Authentication flows

![bg right width:600px](./code_flow.png)

---

<!--
class: invert
-->

# Didn't you say OCaml?

---

<!--
class: uncover
-->

# OCaml OIDC client

![](certified_openid.png)

---

<!--
class: invert
-->

![bg left width:600px](undraw_certification_aif8.svg)

# Certification process

Build your library

Setup e2e tests

Complete all tests

Send results

---

![bg right width:600px](undraw_secure_login_pdn4.svg)

# So what?

It **should** work with any implementation

(that follows the standard)

---

<!--
class: uncover
-->

# My road to a certified library

---

<!--
class: invert
-->

![bg left width:600px](undraw_source_code_xx2e.svg)

# What was there?

- Mirage crypto (formerly Nocrypto)
- Uri, Base64, yojson ... etc
- Hype around Httpaf

---

<!--
class: uncover
-->

![bg right width:600px](undraw_page_not_found_su7k.svg)

# What was not?

- No solid JWT/JWK implementation
- No nice (for me) web story
  - Cohttp was "slow"
  - No cookie solution

---

<!--
class: invert
-->

# JOSE

#### JavaScript Object Signing and Encryption

- ocaml-jwt
- jwto

Needed more than they provided
JWK is a important missing piece in both

---

# ocaml-cookie

I got tired of doing cookies ad-hoc

-

Test suite with 100 or so tests
from IETF's http-state working group

---

# Morph

A web framework

Grew out of me trying to build a OIDC Provider

---

<!--
class: uncover
-->

# Lowering my goals

**Client** instead of a _Provider_

Slightly easier (less state)

More usefull for others

Not as cool

---

<!--
class: invert
-->

# Thanks

# Antonio Monteiro

(Well maintained) Httpaf fork

H2 - http2 implementation

Piaf - Superb http client (and server)

A lot of feedback and pushing

---

# Demo time!

---

<!--
class: uncover
-->

![bg right width:600px](undraw_Questions_re_1fy7.svg)

# Questions?

---

<!--
class: invert
-->

# Links

https://openid.net/
OpenID Foundation

https://github.com/ulrikstrid/ocaml-oidc
OpenID Connect for OCaml and Reason

https://github.com/ulrikstrid/reason-jose
JWT, JWE and JWK for native

https://github.com/reason-native-web/morph
