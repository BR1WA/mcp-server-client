# mcp-server-client

A simple demonstration of a Java-based MCP (Model Context Protocol) server and client implementation. The server uses Spring Boot and exposes MCP-compliant endpoints, while the client uses standard Java and supports full UI testing via Swagger.

## ✨ Features

* **Spring Boot Server**: Hosts MCP-compatible endpoints over JSON-RPC
* **Java Client**: Sends A2A and MCP requests
* **Postman Testing**: Built-in support for Postman requests via JSON-RPC
* **Swagger UI**: Fully interactive UI for testing client interactions

## 🚀 Quick Start

### Prerequisites

* Java 17+
* Maven
* Postman (optional, for server testing)
* Browser (for Swagger UI testing)

### Clone & Build

```bash
# Clone the repo
git clone https://github.com/BR1WA/mcp-server-client.git
cd mcp-server-client

# Build all modules
mvn clean install
```

### Run the Server

```bash
cd server
mvn spring-boot:run
```

Server runs at: `http://localhost:8877/`

### Run the Client

```bash
cd client
mvn spring-boot:run
```

Swagger UI available at: `http://localhost:8086/swagger-ui/index.html`

## 🔧 Testing

### ✅ Server via Postman

The server supports MCP requests directly. You can test using Postman:

**Example MCP Request:**

```json
POST http://localhost:8877/
Content-Type: application/json
{
  "jsonrpc": "2.0",
  "method": "tools/list",
  "params": {},
  "id": 1
}
```

You can also test other methods like `tools/call`, `initialize`, etc.

### ✅ Client via Swagger UI

Once the client is running, visit:

```
http://localhost:8086/swagger-ui/index.html
```

Use the interactive page to:

* Send messages
* Trigger prompts
* Simulate A2A or MCP message flows

## 📂 Project Structure

```
mcp-server-client/
├── mcp-clit/        # Java client with Swagger UI
├── mcp-server/        # Spring Boot MCP server
├── pom.xml        # Parent Maven file
└── README.md
```

## 🙌 Author

[BR1WA](https://github.com/BR1WA)
