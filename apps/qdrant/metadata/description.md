# Qdrant

Qdrant is a high-performance vector search engine and database designed for managing and searching through large-scale vector datasets. It is built to support advanced use cases in artificial intelligence and machine learning, offering robust search capabilities alongside persistent storage and high availability.

## Features

- **High Performance:** Optimized for rapid vector searches.
- **Multi-Protocol APIs:**  
  - **HTTP API & Health/Metrics Endpoints:** Accessible on port **6333**  
  - **gRPC API:** Accessible on port **6334**
  - **Distributed Deployment:** Uses port **6335** for inter-node communication.
- **Persistent Storage:** Ensures durability by mounting block-level storage to `/qdrant/storage`.
- **Flexible Deployment:** Suitable for both development (via Docker Compose) and production environments (via Kubernetes, Qdrant Cloud, or the Enterprise Operator).

## Installation & Setup

1. **Deployment Options:**  
   - **Development:** Run Qdrant using Docker or Docker Compose.
   - **Production:** Consider using Kubernetes with the official Helm chart, the Qdrant Cloud, or the Enterprise Operator for high availability and scalability.
   
2. **Port Configuration:**  
   - **HTTP API & Health Checks:** 6333  
   - **gRPC API:** 6334  
   - **Cluster Communication:** 6335

3. **Volumes:**  
   Mount a persistent storage volume to `/qdrant/storage` to retain your vector data and configurations across container restarts.

4. **Custom Configuration:**  
   If needed, override the default configuration by mounting your own configuration file (for example, to `/qdrant/config/production.yaml`).

For more details on resource requirements and advanced configuration options, please refer to the [official Qdrant documentation](https://github.com/qdrant/qdrant).
