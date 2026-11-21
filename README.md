# Awesome Hono

A curated catalog of **[Hono](https://hono.dev/)** — the small, ultrafast web framework built on **Web Standards** (works on Cloudflare Workers, Deno, Bun, Node, Lambda, and friends).

Inspired by how [public-apis](https://github.com/public-apis/public-apis) organizes free APIs: short rows, honest columns, links that work. **Not** a scrape of [kuzhi1900/awesome-hono](https://github.com/kuzhi1900/awesome-hono) or any other list. Every blurb here is original.

PRs welcome: one link + 1–2 sentences you wrote. No star-farming.

## Index

- [Official](#official)
- [Runtimes / adapters](#runtimes--adapters)
- [Middleware & plugins](#middleware--plugins)
- [Auth / JWT / sessions](#auth--jwt--sessions)
- [Validators](#validators)
- [Examples & starters](#examples--starters)
- [Related ecosystem](#related-ecosystem)
- [Contributing](#contributing)

## Official

| Link | Notes |
|------|--------|
| [hono.dev](https://hono.dev/) | Home — flame-fast Web Standards framework |
| [Docs](https://hono.dev/docs/) | Getting started, guides, middleware, API reference |
| [honojs/hono](https://github.com/honojs/hono) | Core source; zero deps; hono/tiny preset |
| [npm: hono](https://www.npmjs.com/package/hono) | Install for Node / Bun / bundlers |
| [JSR: @hono/hono](https://jsr.io/@hono/hono) | First-class Deno / JSR publish |
| [create-hono](https://github.com/honojs/create-hono) | CLI scaffolds |
| [Discord](https://discord.gg/KMh2eNSdxV) | Official community |
| [@honojs on X](https://x.com/honojs) | Release notes and tips |

## Runtimes / adapters

Same app code; pick the getting-started guide for your edge or server.

| Link | Notes |
|------|--------|
| [Cloudflare Workers](https://hono.dev/docs/getting-started/cloudflare-workers) | Wrangler + Workers; first-class edge target |
| [Cloudflare Pages](https://hono.dev/docs/getting-started/cloudflare-pages) | Pages Functions entry |
| [Deno](https://hono.dev/docs/getting-started/deno) | Native Web APIs; JSR-friendly |
| [Bun](https://hono.dev/docs/getting-started/bun) | Hot reload via bun --hot; hono/bun static |
| [Node.js](https://hono.dev/docs/getting-started/nodejs) | Needs adapter; see @hono/node-server |
| [@hono/node-server](https://github.com/honojs/node-server) | Official Node HTTP server adapter |
| [AWS Lambda](https://hono.dev/docs/getting-started/aws-lambda) | hono/aws-lambda handler wrap |
| [Lambda@Edge](https://hono.dev/docs/getting-started/lambda-edge) | CloudFront edge functions |
| [Vercel](https://hono.dev/docs/getting-started/vercel) | Zero-config Hono on Vercel |
| [Netlify](https://hono.dev/docs/getting-started/netlify) | Netlify Functions / Edge |
| [Fastly Compute](https://hono.dev/docs/getting-started/fastly) | Fastly Compute at Edge |
| [Azure Functions](https://hono.dev/docs/getting-started/azure-functions) | Azure Functions host |
| [Supabase Edge Functions](https://hono.dev/docs/getting-started/supabase-functions) | Deno-based Supabase edge |
| [Google Cloud Run](https://hono.dev/docs/getting-started/google-cloud-run) | Containerized Node/Bun deploy |
| [Service Worker](https://hono.dev/docs/getting-started/service-worker) | Browser / SW fetch handler |

## Middleware & plugins

Built-ins ship in `hono/*`. Third-party packages live under `@hono/*` in the middleware monorepo.

| Link | Notes |
|------|--------|
| [Middleware guide](https://hono.dev/docs/guides/middleware) | How onion-style middleware composes |
| [Third-party index](https://hono.dev/docs/middleware/third-party) | Docs map of official @hono packages |
| [honojs/middleware](https://github.com/honojs/middleware) | Monorepo for validators, auth wrappers, Sentry, etc. |
| [CORS](https://hono.dev/docs/middleware/builtin/cors) | Cross-origin headers |
| [Logger](https://hono.dev/docs/middleware/builtin/logger) | Request logging |
| [Secure Headers](https://hono.dev/docs/middleware/builtin/secure-headers) | Helmet-style security headers |
| [CSRF](https://hono.dev/docs/middleware/builtin/csrf) | Cross-site request forgery guard |
| [Compress](https://hono.dev/docs/middleware/builtin/compress) | Response compression |
| [ETag](https://hono.dev/docs/middleware/builtin/etag) | Conditional GET / caching helper |
| [Cache](https://hono.dev/docs/middleware/builtin/cache) | Cache API middleware |
| [Body Limit](https://hono.dev/docs/middleware/builtin/body-limit) | Cap request body size |
| [Timeout](https://hono.dev/docs/middleware/builtin/timeout) | Abort slow handlers |
| [Request ID](https://hono.dev/docs/middleware/builtin/request-id) | Correlate logs per request |
| [Pretty JSON](https://hono.dev/docs/middleware/builtin/pretty-json) | Human-readable JSON responses |
| [Trailing Slash](https://hono.dev/docs/middleware/builtin/trailing-slash) | Normalize path vs path/ |
| [@hono/trpc-server](https://github.com/honojs/middleware/tree/main/packages/trpc-server) | Mount a tRPC server on Hono |
| [@hono/graphql-server](https://github.com/honojs/middleware/tree/main/packages/graphql-server) | GraphQL HTTP handler |
| [@hono/swagger-ui](https://github.com/honojs/middleware/tree/main/packages/swagger-ui) | Serve Swagger UI for OpenAPI |
| [@hono/sentry](https://github.com/honojs/middleware/tree/main/packages/sentry) | Sentry error reporting |
| [@hono/otel](https://github.com/honojs/middleware/tree/main/packages/otel) | OpenTelemetry instrumentation |
| [@hono/prometheus](https://github.com/honojs/middleware/tree/main/packages/prometheus) | Prometheus metrics endpoint |
| [@hono/mcp](https://github.com/honojs/middleware/tree/main/packages/mcp) | Model Context Protocol server glue |
| [@hono/casbin](https://github.com/honojs/middleware/tree/main/packages/casbin) | Casbin RBAC / ABAC |
| [@hono/node-ws](https://github.com/honojs/middleware/tree/main/packages/node-ws) | WebSocket helper for Node |

## Auth / JWT / sessions

| Link | Notes |
|------|--------|
| [JWT](https://hono.dev/docs/middleware/builtin/jwt) | Verify / sign JWTs in middleware |
| [Basic Auth](https://hono.dev/docs/middleware/builtin/basic-auth) | HTTP Basic |
| [Bearer Auth](https://hono.dev/docs/middleware/builtin/bearer-auth) | Authorization Bearer tokens |
| [@hono/session](https://github.com/honojs/middleware/tree/main/packages/session) | Encrypted cookie / storage sessions via jose |
| [@hono/oidc-auth](https://github.com/honojs/middleware/tree/main/packages/oidc-auth) | OpenID Connect middleware |
| [@hono/oauth-providers](https://github.com/honojs/middleware/tree/main/packages/oauth-providers) | OAuth provider helpers |
| [@hono/clerk-auth](https://github.com/honojs/middleware/tree/main/packages/clerk-auth) | Clerk session verification |
| [@hono/firebase-auth](https://github.com/honojs/middleware/tree/main/packages/firebase-auth) | Firebase Auth token check |
| [@hono/auth-js](https://github.com/honojs/middleware/tree/main/packages/auth-js) | Auth.js NextAuth-style adapter |
| [@hono/stytch-auth](https://github.com/honojs/middleware/tree/main/packages/stytch-auth) | Stytch auth middleware |
| [@hono/cloudflare-access](https://github.com/honojs/middleware/tree/main/packages/cloudflare-access) | Cloudflare Access JWT gate |
| [Better Auth x Hono](https://better-auth.com/docs/integrations/hono) | Mount Better Auth on Web Standards Request |
| [Better Auth on Cloudflare](https://hono.dev/examples/better-auth-on-cloudflare) | Official Hono example walkthrough |
| [jcs224/hono_sessions](https://github.com/jcs224/hono_sessions) | Community cookie sessions + flash + stores |

## Validators

Prefer the Validation guide + a schema library that fits your stack. Official `@hono/*-validator` packages feed `c.req.valid(...)`.

| Link | Notes |
|------|--------|
| [Validation guide](https://hono.dev/docs/guides/validation) | Built-in validator + third-party schema libs |
| [@hono/zod-validator](https://github.com/honojs/middleware/tree/main/packages/zod-validator) | Zod to typed c.req.valid |
| [@hono/zod-openapi](https://github.com/honojs/middleware/tree/main/packages/zod-openapi) | Zod schemas to OpenAPI routes |
| [@hono/valibot-validator](https://github.com/honojs/middleware/tree/main/packages/valibot-validator) | Valibot schemas |
| [@hono/standard-validator](https://github.com/honojs/middleware/tree/main/packages/standard-validator) | Any Standard Schema library |
| [@hono/arktype-validator](https://github.com/honojs/middleware/tree/main/packages/arktype-validator) | ArkType |
| [@hono/typebox-validator](https://github.com/honojs/middleware/tree/main/packages/typebox-validator) | TypeBox / JSON Schema |
| [@hono/typia-validator](https://github.com/honojs/middleware/tree/main/packages/typia-validator) | Typia |
| [@hono/ajv-validator](https://github.com/honojs/middleware/tree/main/packages/ajv-validator) | Ajv |
| [@hono/effect-validator](https://github.com/honojs/middleware/tree/main/packages/effect-validator) | Effect Schema |
| [@hono/class-validator](https://github.com/honojs/middleware/tree/main/packages/class-validator) | class-validator DTOs |

## Examples & starters

| Link | Notes |
|------|--------|
| [Getting Started](https://hono.dev/docs/getting-started/basic) | Hello world, middleware, adapters overview |
| [create-hono](https://github.com/honojs/create-hono) | Interactive templates Workers Bun Deno Node |
| [honojs/starter](https://github.com/honojs/starter) | Official starter template sources |
| [honojs/examples](https://github.com/honojs/examples) | Blog, JSX SSR, Durable Objects, Next.js stack |
| [Examples on hono.dev](https://hono.dev/examples/) | Curated walkthroughs from the docs site |
| [Hono stacks](https://hono.dev/docs/concepts/stacks) | Recommended pairing validator + client RPC |
| [Best practices](https://hono.dev/docs/guides/best-practices) | App structure tips |

## Related ecosystem

| Link | Notes |
|------|--------|
| [RPC / client guide](https://hono.dev/docs/guides/rpc) | Type-safe hc client sharing server types |
| [JSX guide](https://hono.dev/docs/guides/jsx) | Server JSX without a separate UI framework |
| [Cookie helper](https://hono.dev/docs/helpers/cookie) | get/set/delete cookies |
| [html helper](https://hono.dev/docs/helpers/html) | Tagged HTML strings |
| [Streaming helper](https://hono.dev/docs/helpers/streaming) | SSE / streaming responses |
| [SSG helper](https://hono.dev/docs/helpers/ssg) | Static site generation helpers |
| [Factory helper](https://hono.dev/docs/helpers/factory) | Typed middleware / handlers factories |
| [Testing helper](https://hono.dev/docs/helpers/testing) | app.request style tests |
| [HonoX](https://github.com/honojs/honox) | Meta-framework on Hono file-based routes |
| [vite-plugins](https://github.com/honojs/vite-plugins) | Dev server and build plugins for Hono |
| [@honojs/dev-server](https://github.com/honojs/vite-plugins/tree/main/packages/dev-server) | Vite plugin for local Hono apps |
| [honojs/cli](https://github.com/honojs/cli) | CLI aimed at AI coding agents |
| [honojs/vscode](https://github.com/honojs/vscode) | VS Code extension for Hono |
| [honojs/skills](https://github.com/honojs/skills) | Official agent skills for Hono |
| [Routing API](https://hono.dev/docs/api/routing) | Routers, params, wildcards |
| [Context API](https://hono.dev/docs/api/context) | c.req / c.json / variables |
| [xmcp Hono adapter](https://xmcp.dev/docs/adapters/hono) | Expose tools, resources, and prompts through an MCP endpoint in a Hono app |

## Contributing

1. PR = one live URL + a short blurb you wrote.
2. Prefer official docs, `@hono/*` packages, or actively maintained examples.
3. No paid starring, no dumping other awesome lists, no fake badges.

## License

List text: [CC0 1.0](./LICENSE). Linked projects keep their own licenses.
