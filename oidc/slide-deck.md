---
marp: true
theme: uncover
backgroundImage: url('background_white.jpg')
---

![bg](background_white.jpg)

# OpenID Connect

Standard for delegated authentication

---

# Why OIDC?

- Open standard
- Easy to integrate

![bg right fit](undraw_social_thinking_7ule.svg)

---

![bg right fit](undraw_User_flow_re_bvfx.svg)

# How does it work?

Providers and Clients

<!--
Klient: Den applikation som vill logga in en användare/ha information om denna.

Provider: Autentiserar användaren och skickar information om denna till klienten -->

---

### Authentication flows

![bg right width:600px](./implicit_flow.png)

---

### Authentication flows

![bg right width:600px](./code_flow.png)

---

# OIDC at Xenit

- Xenit IDP (eID)
- Azure AD
- Central IDP (HSB)

<!--
På Xenit använder vi OIDC i Xenit IDP eller eID som den även kallas, dvs vår BankID-tjänst

Azure AD använder, bland annat, OIDC när man använder den för att logga in. Detta kan man se bland annat i Portalen.

HSB's Central IDP är en implementation av en Provider, precis som eID.
-->

---

# OCaml OIDC client

![](certified_openid.png)

---

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

# JOSE

#### JavaScript Object Signing and Encryption

- ocaml-jwt
- jwto

Needed more than they provided
JWK is a important missing piece in both

---

# Links

https://openid.net/
OpenID Foundation

https://github.com/ulrikstrid/ocaml-oidc
OpenID Connect for OCaml and Reason

https://github.com/ulrikstrid/reason-jose
JWT, JWE and JWK for native

https://github.com/reason-native-web/morph
