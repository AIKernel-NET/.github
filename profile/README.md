# AIKernel-NET

AIKernel-NET builds **AIKernel**, an OS-shaped runtime for governed AI
applications.

AIKernel treats models, tools, providers, WebAssembly runtimes, and native
accelerators as capability-bearing processes. The project focuses on stable
contracts, deterministic execution context, fail-closed governance, reproducible
replay, and provider isolation.

AIKernel also provides a modular SDK for building AIOS (AI Operating System)
distributions. Each repository maps to an OS layer: contracts, kernel runtime,
providers, control plane, WASM sandbox, GPU backend, observability tools, and
examples. Users assemble only the layers needed for their own AIOS distribution.

> AIKernel は AIOS（AI Operating System）ディストリビューションを構築するための
モジュール式 SDK でもあります。各 repository は OS の層（契約、kernel runtime、
providers、control plane、WASM sandbox、GPU backend、observability tools、
examples）に対応し、必要な層だけを組み合わせて独自の AIOS を構築できます。

AIKernel also has an official AIOS distribution, codenamed **AIKernel.Monolith**.
Monolith is the reference AIOS that integrates the Semantic OS layers after the
0.1.x SDK line stabilizes, embodying semantic runtime, capability graph, and
governance principles in one unified system.

> AIKernel には、公式 AIOS ディストリビューションである **AIKernel.Monolith** もあります。
Monolith は 0.1.x 系 SDK の安定化後に、semantic runtime、capability graph、
governance の思想を統合する標準 AIOS として開発が開始されています。

## Current Release Line

The current public package line is **0.1.1**.

Use the same version family across AIKernel packages. Do not mix 0.1.1
contracts with older Core, Providers, Tools, Wasm, Control, or Demo packages.

## Kernel Sync Day Release Entry

```text
You are reading the unified release entry for the AIKernel ecosystem.
Today is June 10 - Kernel Sync Day - the moment when all semantic surfaces align.
```

```text
これは AIKernel エコシステムの統一リリースエントリです。
本日は 6月10日--Kernel Sync Day--すべてのセマンティック面が同期する日です。
```

**June 10th, 2026 - Synchronizing the 0.1.1 semantic circuit.**
**2026年6月10日--0.1.1 のセマンティック回路を同期する。**

Synchronizing the 0.1.1 semantic circuit: the kernel, providers, and control
plane align into a coherent, governed Semantic OS.
> 0.1.1 のセマンティック回路を
同期--カーネル・プロバイダ・制御面が統治された一貫性ある Semantic OS へと整列する。

```text
[KERNEL.NET] Semantic Circuit: synchronized
[KERNEL.NET] Providers: registered
[KERNEL.NET] Control Plane: governed
```

Today, the Semantic OS becomes unified across all layers.
> 今日、Semantic OS は
全レイヤーを横断して統一された姿を手に入れました。

## Boot AIKernel In Three Lines

For the shortest AIKernel OS-style host path, start with Core, Standard
Providers, and Tools instrumentation:

```bash
dotnet add package AIKernel.Core --version 0.1.1
dotnet add package AIKernel.Providers.Standard --version 0.1.1
dotnet add package AIKernel.Tools.Instrumentation --version 0.1.1
```

First demo to run: **AIKernel.Demo.CoreRuntime**.

```bash
dotnet run --project src/AIKernel.Demo.CoreRuntime/AIKernel.Demo.CoreRuntime.csproj -c Release
```

## Required And Optional Layers

```text
Required:
  AIKernel.NET contracts
    -> AIKernel.Core
    -> AIKernel.Providers.Standard

Optional:
  AIKernel.Control   = physical execution engines
  AIKernel.Wasm      = browser/WebAssembly runtime and WebGPU boundary
  AIKernel.Cuda13.0  = Windows CUDA 13.0 external Capability
  External Providers = ChatOpenAI, MicrosoftAI, LocalLlm, ChatHistory, pipeline compiler
  AIKernel.Tools     = CLI, replay, inspectors, instrumentation
  AIKernel.Demo      = runnable learning and release validation examples
```

## Repository Map

| Repository | Role | Start here |
| --- | --- | --- |
| [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET) | Contract-first specification packages: abstractions, DTOs, enums, and boundary interfaces. | Install `AIKernel.Abstractions`, `AIKernel.Contracts`, `AIKernel.Dtos`, and `AIKernel.Enums` from the same version line. |
| [AIKernel.Core](https://github.com/AIKernel-NET/AIKernel.Core) | Deterministic runtime, monads, DSL, ROM/VFS, Kernel, Hosting, and CPU/default package family. | Validate Core before adding external providers or native capability modules. |
| [AIKernel.Providers](https://github.com/AIKernel-NET/AIKernel.Providers) | Official extension Providers and standard OS driver implementations. | Start with descriptor, manifest, and dry-run validation before enabling live endpoints or native drivers. |
| [AIKernel.Control](https://github.com/AIKernel-NET/AIKernel.Control) | Physical execution layer for semantic graphs: emulator, CPU/GPU engines, diagnostics, and Bonsai-style execution. | Validate CPU and Emulator paths before binding GPU execution. |
| [AIKernel.Tools](https://github.com/AIKernel-NET/AIKernel.Tools) | `aik` CLI, replay, inspectors, canonical formatting, instrumentation, and operator tooling. | Install the .NET tool and run the four smoke commands below. |
| [AIKernel.Wasm](https://github.com/AIKernel-NET/AIKernel.Wasm) | Browser/WebAssembly runtime, WASM Providers, and WebGPU compute boundary. | Run deterministic tests first; keep real browser GPU validation as a manual step. |
| [AIKernel.Cuda13.0](https://github.com/AIKernel-NET/AIKernel.Cuda13.0) | Windows `win-x64` CUDA 13.0 + LibTorch 2.12 external Capability package. | Use only on trusted Windows GPU hosts that explicitly opt in to CUDA execution. |
| [AIKernel.Demo](https://github.com/AIKernel-NET/AIKernel.Demo) | Runnable teaching and validation workspace covering the 0.1.1 package family. | Start with CoreRuntime, Contracts, StandardProviders, Providers, Control, Tools, Wasm, and Cuda demos. |

## Repository Entry Points

Use these links when you already know which layer you need.

| Need | Repository | Documentation | Release Notes |
| --- | --- | --- | --- |
| Contract vocabulary, DTOs, enums, interface packages | [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET) | [README](https://github.com/AIKernel-NET/AIKernel.NET#readme) / [specs](https://github.com/AIKernel-NET/AIKernel.NET/tree/main/docs/specs) | [Release notes](https://github.com/AIKernel-NET/AIKernel.NET/blob/main/RELEASE_NOTES.md) |
| Core runtime, Kernel, Hosting, VFS/ROM, monads | [AIKernel.Core](https://github.com/AIKernel-NET/AIKernel.Core) | [README](https://github.com/AIKernel-NET/AIKernel.Core#readme) / [User Guide](https://github.com/AIKernel-NET/AIKernel.Core/blob/main/docs/user-guide/index.md) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Core/blob/main/RELEASE_NOTES.md) |
| Official Providers and standard OS drivers | [AIKernel.Providers](https://github.com/AIKernel-NET/AIKernel.Providers) | [README](https://github.com/AIKernel-NET/AIKernel.Providers#readme) / [Provider docs](https://github.com/AIKernel-NET/AIKernel.Providers/tree/main/docs) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Providers/blob/main/RELEASE_NOTES.md) |
| Physical execution engines and Bonsai-style execution | [AIKernel.Control](https://github.com/AIKernel-NET/AIKernel.Control) | [README](https://github.com/AIKernel-NET/AIKernel.Control#readme) / [Control docs](https://github.com/AIKernel-NET/AIKernel.Control/tree/main/docs) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Control/blob/main/RELEASE_NOTES.md) |
| CLI, replay, inspectors, instrumentation | [AIKernel.Tools](https://github.com/AIKernel-NET/AIKernel.Tools) | [README](https://github.com/AIKernel-NET/AIKernel.Tools#readme) / [CLI docs](https://github.com/AIKernel-NET/AIKernel.Tools/blob/main/docs/cli/index.md) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Tools/blob/main/RELEASE_NOTES.md) |
| Browser/WASM runtime and WebGPU boundary | [AIKernel.Wasm](https://github.com/AIKernel-NET/AIKernel.Wasm) | [README](https://github.com/AIKernel-NET/AIKernel.Wasm#readme) / [WASM docs](https://github.com/AIKernel-NET/AIKernel.Wasm/tree/main/docs) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Wasm/blob/main/RELEASE_NOTES.md) |
| Windows CUDA 13.0 + LibTorch external Capability | [AIKernel.Cuda13.0](https://github.com/AIKernel-NET/AIKernel.Cuda13.0) | [README](https://github.com/AIKernel-NET/AIKernel.Cuda13.0#readme) / [distribution guide](https://github.com/AIKernel-NET/AIKernel.Cuda13.0/blob/main/docs/package-distribution.md) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Cuda13.0/blob/main/RELEASE_NOTES.md) |
| Runnable learning and validation examples | [AIKernel.Demo](https://github.com/AIKernel-NET/AIKernel.Demo) | [README](https://github.com/AIKernel-NET/AIKernel.Demo#readme) / [User Guide](https://github.com/AIKernel-NET/AIKernel.Demo/blob/main/docs/user-guide/index.md) | [Release notes](https://github.com/AIKernel-NET/AIKernel.Demo/blob/main/RELEASE_NOTES.md) |

## Quick Start

Install the CLI:

```bash
dotnet tool install -g AIKernel.Tools.CLI --version 0.1.1
```

Run the smallest checks:

```bash
aik runtime ping
aik system info
aik system vfs --vfs-root .
aik capabilities invoke aikernel.vfs vfs.exists path=README.md
```

For .NET applications, keep package versions aligned:

```bash
dotnet add package AIKernel.Core --version 0.1.1
dotnet add package AIKernel.Hosting --version 0.1.1
dotnet add package AIKernel.Kernel --version 0.1.1
```

For Python:

```bash
pip install aikernel-net
pip install aikernel-providers
pip install aikernel-tools
pip install aikernel-wasm
```

CUDA is a separate explicit opt-in package and does not belong to the default
Core or Python install path.

## NuGet Packages

NuGet packages are the primary distribution channel for .NET hosts. Keep all
AIKernel packages on the same public version family.

### Contracts

Install these when you need the stable public contract vocabulary without
runtime implementation:

```bash
dotnet add package AIKernel.Abstractions --version 0.1.1
dotnet add package AIKernel.Contracts --version 0.1.1
dotnet add package AIKernel.Dtos --version 0.1.1
dotnet add package AIKernel.Enums --version 0.1.1
```

### Core Runtime

Install these for deterministic runtime, hosting, Kernel, common monads, and
contract test helpers:

```bash
dotnet add package AIKernel.Common --version 0.1.1
dotnet add package AIKernel.Core --version 0.1.1
dotnet add package AIKernel.Hosting --version 0.1.1
dotnet add package AIKernel.Kernel --version 0.1.1
dotnet add package AIKernel.TestKit --version 0.1.1
```

### Official Providers

Install only the provider packages your host actually needs:

```bash
dotnet add package AIKernel.Providers.ChatOpenAI --version 0.1.1
dotnet add package AIKernel.Providers.ChatHistory --version 0.1.1
dotnet add package AIKernel.Providers.CudaCompute --version 0.1.1
dotnet add package AIKernel.Providers.DynamicPipelineCompiler --version 0.1.1
dotnet add package AIKernel.Providers.LocalLlm --version 0.1.1
dotnet add package AIKernel.Providers.MicrosoftAI --version 0.1.1
dotnet add package AIKernel.Providers.Standard --version 0.1.1
```

### Control, Tools, Wasm, and CUDA

```bash
dotnet add package AIKernel.Control.Core --version 0.1.1
dotnet add package AIKernel.Control.CPU --version 0.1.1
dotnet add package AIKernel.Control.Emulator --version 0.1.1
dotnet add package AIKernel.Control.Diagnostics --version 0.1.1
dotnet add package AIKernel.Control.GPU --version 0.1.1

dotnet add package AIKernel.Tools.Instrumentation --version 0.1.1
dotnet add package AIKernel.Tools.Capability.RomStorage --version 0.1.1
dotnet add package AIKernel.Tools.Inspectors.ChatHistoryScraper --version 0.1.1
dotnet add package AIKernel.Tools.Inspectors.KernelClock --version 0.1.1
dotnet add package AIKernel.Tools.Inspectors.Vfs --version 0.1.1

dotnet add package AIKernel.Wasm.Runtime --version 0.1.1
dotnet add package AIKernel.Wasm.WebGpuComputeProvider --version 0.1.1

dotnet add package AIKernel.Cuda13.0.Libtorch2.12.win-x64 --version 0.1.1
```

`AIKernel.Cuda13.0.Libtorch2.12.win-x64` is Windows `win-x64` only. Its NuGet
package is lightweight; full CUDA/LibTorch runtime assets are distributed
through the matching GitHub Release archive.

The CLI is distributed as a .NET tool:

```bash
dotnet tool install -g AIKernel.Tools.CLI --version 0.1.1
```

NuGet profile: [AIKernel-NET on NuGet](https://www.nuget.org/profiles/AIKernel-NET)

## PyPI Packages

Python packages are thin wrappers over the public C# package surfaces. They do
not reimplement AIKernel runtime, provider, governance, tooling, or WASM
semantics in Python.

```bash
pip install aikernel-net
pip install aikernel-governance
pip install aikernel-providers
pip install aikernel-tools
pip install aikernel-wasm
```

CUDA Python support is also explicit opt-in:

```bash
pip install aikernel-cuda13-libtorch2-12-win-x64
```

Import names:

```python
import aikernel_net
import aikernel_governance
import aikernel_providers
import aikernel_tools
import aikernel_wasm
import aikernel_cuda13_libtorch2_12_win_x64
```

PyPI packages bundle or discover managed assemblies and delegate to the public
.NET contract surface. Native CUDA runtime assets remain outside the default
Python install path.

## Architecture In One Screen

```text
AIKernel.NET       = contracts, DTOs, enums, public boundary vocabulary
AIKernel.Core      = deterministic runtime, monads, DSL, Kernel, VFS/ROM
AIKernel.Providers = official provider drivers and standard OS drivers
AIKernel.Control   = physical execution engines and Bonsai-style execution
AIKernel.Tools     = CLI, replay, inspectors, instrumentation
AIKernel.Wasm      = browser/WASM runtime and WebGPU boundary
AIKernel.Cuda13.0  = Windows CUDA external Capability
AIKernel.Demo      = runnable learning and release validation examples
```

## Documentation Principles

- Public contracts live in AIKernel.NET and AIKernel.Core.
- Provider-specific endpoint, credential, and native-driver behavior belongs in
  AIKernel.Providers or dedicated capability repositories.
- Tools inspect, invoke, export, and diagnose; they do not own provider
  implementations.
- WASM-specific runtime behavior stays in AIKernel.Wasm.
- Demo projects consume public packages only and should remain safe, dry-run
  friendly, and educational.
- Release notes describe public package releases. Development package changes
  are folded into the next public release note.

## 日本語

AIKernel-NET は、AI アプリケーションを OS のように扱うための **AIKernel**
を構築しています。

AIKernel は、model、tool、Provider、WebAssembly runtime、native accelerator を
Capability を持つ process として扱います。重視しているのは、安定した contract、
決定論的な実行 context、fail-closed governance、reproducible replay、Provider
isolation です。

現在の public package line は **0.1.1** です。利用時は AIKernel package の version
family を揃えてください。0.1.1 の contract と古い Core / Providers / Tools /
Wasm / Control / Demo package を混在させないでください。

AIKernel を最短で起動する場合:

```bash
dotnet add package AIKernel.Core --version 0.1.1
dotnet add package AIKernel.Providers.Standard --version 0.1.1
dotnet add package AIKernel.Tools.Instrumentation --version 0.1.1
```

最初に触るべき demo は **AIKernel.Demo.CoreRuntime** です。

最初に試す場合:

```bash
dotnet tool install -g AIKernel.Tools.CLI --version 0.1.1
aik runtime ping
aik system info
aik system vfs --vfs-root .
aik capabilities invoke aikernel.vfs vfs.exists path=README.md
```

学習用には [AIKernel.Demo](https://github.com/AIKernel-NET/AIKernel.Demo) を
入口にしてください。CoreRuntime、Contracts、StandardProviders、Providers、
Control、Tools、Wasm、Cuda の順に確認すると、AIKernel 0.1.1 の全体像を追えます。

NuGet は .NET host 向けの配布 channel です。契約だけを使う場合は
`AIKernel.Abstractions`、`AIKernel.Contracts`、`AIKernel.Dtos`、`AIKernel.Enums`
を同じ version family で導入してください。実行環境には `AIKernel.Core`、
`AIKernel.Hosting`、`AIKernel.Kernel` を追加し、必要に応じて
`AIKernel.Providers.*`、`AIKernel.Control.*`、`AIKernel.Wasm.*`、`AIKernel.Tools.*`
を導入します。

PyPI では `aikernel-net`、`aikernel-governance`、`aikernel-providers`、
`aikernel-tools`、`aikernel-wasm` を提供します。これらは C# public surface への
薄い wrapper であり、Python 側で runtime semantics を再実装しません。

各 repository への入口は上記の Repository Entry Points を使ってください。まず全体像を
学ぶ場合は `AIKernel.Demo`、契約から確認する場合は `AIKernel.NET`、実行 runtime から
確認する場合は `AIKernel.Core` が入口になります。
