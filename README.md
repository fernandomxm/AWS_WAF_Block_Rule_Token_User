# AWS_WAF_Block_Rule_Token_User
AWS_WAF_Block_Rule_Token_User

**Regular rule (AWS WAF) Token Bearer**
- Field to match: Single header (authorization)
- Positional constraint: Exactly matches string
- Search string: Bearer
- Action: Block
- Custom response code: 401
- Custom response body: block_token_invalid
{
  "status": 401,
  "error": "Token Invalido",
  "message": "Token Invalido"
}

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
- Action: Block
- Custom response code: 401
- Custom response body: usuario_incorreto
{
  "status": 401,
  "error": "Não autorizado",
  "message": "Usuário incorreto"
}
