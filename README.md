# Kazama: Ollama Client in Rust 🦀

🤖 Rust client library for interacting with the Ollama API, enabling seamless operations like chat completions, model pulls, embeddings generation, model listing, and model pushes.

## ✅ **Features:**
- Chat Completion: `chat_completion(model, content, role)`
- Model Pull: `pull_model(name, stream_mode)`
- Generate Embeddings: `gen_embeddings(model, prompt)`
- List Models: `list_models()`
- Push Models: `push_models(name, stream_mode)`

## ✅ **Usage:**
```rust
use kazama::{chat_completion, pull_model, gen_embeddings, list_models, push_models};

#[tokio::main]
async fn main() {
    // Example: Chat Completion
    chat_completion("model_name", "Hello!", "user").await.expect("Failed to complete chat");

    // Example: Model Pull
    pull_model("model_name", false).await.expect("Failed to pull model");

    // Example: Generate Embeddings
    gen_embeddings("model_name", "Generate embeddings from this prompt").await.expect("Failed to generate embeddings");

    // Example: List Models
    list_models().await.expect("Failed to list models");

    // Example: Push Models
    push_models("model_name", true).await.expect("Failed to push model");
}
```

For detailed API documentation, refer [here](https://crates.io/crates/kazama/).

