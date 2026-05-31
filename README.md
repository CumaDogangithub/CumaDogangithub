<!-- ============ LIVED-IN BLUEPRINT ============ -->

<h1 align="center">Cuma Doğan</h1>

<p align="center">
  Yapay zekâ, dağıtık sistemler ve veri hatları üzerine çalışıyorum.<br/>
  <sub>Projelerimi uçtan uca kuruyorum — modelden arayüze, container'dan deploy'a kadar.</sub>
</p>

<p align="center">
  <img src="./assets/data-flow.svg?v=2" width="100%" alt="Tipik mimari iskeletim: Next.js → API → AI modeli → veritabanı"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000?style=flat-square&logo=nextdotjs"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-000?style=flat-square&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
</p>

---

## Öne çıkan projeler

Aşağıdaki üçü, kendi projelerimden mimari olarak en çok uğraştıklarım. Her birinin küçük, hareketli akış şeması yanında.

<table>
<tr>
<td valign="top">

### 🩺 Akıllı Tıbbi Görüntü Analiz Sistemi
<img src="./assets/pod-medical.svg?v=2" width="100%" alt="Tıbbi görüntü analiz akışı"/>

CT, MR ve röntgen görüntülerini EfficientNetV2-M tabanlı bir modelle işleyip hekime ön tanı desteği veren platform. DICOM ön işleme hattı, rol bazlı erişim (doktor / radyolog / akademisyen) ve Cloudflare → Nginx → Docker → Flask şeklinde konumlandırılmış bir servis katmanı içeriyor.

<sub>Python · TensorFlow/Keras · Flask · OpenCV · Supabase · Docker</sub>

</td>
</tr>
<tr>
<td valign="top">

### 🧪 StandAi — Sentetik Tüketici Paneli
<img src="./assets/pod-stand.svg?v=2" width="100%" alt="Sentetik tüketici paneli akışı"/>

Bir reklam ya da ürün metnini, TÜİK demografisine göre katmanlı örneklenmiş ~1000 sentetik persona üzerinde test eden B2B araç. Celery + Redis ile kuyruğa alınan istekler Gemini Flash'a toplu (10 persona/çağrı) gidiyor; sonuçlar pgvector (768D) ile anlamsal olarak kümeleniyor. Tam bir test ~12 dakikada tamamlanıyor.

<sub>Next.js · FastAPI · Celery/Redis · pgvector · Google Generative AI · Docker Compose</sub>

</td>
</tr>
<tr>
<td valign="top">

### 🛡️ textSansür — Yerel KVKK Maskeleme
<img src="./assets/pod-censor.svg?v=2" width="100%" alt="Yerel KVKK maskeleme akışı"/>

Metin ve görsellerdeki kişisel veriyi tamamen yerelde — buluta hiçbir şey göndermeden — maskeleyen araç. Ollama üzerinde qwen2.5:14b bağlamı çözüyor (örn. mağdurun adını maskeler, dolandırıcınınkini bırakır), EasyOCR görseldeki metni yakalıyor, tarayıcıdaki canvas editöründe blur/pixel/bant uygulanıyor.

<sub>Python · Ollama (qwen2.5) · EasyOCR · Flask · Docker · %0 bulut transferi</sub>

</td>
</tr>
</table>

---

## Diğer çalıştıklarım

| Proje | Ne yapıyor | Yığın |
|---|---|---|
| **myHackBot** | Komut allowlist'i ve enjeksiyon korumasıyla çalışan, araç çağıran etik (white-hat) güvenlik asistanı | Python · Ollama · Tkinter · faster-whisper |
| **claude_sohbet** | SIR/SEIR modeliyle salgın yayılımını simüle eden ve canlı grafikleyen panel | Next.js · FastAPI · Recharts |
| **screenEnergy** | Çok monitörlü kurulumlarda poz tespitine göre ekran/enerji yönetimi | Python · MediaPipe · OpenCV |
| **akaryakit-listeleme** | Türkiye akaryakıt fiyatlarını harita üzerinde karşılaştıran MVP | Next.js 14 · Leaflet · Tailwind |
| **FIRATHUB2** | Üniversite içi akademisyen–öğrenci eşleştirme ve işbirliği platformu | Web · AI öneri |

---

## Nasıl çalışıyorum

Tek bir desen üç projede de tekrar ediyor: ince bir arayüz, işi yapan bir API katmanı, arkada bir model (yerel ya da bulut) ve durumun yaşadığı bir veritabanı. Çoğunu Docker'la paketleyip kendi sunucuma alıyorum.

```mermaid
%%{init: {'theme':'dark'}}%%
flowchart LR
    subgraph WS["Geliştirme"]
        OS[Windows 11 + WSL2]
        ED[VS Code]
    end
    subgraph LOCAL["Yerel"]
        DK[Docker]
        ML[Ollama / TF]
    end
    subgraph CLOUD["Dağıtım"]
        SRV[Nginx + Cloudflare]
    end
    ED --> OS --> DK
    DK --> ML
    DK -.deploy.-> SRV
    classDef d fill:#0B0E14,stroke:#38BDF8,color:#E2E8F0;
    class OS,ED,DK,ML,SRV d;
```

---

<table>
<tr>
<td>
<img src="https://github-readme-stats.vercel.app/api?username=CumaDogangithub&show_icons=true&hide_border=true&bg_color=0B0E14&title_color=38BDF8&icon_color=A78BFA&text_color=E2E8F0"/>
</td>
<td>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=CumaDogangithub&layout=compact&hide_border=true&bg_color=0B0E14&title_color=38BDF8&text_color=E2E8F0"/>
</td>
</tr>
</table>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=CumaDogangithub&bg_color=0B0E14&color=38BDF8&line=A78BFA&point=FBBF24&hide_border=true&area=true" width="100%"/>
