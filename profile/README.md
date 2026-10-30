> **An open-source, declarative application delivery platform designed to resolve the fundamental tension in modern cloud delivery: balancing autonomous developer release velocity with strict, automated security governance.**   

### Architecture

IngotADP decouples foundational cloud primitives from tenant application logic using modular, version-pinned components via a repository-native **Hub-and-Spoke** topology:   

🔸 **[ingot-core](https://github.com/ingotadp/ingot-core) (The Hub):** The authoritative control plane managing shared cloud infrastructure, remote state-locking, and zero-trust identity federation (Google Cloud Workload Identity Federation).   
🔸 **[ingot-build](https://github.com/ingotadp/ingot-build) (Spoke):** Reusable workflow engines providing container compilation, granular caching, and multi-architecture build orchestration.   
🔸 **[ingot-observe](https://github.com/ingotadp/ingot-observe) (Spoke):** OpenTelemetry-compliant pipeline metrics, distributed tracing, and deployment health telemetry.   
🔸 **[ingot-secure](https://github.com/ingotadp/ingot-secure) (Spoke):** Declarative Policy-as-Code (Open Policy Agent / Rego) and supply chain security gating (Trivy, Gitleaks) enforced automatically pre-merge.   
🔸 **[ingot-sandbox](https://github.com/ingotadp/ingot-sandbox) (Spoke):** Ephemeral, disposable staging and preview environments for isolated validation.   

---

### Key Capabilities

* **Zero-Trust Credentialing:** Completely eliminates long-lived static cloud keys in CI runners via short-lived OIDC tokens.   
* **Drift Elimination:** Shared infrastructure baselines and policies are defined once at the hub and consumed declaratively by application spokes.   
* **Minimal Developer Friction:** Polyglot application services register via lightweight YAML manifests without having to maintain boilerplate IaC or container build scripts.   
* **Empirically Evaluated:** Developed as part of an MSc Computer Science dissertation project at Keele University, quantitatively evaluating delivery lead times, configuration reuse, and automated compliance efficacy.   

### Licence

All repositories under IngotADP are open source and provided under the MIT License.   
