<div align="justify">

> An open-source, declarative application delivery platform designed to resolve the fundamental tension in modern cloud delivery: balancing autonomous developer release velocity with strict, automated security governance.   

</div>

### Architecture

<div align="justify">

IngotADP decouples foundational cloud primitives from tenant application logic using modular, version-pinned components via a repository-native **Hub-and-Spoke** topology:   

🔸 **[ingot-core](https://github.com/ingotadp/ingot-core) (The Hub):** The authoritative control plane managing shared cloud infrastructure, remote state-locking, and zero-trust identity federation (Google Cloud Workload Identity Federation).   
🔸 **[ingot-build](https://github.com/ingotadp/ingot-build) (Spoke):** Reusable workflow engines providing container compilation, granular caching, and multi-architecture build orchestration.   
🔸 **[ingot-observe](https://github.com/ingotadp/ingot-observe) (Spoke):** OpenTelemetry-compliant pipeline metrics, distributed tracing, and deployment health telemetry.   
🔸 **[ingot-secure](https://github.com/ingotadp/ingot-secure) (Spoke):** Declarative Policy-as-Code (Open Policy Agent / Rego) and supply chain security gating (Trivy, Gitleaks) enforced automatically pre-merge.   
🔸 **[ingot-sandbox](https://github.com/ingotadp/ingot-sandbox) (Spoke):** Ephemeral, disposable staging and preview environments for isolated validation.   

</div>

### Licence

<div align="justify">

All repositories under IngotADP are open source and provided under the MIT License.   

</div>
