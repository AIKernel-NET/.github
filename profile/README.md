<div align="center">

<img src="https://raw.githubusercontent.com/AIKernel-NET/AIKernel.NET/main/docs/assets/aikernel-logo.png" alt="AIKernel.NET Logo" width="180" />

<h1>AIKernel.NET — Semantic Context OS</h1>

<p>
  <strong>An operating system for AI applications, designed around Semantic Context.</strong><br />
  <strong>Semantic Context を中心に設計された、AI アプリケーションのためのオペレーティングシステム。</strong>
</p>

</div>

---

**AIKernel.NET** is an OS-like architecture for AI applications.

AIKernel.NET does not define individual AI features themselves.  
It defines the deterministic execution context in which AI capabilities, reasoning workflows, agents, and applications can operate consistently.

**AIKernel.NET** は、AI アプリケーションのための OS 的アーキテクチャです。

AIKernel.NET は、個別の AI 機能そのものを定義するものではありません。  
AI の能力、推論ワークフロー、Agent、アプリケーションが一貫して動作するための、決定論的な実行コンテキストを定義します。

AIKernel.NET is organized as a four-layer stack:

AIKernel.NET は、次の 4 層スタックとして構成されます。

- **L4: Semantic App**
- **L3: AI Agent / AAU**  
  **AAU = Autonomous Agent Unit（自律型エージェント実行単位）**
- **L2: Pipeline**
- **L1: Provider**

Together, these layers form the foundation of the **Semantic Context OS**.

これらのレイヤーは、**Semantic Context OS** の基盤を構成します。

---

## AIKernel Stack — Sovereign Architecture

**AIKernel Stack — Sovereign Architecture** is a layered architecture for separating applications, agents, reasoning workflows, and providers around Semantic Context.

**AIKernel Stack — Sovereign Architecture** は、Semantic Context を中心に、アプリケーション、Agent、推論ワークフロー、Provider を分離して扱うための階層構造です。

---

### L4: Semantic App — セマンティックアプリ

A **Semantic App** is the top-level layer that transforms a user's **Semantic Intent** into value.

**Semantic App** は、ユーザーの **Semantic Intent** を価値へ変換する最上位レイヤーです。

It represents the application-level realization of a purpose by coordinating one or more Agents.

1 つ以上の Agent を統合し、目的をアプリケーションとして具体化します。

- Converts user intent into meaningful outcomes  
  ユーザーの意図を意味のある成果へ変換する
- Coordinates one or more Agents  
  1 つ以上の Agent を統合・調整する
- Serves as the application layer of the Semantic Context OS  
  Semantic Context OS のアプリケーション層として機能する

---

### L3: AI Agent / AAU — Autonomous Agent Unit

An **AI Agent** is an independent intelligence unit specialized for a specific purpose.

**AI Agent** は、特定の目的に特化した独立した知能単位です。

**AAU** stands for **Autonomous Agent Unit**.  
It represents an Agent as a governed executable unit that can encapsulate Pipelines, Providers, and runtime context.

**AAU** は **Autonomous Agent Unit（自律型エージェント実行単位）** の略です。  
Agent を、Pipeline、Provider、実行時コンテキストを内包できる、ガバナンス可能な実行単位として表します。

An AAU can be loaded from the VFS and executed independently within the Semantic Context OS.

AAU は VFS からロードされ、Semantic Context OS 内で独立した実行単位として扱われます。

- Acts as a purpose-specific intelligence unit  
  目的特化型の知能単位として機能する
- Encapsulates Pipelines, Providers, and runtime context  
  Pipeline、Provider、実行時コンテキストを内包する
- Operates as a governed executable unit  
  ガバナンス可能な実行単位として動作する

---

### L2: Pipeline — パイプライン

A **Pipeline** defines the logical reasoning workflow of an AI process.

**Pipeline** は、AI プロセスにおける論理的な推論ワークフローを定義します。

It describes how Providers are composed and executed to perform inference, retrieval, transformation, validation, and other AI-related operations.

Provider をどのように組み合わせ、推論・検索・変換・検証などの処理を進めるかを表現します。

- Defines the reasoning workflow  
  推論ワークフローを定義する
- Composes Providers into executable processes  
  Provider を実行可能なプロセスとして構成する
- Separates logical execution from physical capabilities  
  論理的な実行手順と物理的な能力を分離する

---

### L1: Provider — プロバイダー

A **Provider** is the physical grounding layer of AIKernel.NET.

**Provider** は、AIKernel.NET における物理的な接地レイヤーです。

Providers expose concrete capabilities such as LLMs, embeddings, VFS access, RAG, secure credentials, and other internal or external resources.

Provider は、LLM、Embedding、VFS、RAG、SecureCredential など、内部または外部の具体的な能力を提供します。

- Provides concrete AI and infrastructure capabilities  
  AI およびインフラストラクチャの具体的な能力を提供する
- Connects the OS to models, data sources, and external systems  
  OS をモデル、データソース、外部システムと接続する
- Acts as the capability unit of the system  
  システムにおける能力ユニットとして機能する

Examples:

- LLM Provider
- Embedding Provider
- VFS Provider
- RAG Provider
- SecureCredential Provider

---

## Vision: AIStore & Self-Extending AI

AIKernel.NET aims to enable an ecosystem where AI capabilities, Agents, and applications can be composed, distributed, and extended.

AIKernel.NET は、AI の能力、Agent、アプリケーションを構成・配布・拡張できるエコシステムの実現を目指します。

The long-term vision includes:

長期的なビジョンは以下のとおりです。

- **Provider Marketplace**  
  A marketplace for reusable AI and infrastructure capabilities.  
  再利用可能な AI 能力およびインフラ能力のマーケット。

- **Agent Marketplace**  
  A marketplace for purpose-specific Agent units.  
  目的特化型の Agent 単位を流通させるマーケット。

- **Semantic App Marketplace**  
  A marketplace for AI applications built on Semantic Context.  
  Semantic Context を基盤とした AI アプリケーションのマーケット。

- **Self-Extending AI**  
  AI systems that can extend their own capabilities through governed, composable units.  
  ガバナンスされた構成可能な単位を通じて、自ら能力を拡張できる AI システム。

- **AIDevOps**  
  A development model where AI assists in designing, building, testing, and evolving AI systems.  
  AI が AI システムの設計・実装・検証・進化を支援する開発モデル。

---

## Representative Repository

- [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET)

---

## Documents

- [AIKernel.NET Documentation](https://github.com/AIKernel-NET/AIKernel.NET/tree/main/docs)

---

## License

AIKernel.NET is released under the MIT License.

AIKernel.NET は MIT License の下で公開されています。