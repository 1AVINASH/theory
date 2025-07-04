## MCP (Model Context Protocol)
* MCP defines a standardized interface for supplying structured, real-time context to LLMs
* MCP lets you pull in external resources — like files, database rows, or API responses — right into the prompt or working memory. All of it comes through a standardized interface, so your LLM can stay lightweight and clean.
* MCP also lets models call tools dynamically. You can register capabilities like searchCustomerData or generateReport, and the LLM can invoke them on demand. It’s like giving your AI access to a toolbox, but without hardwiring the tools into the model itself.

### Implementation Characteristics
* Operates over HTTP(S) with JSON-based capability descriptors
* Designed to be model-agnostic — any LLM with a compatible runtime can leverage MCP-compliant servers
* Compatible with API gateways and enterprise authentication standards (e.g., OAuth2, mTLS)

## ACP (Agent Communication Protocol)
* An open standard originally proposed by BeeAI and IBM to enable structured communication, discovery, and coordination between AI agents operating in the same local or edge environment.
* Unlike cloud-oriented protocols such as A2A or context-routing protocols like MCP, ACP is designed for local-first, real-time agent orchestration with minimal network overhead and tight integration across agents deployedc within a shared runtime.

## Implementation
* Each agent advertises its identity, capabilities, and state using a local broadcast/discovery layer.
* Agents communicate through event-driven messaging, often using a local bus or IPC (inter-process communication) system.

## A2A (Agent to agent protocol)
* The Agent-to-Agent (A2A) Protocol, introduced by Google, is a cross-platform specification for enabling AI agents to communicate, collaborate, and delegate tasks across heterogeneous systems.
* Unlike ACP’s local-first focus or MCP’s tool integration layer, A2A addresses horizontal interoperability — standardizing how agents from different vendors or runtimes can exchange capabilities and coordinate workflows over the open web.
* A2A defines a HTTP-based communication model where agents are treated as interoperable services. Each agent exposes an “Agent Card” — a machine-readable JSON descriptor detailing its identity, capabilities, endpoints, and authentication requirements.

