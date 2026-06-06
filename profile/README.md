<div align="center">

<img src="https://raw.githubusercontent.com/AIKernel-NET/AIKernel.NET/main/docs/assets/aikernel-logo.png" alt="AIKernel.NET Logo" width="180" />

# AIKernel.NET

**Interface-led runtime architecture for semantic AI systems**
**Semantic AI システムのための Interface-Led Runtime Architecture**

</div>

---

AIKernel.NET defines a deterministic execution foundation for AI applications:
contracts, monads, semantic DSLs, replay logs, capability routing, VFS/ROM
semantics, and governed provider execution.

AIKernel.NET は、AI アプリケーションのための決定論的な実行基盤を定義します。対象は
Contracts、Monads、Semantic DSL、ReplayLog、Capability Routing、VFS/ROM
セマンティクス、Governed Provider Execution です。

## Release Line

The current release line is **v0.0.5**.

- **AIKernel.NET** provides the public contracts, DTOs, enums, and canonical documents.
- **AIKernel.Core** provides the runtime implementation: Common monads, Core, Kernel, Hosting, providers, TestKit, and Python binding.
- **AIKernel.Cuda13.0** provides the opt-in Windows CUDA capability package.

Core packages are CUDA-free by default. GPU and native accelerator support lives in
separate Capability repositories so each CUDA / LibTorch / OS / RID combination can
evolve independently.

現在のリリース系列は **v0.0.5** です。

- **AIKernel.NET** は public contracts、DTO、Enum、正典ドキュメントを提供します。
- **AIKernel.Core** は runtime 実装を提供します。Common monads、Core、Kernel、Hosting、providers、TestKit、Python binding が含まれます。
- **AIKernel.Cuda13.0** は opt-in の Windows CUDA Capability package を提供します。

Core package は既定で CUDA-free です。GPU / native accelerator support は
Capability リポジトリに分離され、CUDA / LibTorch / OS / RID ごとに独立して進化します。

## Package Map

| Area | Packages / Repositories |
| --- | --- |
| Contracts | `AIKernel.Abstractions`, `AIKernel.Dtos`, `AIKernel.Enums` |
| Runtime | `AIKernel.Common`, `AIKernel.Core`, `AIKernel.Kernel`, `AIKernel.Hosting` |
| Providers | `AIKernel.Providers.MicrosoftAI` |
| Testing | `AIKernel.TestKit` |
| Python | `aikernel` |
| CUDA Capability | `AIKernel.Cuda13.0.Libtorch2.12.win-x64` |

`AIKernel.Vfs` is not a separate package. VFS contracts belong to Abstractions,
and implementation lives in Core/Kernel runtime packages.

`AIKernel.Vfs` は独立 package ではありません。VFS contracts は Abstractions に、
実装は Core/Kernel runtime packages に配置されます。

## Install

### .NET Runtime

```powershell
dotnet add package AIKernel.Core --version 0.0.5
dotnet add package AIKernel.Kernel --version 0.0.5
dotnet add package AIKernel.Hosting --version 0.0.5
dotnet add package AIKernel.Providers.MicrosoftAI --version 0.0.5
```

### Python Binding

```powershell
pip install aikernel
```

The Python package is CPU-only by default and exposes the outer AIKernel API,
monad helpers, managed assembly discovery, and DSL composition helpers.

Python package は既定で CPU-only です。外側の AIKernel API、monad helpers、
managed assembly discovery、DSL composition helpers を提供します。

### Optional CUDA Capability

```powershell
dotnet add package AIKernel.Cuda13.0.Libtorch2.12.win-x64 --version 0.0.5
```

This package targets Windows `win-x64`, CUDA 13.0, and LibTorch 2.12.0.
Other CUDA, LibTorch, OS, or RID combinations should be implemented as separate
Capability repositories using the same public AIKernel contracts.

この package は Windows `win-x64`、CUDA 13.0、LibTorch 2.12.0 を対象にします。
他の CUDA / LibTorch / OS / RID の組み合わせは、同じ public AIKernel contracts に従う
別 Capability リポジトリとして実装します。

## Architecture

AIKernel is organized around a small set of stable boundaries:

- **Contracts**: interface-only public boundary for implementations.
- **Common**: pure functional primitives such as Result, Option, Either, and ResultStep.
- **Core / Kernel**: deterministic orchestration, DSL execution, ReplayLog, VFS/ROM, and governance.
- **Providers**: external model or service integrations.
- **Capabilities**: opt-in native, GPU, solver, or tool modules.
- **Bindings**: language-facing APIs such as Python.

AIKernel は、安定した境界を中心に構成されます。

- **Contracts**: 実装を結合するための interface-only public boundary。
- **Common**: Result、Option、Either、ResultStep などの純粋な functional primitives。
- **Core / Kernel**: 決定論的 orchestration、DSL execution、ReplayLog、VFS/ROM、governance。
- **Providers**: 外部モデルまたは service integrations。
- **Capabilities**: opt-in の native / GPU / solver / tool modules。
- **Bindings**: Python などの language-facing API。

## Repositories

- [AIKernel.NET](https://github.com/AIKernel-NET/AIKernel.NET): contracts, DTOs/enums, architecture docs, canonical papers.
- [AIKernel.Core](https://github.com/AIKernel-NET/AIKernel.Core): runtime packages, monads, DSL, Kernel, providers, Python binding.
- [AIKernel.Cuda13.0](https://github.com/AIKernel-NET/AIKernel.Cuda13.0): CUDA 13.0 / LibTorch 2.12 / Windows win-x64 capability.
- [AIKernel.RH](https://github.com/AIKernel-NET/AIKernel.RH): proof-oriented and native capability experiments.
- [AIKernel.Tools](https://github.com/AIKernel-NET/AIKernel.Tools): tooling and capability helpers.

## License

AIKernel uses different licenses by layer:

| Layer | Scope | License | Reason |
| --- | --- | --- | --- |
| AIKernel.NET | Interfaces and DTOs | MIT | Easy standardization; no implementation patent surface |
| AIKernel.Core | DSL, monads, Kernel abstractions | Apache License 2.0 | Patent grant for runtime architecture |
| Capability | CUDA, ROCm, DirectML, external modules | Apache License 2.0 | Native/GPU implementation risk |
| Native ABI | `libtorch_bridge` and C++ bridges | Apache License 2.0 | Native implementation risk |
| Python | Python binding | Apache License 2.0 | Stronger fit for binary-capable distribution |

AIKernel はレイヤーごとにライセンスを分けます。

| レイヤー | 内容 | ライセンス | 理由 |
| --- | --- | --- | --- |
| AIKernel.NET | Interface と DTO | MIT | 標準化しやすく、実装特許面がない |
| AIKernel.Core | DSL、モナド、Kernel 抽象 | Apache License 2.0 | ランタイムアーキテクチャに特許条項が必要 |
| Capability | CUDA、ROCm、DirectML、外部 module | Apache License 2.0 | Native/GPU 実装リスクが高い |
| Native ABI | `libtorch_bridge` などの C++ bridge | Apache License 2.0 | Native 実装リスクが高い |
| Python | Python binding | Apache License 2.0 | バイナリ配布を含む配布形態に強い |

Third-party native dependencies keep their own licenses and notices.

third-party native dependencies は、それぞれの license / notice を保持します。
