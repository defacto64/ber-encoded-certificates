# ber-encoded-certificates
_Some ruminations about BER-encoded (i.e. non DER) certificates._

BER-encoded certificate are rare birds: you can hardly find any examples by Googling... It is commonly believed that all X.509 certificates MUST be DER-encoded, but that's not precisely true. Or rather, it is only true in particular contexts (e.g. within the TLS protocol, as it's required by RFC 8446, and when downloaded from an id-ad-caIssuers URI per [RFC 5280](https://datatracker.ietf.org/doc/html/rfc5280)). In other circumstances, it is okay that an X.509 certificate be BER-encoded, at least in its outermost structure. As to the internal elements, that's another matter and indeed it's considered almost "obvious" that at least the tbsCertificate element be DER-encoded, for good reasons.

