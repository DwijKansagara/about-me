# Security

Report suspected vulnerabilities privately to **kansagara.dwij@gmail.com**.

This is a static, login-free document site. It has no passwords, JWTs, uploads, database client, payments, webhooks, forms, or server-side URL fetching. Static content is rendered without untrusted HTML. The only state-changing request is the shared appreciation control, whose server applies exact-origin validation, request-intent checks, parameterized SQL, durable rate limiting, restricted database privileges, and salted identifiers.

Future features must follow the workspace security baseline before release. In particular, authentication requires server-side authorization and MFA for privileged accounts; uploads require size, type, signature, isolation, and permission checks; webhooks require signed raw-body verification; outbound URL fetching requires SSRF defenses; and client database access requires explicit RLS policies. Do not publish source maps, secrets, default credentials, or sensitive logs.
