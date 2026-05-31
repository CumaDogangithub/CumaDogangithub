<!-- ============ LIVED-IN BLUEPRINT · COMMAND CENTER ============ -->

<h1 align="center">
  <code>&lt; Cuma Doğan / System Architect &gt;</code>
</h1>

<p align="center">
  <em>Kutu çizmiyorum — sistem akışı tasarlıyorum.</em><br/>
  <sub>AI Engineering · Distributed Systems · Real-Time Data Pipelines</sub>
</p>

<!-- LIVE DATA FLOW HEADER -->
<p align="center">
  <img src="./assets/data-flow.svg?v=1" width="100%" alt="Live system data flow — GraphQL → ML Engine → Kafka"/>
</p>

---

## 🧭 System Command Center

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    subgraph CLIENT["🖥️ Edge / Client"]
        A[Next.js App]
    end
    subgraph GATEWAY["⚡ API Mesh"]
        B{{GraphQL Gateway}}
        C[[Auth / Rate-Limit]]
    end
    subgraph CORE["🧠 Intelligence Layer"]
        D[ML Inference Engine]
        E[(Vector Store)]
    end
    subgraph DATA["💾 State & Streams"]
        F[(PostgreSQL)]
        G>Kafka Event Bus]
    end
    A -->|GraphQL| B
    B --> C
    C -->|gRPC| D
    D <-->|embeddings| E
    D -->|infer result| G
    G -->|persist| F
    B -.->|cache read| F
    classDef edge fill:#0B0E14,stroke:#38BDF8,color:#38BDF8;
    classDef ai fill:#0B0E14,stroke:#A78BFA,color:#A78BFA;
    classDef data fill:#0B0E14,stroke:#FBBF24,color:#FBBF24;
    class A,B,C edge;
    class D,E ai;
    class F,G data;
```

---

## 🛰️ Project Pods

<table>
<tr>
<td width="50%" valign="top">

### 🧠 NeuroScan · Medical Imaging AI
<img src="./assets/pod-medical.svg?v=1" width="100%" alt="NeuroScan architecture"/>

**Flow:** `DICOM → Flask → TensorFlow CNN → Grad-CAM`

<sub>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-000?style=flat-square&logo=flask"/>
<img src="https://img.shields.io/badge/Next.js-000?style=flat-square&logo=nextdotjs"/>
</sub>
<br/>
<sub>⚡ 94% accuracy · 120ms inference · Grad-CAM explainability</sub>

</td>
<td width="50%" valign="top">

### 📈 QuantForge · Algo Trading Engine
<img src="./assets/pod-trading.svg?v=1" width="100%" alt="QuantForge architecture"/>

**Flow:** `Market Feed → C++ Ingestor → Python Signals → MQL5 Exec`

<sub>
<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/MQL5-2E8B57?style=flat-square"/>
</sub>
<br/>
<sub>⚡ sub-ms tick processing · risk-gated execution · backtested</sub>

</td>
</tr>
</table>

---

## ⚙️ Capability Reactors

<table>
<tr>
<td width="50%" align="center" valign="top">
<sub><b>System Efficiency</b></sub><br/>
<img src="./assets/complexity.svg?v=1" width="90%" alt="O(n) optimized to O(log n)"/>
</td>
<td width="50%" align="center" valign="top">
<sub><b>Cloud Autoscaling</b></sub><br/>
<img src="./assets/k8s-scale.svg?v=1" width="90%" alt="Kubernetes pods autoscaling"/>
</td>
</tr>
</table>

---

## 🛠️ Workspace Architecture

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    subgraph WS["⌨️ Workspace"]
        OS[Windows 11 + WSL2]
        ED[VS Code · Neovim]
    end
    subgraph LOCAL["🐳 Local Cluster"]
        DK[Docker Desktop]
        K8[Minikube]
    end
    subgraph CLOUD["☁️ Targets"]
        AWS[AWS / GCP]
    end
    ED --> OS --> DK --> K8 -.deploy.-> AWS
    classDef d fill:#0B0E14,stroke:#38BDF8,color:#E2E8F0;
    class OS,ED,DK,K8,AWS d;
```

---

## 📡 Telemetry · Hologram Panels

<table>
<tr>
<td>
<img src="https://github-readme-stats.vercel.app/api?username=CumaDogangithub&show_icons=true&hide_border=true&bg_color=0B0E14&title_color=38BDF8&icon_color=A78BFA&text_color=E2E8F0"/>
</td>
<td>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=CumaDogangithub&hide_border=true&background=0B0E14&stroke=1E293B&ring=38BDF8&fire=FBBF24&currStreakLabel=38BDF8"/>
</td>
</tr>
</table>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=CumaDogangithub&bg_color=0B0E14&color=38BDF8&line=A78BFA&point=FBBF24&hide_border=true&area=true" width="100%"/>

<p align="center">
  <sub>// Projects are not isolated — they are nodes of the same engineering philosophy.</sub>
</p>
