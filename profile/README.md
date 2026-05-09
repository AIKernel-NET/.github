<div align="center">

<img src="https://raw.githubusercontent.com/AIKernel-NET/AIKernel.NET/main/docs/assets/aikernel-logo.png" alt="AIKernel.NET Logo" width="160" />

# AIKernel.NET — Semantic Context OS

**AIKernel.NET is an AI operating system that treats Semantic Context as a first-class citizen.**  
**AIKernel.NET は、「意味的文脈（Semantic Context）」を第一級市民として扱う AI オペレーティングシステムです。**

</div>

AIKernel.NET provides a unified architecture for handling AI capabilities, reasoning workflows, intelligence units, and applications through a four-layer stack:

AIKernel.NET は、AI の能力・推論フロー・知能単位・アプリケーションを、4 層のスタックとして統一的に扱うためのアーキテクチャを提供します。

- **L4: Semantic App**
- **L3: AI Agent / AAU**
- **L2: Pipeline**
- **L1: Provider**

Together, these layers form the foundation of the **Semantic Context OS**.

これらのレイヤーは、**Semantic Context OS** の基盤を構成します。

---

## AIKernel Stack — Sovereign Architecture

（AIKernel Stack —主権的アーキテクチャ）

---

### L4: Semantic App（セマンティック・アプリ）

A **Semantic App** is the top-level layer that transforms a user's **Semantic Intent** into value.

**Semantic App** は、ユーザーの **Semantic Intent** を価値へ変換する最上位レイヤーです。

It represents the concrete realization of a purpose by orchestrating one or more Agents.

複数の Agent を束ね、目的を具体的な成果として具現化します。

- Converts user intent into meaningful outcomes  
  ユーザーの意図を意味のある成果へ変換する
- Coordinates one or more Agents  
  1 つ以上の Agent を統合・調整する
- Serves as the output layer of the Semantic Context OS  
  Semantic Context OS の出口として機能する

---

###  L3: AI Agent / AAU
（エージェント）

An **AI Agent** is an independent intelligence unit specialized for a specific purpose.

**AI Agent** は、特定の目的に特化した独立した知能単位です。

It encapsulates Pipelines and Providers, and can be loaded as an executable unit from the VFS.

Pipeline と Provider を内包し、VFS からロード可能な実行単位として扱われます。

- Purpose-specific intelligence packet  
  目的特化型の知能パケット
- Encapsulates Pipelines and Providers  
  Pipeline と Provider を内包する
- Operates as an independent executable unit  
  独立した実行単位として動作する

---

### L2: Pipeline
（パイプライン）

A **Pipeline** defines the logical reasoning workflow of an AI process.

**Pipeline** は、AI プロセスにおける論理的な推論ワークフローを定義します。

It describes how Providers are composed and executed to perform inference, retrieval, transformation, validation, or other AI-related operations.

Provider をどのように組み合わせ、推論・検索・変換・検証などの処理を進めるかを表現します。

- Defines the reasoning workflow  
  推論の流れを定義する
- Composes Providers into executable processes  
  Provider を実行可能なプロセスとして構成する
- Separates logical execution from physical capabilities  
  論理的な実行手順と物理的な能力を分離する

---

###  L1: Provider
（プロバイダー）

A **Provider** is the physical grounding layer of AIKernel.NET.

**Provider** は、AIKernel.NET における物理的な接地レイヤーです。

Providers expose concrete capabilities such as LLMs, embeddings, VFS access, RAG, secure credentials, and other external or internal resources.

LLM、Embedding、VFS、RAG、SecureCredential など、外部または内部の具体的な能力を提供します。

- Provides concrete AI and infrastructure capabilities  
  AI およびインフラストラクチャの具体的な能力を提供する
- Connects the OS to the outside world  
  OS を外界と接続する
- Acts as the capability unit of the system  
  システムにおける能力ユニットとして機能する

Examples:

例:

- LLM Provider
- Embedding Provider
- VFS Provider
- RAG Provider
- SecureCredential Provider

---

## Vision: AIStore & Self-Extending AI

（Vision: AIStore と自己拡張型 AI）

AIKernel.NET aims to enable an ecosystem where AI capabilities, intelligence units, and applications can be composed, distributed, and extended.

AIKernel.NET は、AI の能力・知能単位・アプリケーションを構成し、配布し、拡張できるエコシステムの実現を目指します。

The long-term vision includes:

長期的なビジョンは以下のとおりです。

- **Provider Marketplace**  
  A marketplace for reusable AI and infrastructure capabilities.  
  再利用可能な AI 能力およびインフラ能力のマーケット。

- **Agent Marketplace**  
  A marketplace for purpose-specific intelligence packets.  
  目的特化型の知能パケットを流通させるマーケット。

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

（代表リポジトリ）

- [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET)
- [AIKernel.Core](https://github.com/AIKernel-NET/AIKernel.Core)

---

## Documents
（ドキュメント）

- [AIKernel.NET Documentation](https://github.com/AIKernel-NET/AIKernel.NET/tree/main/docs)

---

## License
（ ライセンス）

AIKernel.NET is released under the MIT License.

AIKernel.NET は MIT License の下で公開されています。
