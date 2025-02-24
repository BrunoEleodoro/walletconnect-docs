# Invite Keys

Invite keys are used by Chat API for public blockchain account resolution.

When we are registering a chat invite key we must use the following mandatory fields in the jwt:

* iat - timestamp when jwt was issued 
* exp - timestamp when jwt must expire
* iss - public identity key in form of did:key according to the [Ed25519](https://w3c-ccg.github.io/did-method-key/#ed25519-x25519)
* sub - public key for chat invite key in form of did:key according to the [X25519](https://w3c-ccg.github.io/did-method-key/#x25519)
* aud - key server url used for registering
* pkh - corresponding blockchain account (did:pkh)

Expiry will be calculated 1 hour (3600 seconds) from issued date
