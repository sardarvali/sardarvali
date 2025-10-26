
<h1 align="center">Sardar Vali</h1>
<p align="center">
  <strong>DevOps Engineer • Cloud Architect • Android Developer</strong><br/>
  Building resilient cloud platforms, high-velocity CI/CD, and modern Android apps.
</p>

<p align="center">
  <a href="https://github.com/sardarvali"><img src="https://img.shields.io/badge/GitHub-Profile-181717?logo=github&logoColor=white"/></a>
  <img src="https://img.shields.io/badge/DevOps-Hands--on-blue?logo=linux&logoColor=white"/>
  <img src="https://img.shields.io/badge/IaC-Terraform-7B42BC?logo=terraform&logoColor=white"/>
  <img src="https://img.shields.io/badge/Containers-Docker-2496ED?logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kubernetes-Production%20Ready-326CE5?logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Android-Kotlin-7F52FF?logo=kotlin&logoColor=white"/>
</p>

<hr/>

## Cloud | Platforms | Languages
<p>
  <img src="https://img.shields.io/badge/OCI-FF0000?logo=oracle&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-232F3E?logo=amazon-aws&logoColor=FF9900"/>
  <img src="https://img.shields.io/badge/GCP-4285F4?logo=googlecloud&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-2671E5?logo=githubactions&logoColor=white"/>
  <img src="https://img.shields.io/badge/ArgoCD-EF7B4D?logo=argo&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white"/>
  <img src="https://img.shields.io/badge/Java-007396?logo=java&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Bash-4EAA25?logo=gnu-bash&logoColor=white"/>
</p>

---

## 🎓 Certifications
<p>
  <img src="https://img.shields.io/badge/✅-Verified-success"/>
</p>

<p>
  <img src="https://img.shields.io/badge/OCI%202025-AI%20Foundations%20Associate-red?logo=oracle&logoColor=white"/>
  <img src="https://img.shields.io/badge/Generative%20AI-Professional-blueviolet"/>
  <img src="https://img.shields.io/badge/OCI%202025-DevOps%20Professional-red?logo=oracle&logoColor=white"/>
  <img src="https://img.shields.io/badge/OCI%202025-Multicloud%20Architect%20Professional-red?logo=oracle&logoColor=white"/>
  <img src="https://img.shields.io/badge/OCI-Foundations%20Associate%20(2025)-red?logo=oracle&logoColor=white"/>
  <img src="https://img.shields.io/badge/OCI-Networking%20Professional-red?logo=oracle&logoColor=white"/>
</p>

> Note: Add credential IDs/links here for quick verification when available.

---

## 🧰 Tools & Technologies
- Clouds: OCI, AWS, GCP, Azure (basic)
- Containers & Orchestration: Docker, Kubernetes, Helm
- CI/CD: Jenkins, GitHub Actions, GitLab CI, Argo CD
- IaC & Config: Terraform, Ansible, CloudFormation
- Observability: Prometheus, Grafana, ELK, CloudWatch
- Databases: PostgreSQL, MySQL, MongoDB, Redis
- Languages: Kotlin, Java, Python, Bash, YAML, Groovy

---

<details>
  <summary>☁️ Cloud & DevOps Expertise</summary>

- Multi-cloud reference architectures (AWS, GCP, OCI) with resilient networking and 99.9%+ uptime
- GitOps workflows with Argo CD and Progressive Delivery (blue/green, canary)
- Secure supply chain (SLSA concepts), SBOM, and secrets management (Sealed Secrets, Vault)
- Policy as Code with OPA/Gatekeeper, RBAC, IAM, and least privilege
- Cost optimization, auto-scaling, and chaos testing for reliability
</details>

<details>
  <summary>📱 Android Development</summary>

- Kotlin-first, Jetpack Compose, MVVM + Clean Architecture
- Coroutines/Flow, Room, Retrofit/OkHttp, Kotlinx Serialization
- Modularization, DI (Hilt), testing with JUnit/MockK
- Material 3, animations, responsive UI, and accessibility
</details>

<details>
  <summary>🛠️ Technical Arsenal</summary>

- DevOps: Docker, Kubernetes, Jenkins, GitHub Actions, GitLab CI, Argo CD
- IaC: Terraform, Ansible, CloudFormation
- Security: IAM, RBAC, CIS benchmarks, image scanning, secret rotation
- SRE: Monitoring/alerting (Prometheus, Grafana), logging (ELK), tracing (OTel)
</details>

---

## 🧪 Example Snippets

### 1) CI/CD: GitHub Actions (containerized app)
```yaml
name: ci
on: [push, pull_request]
jobs:
  build-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-java@v4
        with:
          distribution: temurin
          java-version: '21'
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
      - name: Build
        run: ./gradlew build --no-daemon
      - name: Docker build
        run: |
          docker build -t ghcr.io/${{ github.repository }}:${{ github.sha }} .
      - name: Docker login
        run: echo $CR_PAT | docker login ghcr.io -u ${{ github.actor }} --password-stdin
      - name: Push image
        run: docker push ghcr.io/${{ github.repository }}:${{ github.sha }}
```

### 2) Dockerfile (distroless + non-root)
```dockerfile
FROM eclipse-temurin:21-jre AS base
WORKDIR /app
COPY build/libs/app.jar app.jar

FROM gcr.io/distroless/java21-debian12
USER 65532:65532
WORKDIR /app
COPY --from=base /app/app.jar /app/app.jar
ENTRYPOINT ["/usr/bin/java","-jar","/app/app.jar"]
```

### 3) Android ViewModel (Kotlin + Flow)
```kotlin
@HiltViewModel
class HomeViewModel @Inject constructor(
  private val repo: Repo
) : ViewModel() {
  private val _state = MutableStateFlow(State())
  val state: StateFlow<State> = _state.asStateFlow()

  fun load() = viewModelScope.launch {
    runCatching { repo.fetch() }
      .onSuccess { _state.update { it.copy(items = it.items + it) } }
      .onFailure { _state.update { it.copy(error = it.message) } }
  }

  data class State(
    val items: List<Item> = emptyList(),
    val error: String? = null
  )
}
```

### 4) Terraform (OCI VCN + subnet)
```hcl
provider "oci" {
  region = var.region
}

resource "oci_core_vcn" "main" {
  cidr_block     = "10.0.0.0/16"
  compartment_id = var.compartment_id
  display_name   = "main-vcn"
}

resource "oci_core_subnet" "public" {
  cidr_block        = "10.0.1.0/24"
  compartment_id    = var.compartment_id
  vcn_id            = oci_core_vcn.main.id
  display_name      = "public-subnet"
  prohibit_public_ip_on_vnic = false
}
```

---

## 🎯 Featured Projects
- DevOps: [K8s GitOps Starter](https://github.com/sardarvali/k8s-gitops-starter) <img src="https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white"/> <img src="https://img.shields.io/badge/Argo%20CD-EF7B4D?logo=argo&logoColor=white"/> <img src="https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white"/>
- Cloud: [OCI IaC Modules](https://github.com/sardarvali/oci-iac-modules) <img src="https://img.shields.io/badge/OCI-red?logo=oracle&logoColor=white"/> <img src="https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white"/>
- Android: [Compose Starter](https://github.com/sardarvali/compose-starter) <img src="https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white"/> <img src="https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white"/>

> Explore more at the pinned repositories below.

---

## 🌱 Currently Learning & Exploring
- Platform Engineering, Backstage, and Internal Developer Platforms (IDP)
- Advanced Kubernetes (eBPF, CNI, multi-cluster, service mesh)
- GenAI on clouds (OCI, AWS Bedrock, Vertex AI) and MLOps

---

## 💡 Philosophy
- Automate everything. Measure everything. Secure everything.
- Prefer simple, observable, and scalable designs.

---

## 📫 Let’s Connect!
<p>
  <a href="mailto:sardarvali1912@gmail.com"><img src="https://img.shields.io/badge/Email-Contact%20Me-D14836?logo=gmail&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/sardarvali"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white"/></a>
  <a href="https://twitter.com/sardarvali"><img src="https://img.shields.io/badge/X(Twitter)-Follow-000000?logo=x&logoColor=white"/></a>
  <a href="https://play.google.com/store/apps/dev?id="><img src="https://img.shields.io/badge/Google%20Play-Apps-414141?logo=google-play&logoColor=white"/></a>
</p>

<p align="center">
  🚀 If my work resonates, star the repos or reach out for collaboration!
</p>
