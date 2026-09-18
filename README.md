# System Design Case Studies

Architecture case studies for discussing APIs, multi-tenant SaaS, asynchronous provisioning, and legacy modernisation.

These are deliberately evidence-led thought exercises. They use synthetic constraints and clearly-labelled assumptions; they do not reproduce employer code, internal diagrams, customer data, credentials, or confidential operational details.

## Case studies

| Case study | Question it explores | Main trade-off |
| --- | --- | --- |
| [Scalable REST API](docs/scalable-rest-api.md) | How can a versioned API remain predictable as clients and traffic grow? | Simplicity and compatibility versus feature velocity |
| [Multi-tenant SaaS](docs/multi-tenant-saas.md) | How should tenant isolation work across requests, data, and operations? | Strong isolation versus operational cost |
| [Asynchronous provisioning](docs/asynchronous-provisioning.md) | How can a workflow tolerate provider latency, retries, and duplicate messages? | Eventual consistency versus responsive request handling |
| [Legacy modernisation](docs/legacy-modernisation.md) | How can a critical monolith be improved without a risky rewrite? | Incremental safety versus architectural purity |

## How to read these studies

Each study states its assumptions, proposes a design, names failure modes, and explains what would be measured. Numbers are omitted unless they are explicit hypothetical planning inputs. No production metric is implied.

## Engineering lens

- Make boundaries and ownership visible.
- Treat failure, retries, and degraded modes as first-class design inputs.
- Keep authentication, authorisation, and data isolation explicit.
- Prefer reversible migration steps over a single rewrite.
- Connect architecture decisions to operability and team workflows.

## Validation

The repository is documentation-only. Every case study includes a Mermaid diagram and a trade-off section. The included CI workflow checks that the required documents and diagrams remain present.

## License

MIT. See [LICENSE](LICENSE).
