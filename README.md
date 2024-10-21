# AWS_WAF_Block_Rule_Token_User
AWS_WAF_Block_Rule_Token_User

**Regular rule (AWS WAF) Token Bearer**
- Field to match: Single header (authorization)
- Positional constraint: Exactly matches string
- Search string: Bearer

**Regular rule (AWS WAF) URI path (Regular expression)**
- Field to match: URI path
- Regular Expression: (api\/v2\/auth|api\/v1\/login|api\/version)

**Regular rule (AWS WAF) URI path**
- Field to match: URI path
- Positional constraint: Exactly matches string
- Search string: /api/v1/login

**Regular rule (AWS WAF) User in body**
- Field to match: Body
- Positional constraint: Exactly matches string
- Search string: user
- Oversize handling: No match - Treat the web request as not matching the rule statement
