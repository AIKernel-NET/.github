# AIKernel.NET

AIKernelは、モデルやツールの接続、実行条件の設定、処理結果の確認を.NETアプリに組み込むためのモジュール式SDKです。

AIKernel is a modular .NET SDK for connecting AI models and tools, controlling execution, and inspecting what ran.

**最新版 / Latest stable SDK** [v0.1.4](https://github.com/AIKernel-NET/AIKernel.NET/releases/tag/v0.1.4) · [公式サイト / Website](https://aikernel.net/) · [技術ブログ / Technical blog](https://aikernel.net/blog/)

## はじめる / Get started

| やりたいこと | 日本語 | English |
| --- | --- | --- |
| 最初の.NETサンプルを動かす / Run the first .NET sample | [クイックスタート](https://aikernel.net/docs/overview/quick-start-jp/) | [Quickstart](https://aikernel.net/docs/overview/quick-start/) |
| 必要なパッケージを選ぶ / Choose packages | [NuGet・PyPI導入ガイド](https://aikernel.net/docs/operations/PACKAGE_INSTALLATION_GUIDE-jp/) | [NuGet and PyPI](https://aikernel.net/docs/operations/PACKAGE_INSTALLATION_GUIDE/) |
| 0.1.3から更新する / Upgrade from 0.1.3 | [移行ガイド](https://aikernel.net/docs/overview/upgrade-0-1-4-jp/) | [Upgrade guide](https://aikernel.net/docs/overview/upgrade-0-1-4/) |
| AIアシスタントと開発する / Build with an AI assistant | [開発者向け手引き](https://aikernel.net/ai/) | [Developer guide](https://aikernel.net/en/ai/) |
| ブラウザーでモデルを試す / Try models in a browser | [チャットデモ](https://aikernel.net/demo/chat/) | [Chat demo](https://aikernel.net/en/demo/chat/) |

最初の.NETサンプルは.NET 10 SDKで動作し、APIキーやGPUは不要です。既存の.NET 10プロジェクトに実行基盤を追加するには `AIKernel.Core` を参照します。

The first sample runs on the .NET 10 SDK without an API key or GPU. Add `AIKernel.Core` to an existing .NET 10 project to use the runtime.

```shell
dotnet add package AIKernel.Core --version 0.1.4
```

Pythonから使う場合 / For Python applications

```shell
python -m pip install aikernel-net==0.1.4
```

[公開NuGetパッケージ / NuGet packages](https://www.nuget.org/profiles/AIKernel-NET) · [Pythonパッケージ / PyPI](https://pypi.org/project/aikernel-net/0.1.4/)

## 0.1.4の主な機能 / What you can build

| 機能 / Feature | 公式資料 / Documentation |
| --- | --- |
| ローカル推論と操作の評価 / Local inference and governed operations | [モデル別・Bonsai CTGの呼び出し例](https://aikernel.net/docs/overview/inference-api-0-1-4-jp/) · [Inference and CTG API examples](https://aikernel.net/docs/overview/inference-api-0-1-4/) |
| 同じ業務処理をHTTPとMCPに公開 / Expose the same operation over HTTP and MCP | [サンプル](https://github.com/AIKernel-NET/AIKernel.Providers/blob/c184f421193a51a9f540804922ef481200de1ada/samples/DistributedApplication/README.md) · [Sample](https://github.com/AIKernel-NET/AIKernel.Providers/blob/c184f421193a51a9f540804922ef481200de1ada/samples/DistributedApplication/README.en.md) |
| 外部の音声合成エンジンを接続 / Connect an external text-to-speech engine | [AIKernel.Providers.Tts 0.1.4](https://www.nuget.org/packages/AIKernel.Providers.Tts/0.1.4) |
| 実行記録とリプレイ仕様 / Execution records and replay | [日本語仕様](https://github.com/AIKernel-NET/AIKernel.NET/blob/v0.1.4/docs/specs/06.REPLAY_DUMP_SPEC-jp.md) · [Replay format](https://github.com/AIKernel-NET/AIKernel.NET/blob/v0.1.4/docs/specs/06.REPLAY_DUMP_SPEC.md) |

CPU実行を標準とし、アクセラレーターや外部Providerは用途に応じて追加できます。対応モデル、OS、ドライバー、メモリ条件は個別のガイドで確認してください。

Start with CPU execution. Add accelerators and external Providers for the workloads that need them. Check the individual guides for supported models, operating systems, drivers, and memory requirements.

## リポジトリ / Repositories

| リポジトリ / Repository | 責務 / Responsibility |
| --- | --- |
| [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET) | 共有インターフェース、DTO、列挙型 / Shared interfaces, DTOs, and enums |
| [AIKernel.Core](https://github.com/AIKernel-NET/AIKernel.Core) | 実行基盤、ルーティング、ホスティング。`AIKernel.Kernel` 0.1.4 に CUDA Driver を同梱（ネイティブ依存は NVIDIA ドライバのみ） / Runtime, routing, and hosting. `AIKernel.Kernel` 0.1.4 bundles the CUDA Driver and requires the NVIDIA driver at runtime. |
| [AIKernel.Providers](https://github.com/AIKernel-NET/AIKernel.Providers) | 外部サービスとローカルエンジンの接続 / Adapters for services and local engines |
| [AIKernel.Control](https://github.com/AIKernel-NET/AIKernel.Control) | 実行制御と診断 / Execution control and diagnostics |
| [AIKernel.Tools](https://github.com/AIKernel-NET/AIKernel.Tools) | CLI、実行記録、調査ツール / CLI, execution records, and inspection |
| [AIKernel.Wasm](https://github.com/AIKernel-NET/AIKernel.Wasm) | ブラウザー実行とWebGPUの境界 / WebAssembly and WebGPU integration |
| [AIKernel.Cuda13.0](https://github.com/AIKernel-NET/AIKernel.Cuda13.0) | 0.1.3 までの旧 LibTorch 参照実装（保守終了・アーカイブ済み） / Legacy LibTorch reference implementation through 0.1.3 (unmaintained and archived). [CUDA Driver 移行ガイド / Migration guide](https://github.com/AIKernel-NET/AIKernel.Providers/blob/dev/docs/CUDA-DRIVER-MIGRATION.md) |
| [AIKernel.Demo](https://github.com/AIKernel-NET/AIKernel.Demo) | 実行できるサンプル / Runnable examples |

[パッケージごとの責務](https://aikernel.net/docs/architecture/module-map-jp/) · [Package responsibilities](https://aikernel.net/docs/architecture/module-map/) · [APIリファレンス / API reference](https://aikernel.net/reference/) · [お問い合わせ / Contact](https://aikernel.net/contact/)
