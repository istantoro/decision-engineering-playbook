# Memahami AI Secara Sistemik

Dokumen ini merangkum peta besar Artificial Intelligence (AI) dari sudut pandang AI Engineer. Fokusnya adalah membedakan dan menghubungkan lima lapisan utama:

1. Metode
2. Domain
3. Architecture
4. Aplikasi
5. Produk

Tujuannya agar AI tidak dipahami hanya sebagai ChatGPT, tetapi sebagai sistem teknologi yang luas dan saling terhubung.

---

## 1. Peta Besar AI

Secara sederhana:

> AI adalah upaya membuat mesin mampu melakukan tugas yang biasanya membutuhkan kecerdasan manusia: memahami, memprediksi, mengambil keputusan, membuat konten, bergerak, dan berinteraksi.

Struktur besar AI dapat dibaca seperti berikut:

```text
Artificial Intelligence
│
├── Metode
│   ├── Rule-based AI
│   ├── Machine Learning
│   ├── Deep Learning
│   ├── Reinforcement Learning
│   ├── Generative AI
│   └── Agentic AI
│
├── Domain Masalah
│   ├── Bahasa
│   ├── Gambar / Video
│   ├── Suara
│   ├── Data Tabular
│   ├── Rekomendasi
│   ├── Robotik
│   ├── Knowledge / Reasoning
│   └── Decision Intelligence
│
├── Architecture
│   ├── Transformer
│   ├── CNN
│   ├── RNN / LSTM
│   ├── Diffusion Model
│   ├── Graph Neural Network
│   ├── Retrieval-Augmented Generation
│   └── AI Agent Architecture
│
├── Aplikasi
│   ├── Chatbot
│   ├── Forecasting
│   ├── Fraud Detection
│   ├── Document Analysis
│   ├── Image Recognition
│   ├── Voice Assistant
│   ├── Recommendation System
│   ├── Automation
│   └── Decision Support
│
└── Produk
    ├── ChatGPT
    ├── Claude
    ├── Gemini
    ├── Copilot
    ├── Perplexity
    ├── Midjourney
    ├── Azure AI
    ├── AWS AI
    ├── Vertex AI
    └── OpenAI API
```

---

## 2. Bedakan Dulu: Metode, Domain, Architecture, Aplikasi, Produk

Banyak orang mencampur istilah AI. Padahal, masing-masing punya posisi berbeda.

| Istilah | Artinya | Contoh |
|---|---|---|
| Metode | Cara AI belajar atau bekerja | Machine Learning, Deep Learning, Reinforcement Learning |
| Domain | Area masalah yang ditangani AI | Bahasa, gambar, suara, data keuangan |
| Architecture | Bentuk teknis model di dalam AI | Transformer, CNN, Diffusion, RAG |
| Aplikasi | Penggunaan AI untuk tugas tertentu | Chatbot, forecasting, fraud detection |
| Produk | Tools/platform yang dipakai user | ChatGPT, Claude, Gemini, Copilot |

Contoh:

> ChatGPT bukan metode.  
> ChatGPT adalah produk.  
> Di dalamnya ada model berbasis Transformer architecture.  
> Modelnya bekerja di domain NLP / bahasa.  
> Metodenya masuk ke Deep Learning / Generative AI.  
> Aplikasinya adalah chatbot, writing assistant, coding assistant, dan reasoning assistant.

---

## 3. Metode AI

### A. Rule-Based AI

Rule-Based AI adalah AI yang bekerja berdasarkan aturan eksplisit yang dibuat manusia.

Contoh logika:

```text
Jika umur > 60 dan tekanan darah tinggi,
maka risiko kesehatan = tinggi.
```

| Aspek | Penjelasan |
|---|---|
| Cara kerja | Mengikuti aturan manusia |
| Butuh data besar? | Tidak selalu |
| Bisa belajar sendiri? | Tidak |
| Kelebihan | Mudah dijelaskan |
| Kelemahan | Kaku, sulit menangani kasus kompleks |

Contoh aplikasi:

- Expert system
- Aturan kredit sederhana
- Sistem validasi dokumen
- Rule engine di proses bisnis

---

### B. Machine Learning

Machine Learning adalah bagian dari AI yang membuat sistem belajar dari data, bukan hanya mengikuti aturan manual.

Contoh:

```text
Data historis pelanggan
→ model belajar pola
→ prediksi pelanggan mana yang berisiko churn
```

Jenis utama Machine Learning:

| Jenis ML | Fungsi | Contoh |
|---|---|---|
| Supervised Learning | Belajar dari data yang sudah punya jawaban | Prediksi penjualan, credit scoring |
| Unsupervised Learning | Mencari pola tanpa label jawaban | Customer segmentation |
| Semi-Supervised Learning | Gabungan data berlabel dan tidak berlabel | Klasifikasi dokumen |
| Self-Supervised Learning | Model membuat tugas belajar dari data itu sendiri | Training LLM |
| Reinforcement Learning | Belajar dari reward/punishment | Game AI, robotik, agent optimization |

---

### C. Deep Learning

Deep Learning adalah bagian dari Machine Learning yang memakai neural network berlapis-lapis.

```text
AI
└── Machine Learning
    └── Deep Learning
```

Deep Learning kuat untuk data kompleks seperti:

- Teks
- Gambar
- Suara
- Video
- Bahasa manusia
- Pola besar yang sulit dibuat manual

| Tugas | Deep Learning digunakan untuk |
|---|---|
| Gambar | Mendeteksi wajah, objek, kanker dari citra medis |
| Bahasa | Memahami teks, menerjemahkan, menjawab pertanyaan |
| Suara | Speech-to-text, text-to-speech |
| Video | Object tracking, activity recognition |

---

### D. Reinforcement Learning

Reinforcement Learning adalah metode AI yang belajar melalui aksi dan umpan balik.

Strukturnya:

```text
Agent
→ melakukan aksi
→ lingkungan memberi reward
→ agent belajar strategi lebih baik
```

Contoh:

- AI bermain catur
- Robot belajar berjalan
- Sistem rekomendasi yang belajar dari respons user
- Optimization engine
- Autonomous driving

---

### E. Generative AI

Generative AI adalah AI yang dapat membuat output baru.

Contoh output:

- Teks
- Gambar
- Suara
- Video
- Kode
- Desain
- Dokumen

Contoh produk:

- ChatGPT untuk teks, reasoning, coding
- Midjourney untuk gambar
- Runway untuk video
- Suno untuk musik
- GitHub Copilot untuk coding

---

### F. Agentic AI

Agentic AI adalah AI yang tidak hanya menjawab, tetapi bisa menjalankan alur kerja.

Strukturnya:

```text
Goal
→ planning
→ tool use
→ execution
→ checking
→ revision
→ final output
```

Contoh:

- AI agent membaca email, menyusun draft, dan mengatur jadwal
- Coding agent membaca repo, memperbaiki file, menjalankan test
- Finance agent mengambil data, menganalisis variance, lalu membuat management report

---

## 4. Domain AI

Domain adalah jenis masalah yang ditangani AI.

---

### A. Natural Language Processing

Natural Language Processing atau NLP adalah AI untuk memahami dan menghasilkan bahasa manusia.

Contoh tugas NLP:

| Tugas | Contoh |
|---|---|
| Text classification | Klasifikasi email komplain |
| Summarization | Meringkas laporan |
| Translation | Terjemahan bahasa |
| Question answering | Menjawab pertanyaan dari dokumen |
| Sentiment analysis | Membaca sentimen pelanggan |
| Information extraction | Mengambil angka penting dari kontrak |
| Text generation | Membuat artikel, email, memo |

Produk:

- ChatGPT
- Claude
- Gemini
- DeepL
- Grammarly
- Notion AI

---

### B. Computer Vision

Computer Vision adalah AI untuk memahami gambar dan video.

Contoh tugas:

| Tugas | Contoh |
|---|---|
| Image classification | Membedakan kucing vs anjing |
| Object detection | Mendeteksi mobil di jalan |
| Face recognition | Verifikasi wajah |
| OCR | Membaca teks dari gambar |
| Medical imaging | Deteksi tumor dari scan |
| Video analytics | Mendeteksi aktivitas di CCTV |

Produk:

- Google Vision AI
- Azure Computer Vision
- AWS Rekognition
- YOLO-based systems
- OpenCV

---

### C. Speech / Audio AI

Domain ini menangani suara.

Contoh tugas:

| Tugas | Contoh |
|---|---|
| Speech-to-text | Transkrip meeting |
| Text-to-speech | Suara sintetis |
| Speaker recognition | Identifikasi pembicara |
| Voice command | Perintah suara |
| Real-time translation | Terjemahan langsung |

Produk:

- Whisper
- ElevenLabs
- Google Speech-to-Text
- Azure Speech
- Amazon Transcribe

---

### D. Tabular AI / Predictive Analytics

Ini domain yang sangat dekat dengan finance, business, dan operations.

Data bentuknya tabel:

```text
tanggal | revenue | cost | customer | region | margin | aging piutang
```

Contoh tugas:

| Tugas | Contoh |
|---|---|
| Forecasting | Prediksi revenue bulan depan |
| Classification | Risiko gagal bayar |
| Regression | Prediksi nilai penjualan |
| Anomaly detection | Mendeteksi transaksi tidak wajar |
| Optimization | Alokasi budget terbaik |
| Driver analysis | Mencari penyebab perubahan laba |

Produk:

- DataRobot
- H2O.ai
- BigQuery ML
- Azure Machine Learning
- Amazon SageMaker
- Vertex AI

---

### E. Recommendation System

AI untuk memberi rekomendasi.

| Industri | Rekomendasi |
|---|---|
| E-commerce | Produk yang mungkin dibeli |
| Streaming | Film/musik yang relevan |
| Banking | Produk finansial yang sesuai |
| HR | Kandidat yang cocok |
| Learning | Materi belajar berikutnya |

Produk/sistem:

- Netflix recommendation
- YouTube recommendation
- Spotify recommendation
- Amazon recommendation
- TikTok feed ranking

---

### F. Robotics & Autonomous Systems

AI yang berhubungan dengan mesin fisik.

Contoh:

- Robot gudang
- Autonomous vehicle
- Drone
- Robot medis
- Robot manufaktur
- Smart warehouse

Domain ini biasanya menggabungkan:

```text
Computer Vision
+ Reinforcement Learning
+ Sensor Fusion
+ Control System
```

---

### G. Knowledge, Reasoning, and Decision Intelligence

Domain ini penting untuk bisnis karena fokusnya bukan hanya prediksi, tetapi membantu keputusan.

| Area | Contoh |
|---|---|
| Knowledge AI | Menjawab dari dokumen internal |
| Reasoning AI | Menyusun logika analisis |
| Decision Intelligence | Menghubungkan data, insight, dan keputusan |
| Planning AI | Menyusun langkah aksi |
| Simulation AI | Membuat skenario dan sensitivitas |

Untuk konteks finance:

```text
Data laporan keuangan
→ variance analysis
→ driver analysis
→ business explanation
→ management narrative
→ decision recommendation
```

---

## 5. Architecture AI

Architecture adalah bentuk teknis model atau sistem.

---

### A. Neural Network

Neural Network adalah fondasi deep learning.

Struktur sederhana:

```text
Input
→ hidden layers
→ output
```

Dipakai untuk:

- Prediksi
- Klasifikasi
- Pattern recognition
- Language model
- Image model

---

### B. CNN — Convolutional Neural Network

CNN banyak digunakan untuk gambar.

Kuat untuk:

- Image classification
- Object detection
- Medical imaging
- Visual inspection
- Face detection

Struktur sederhana:

```text
Image
→ feature extraction
→ pattern detection
→ classification
```

---

### C. RNN / LSTM / GRU

Architecture lama untuk data berurutan.

Dipakai untuk:

- Time series
- Teks
- Suara
- Sequence prediction

Sekarang banyak digantikan Transformer, tetapi konsep sequence-nya tetap penting.

---

### D. Transformer

Transformer adalah architecture penting di balik banyak LLM modern.

Kuat karena bisa membaca hubungan antar kata/token dalam konteks panjang.

Dipakai untuk:

- LLM
- Translation
- Summarization
- Chatbot
- Coding assistant
- Multimodal AI

Contoh model berbasis Transformer:

- GPT
- Claude
- Gemini
- Llama
- Mistral

---

### E. Diffusion Model

Diffusion banyak dipakai untuk generative image dan video.

Cara berpikirnya:

```text
Noise
→ model belajar mengurangi noise
→ gambar terbentuk
```

Dipakai untuk:

- Image generation
- Image editing
- Video generation
- Design generation

Produk:

- Midjourney
- Stable Diffusion
- DALL·E
- Adobe Firefly
- Runway

---

### F. Graph Neural Network

Graph Neural Network atau GNN dipakai untuk data yang bentuknya jaringan/relasi.

| Domain | Relasi |
|---|---|
| Fraud detection | Hubungan antar akun |
| Supply chain | Hubungan pemasok dan distributor |
| Social network | Hubungan antar user |
| Molecule discovery | Hubungan antar atom |
| Knowledge graph | Hubungan antar konsep |

---

### G. RAG — Retrieval-Augmented Generation

RAG bukan model tunggal, tetapi arsitektur sistem.

Fungsinya adalah membuat LLM menjawab berdasarkan dokumen/data tertentu.

Struktur:

```text
User question
→ cari dokumen relevan
→ ambil konteks
→ kirim ke LLM
→ jawab berdasarkan konteks
```

Dipakai untuk:

- Chatbot perusahaan
- Tanya jawab dokumen
- Knowledge management
- Legal assistant
- Finance report assistant
- Policy assistant

---

### H. AI Agent Architecture

AI agent biasanya punya komponen:

```text
Goal
→ planner
→ memory
→ tools
→ executor
→ evaluator
→ final answer/action
```

Contoh tools:

- Database query
- Spreadsheet reader
- Email sender
- Calendar access
- Web search
- Code executor
- API connector

Ini yang membuat AI mulai bergeser dari answer engine menjadi work execution system.

---

## 6. Aplikasi AI

Aplikasi adalah penggunaan AI untuk menyelesaikan pekerjaan nyata.

---

### A. Chatbot dan Assistant

Contoh:

- Customer service bot
- Internal knowledge assistant
- HR assistant
- Finance assistant
- Legal assistant

Nilai bisnis:

- Mengurangi pertanyaan berulang
- Mempercepat akses informasi
- Membantu drafting
- Membantu analisis awal

---

### B. Forecasting

Contoh:

- Revenue forecasting
- Demand forecasting
- Cash flow forecasting
- Sales forecasting
- Workload forecasting

Metode yang bisa dipakai:

- Regression
- Time series model
- Machine learning
- Deep learning
- Hybrid forecasting

---

### C. Fraud Detection

Contoh:

- Transaksi tidak wajar
- Klaim palsu
- Pola pembayaran aneh
- Manipulasi data
- Anomali vendor

Metode:

- Anomaly detection
- Graph analysis
- Classification model
- Rules + ML hybrid

---

### D. Document Intelligence

AI membaca dokumen.

Contoh:

- Invoice
- Kontrak
- Laporan keuangan
- Memo internal
- Notulen rapat
- Regulasi
- Dokumen legal

Kemampuan:

```text
OCR
→ extraction
→ classification
→ validation
→ summary
→ recommendation
```

---

### E. Recommendation System

Contoh:

- Rekomendasi produk
- Rekomendasi konten
- Next best action
- Next best offer
- Kandidat terbaik
- Materi belajar berikutnya

---

### F. Image and Video Analytics

Contoh:

- Quality control di pabrik
- CCTV analytics
- Medical image analysis
- Inventory detection
- Facial verification
- Damage assessment

---

### G. Coding and Software Engineering

Contoh:

- Code generation
- Bug fixing
- Test generation
- Code review
- Documentation
- Repo analysis
- Deployment assistant

Produk:

- GitHub Copilot
- Claude Code
- Cursor
- Replit AI
- OpenAI Codex-style coding tools

---

### H. Finance and Decision Support

Contoh paling relevan untuk finance:

| Kebutuhan Finance | AI Use Case |
|---|---|
| Management reporting | Automated report generation |
| Variance analysis | Mencari penyebab perubahan angka |
| Forecasting | Prediksi revenue, cost, cash flow |
| Working capital | Analisis DSO, aging, liquidity |
| Scenario analysis | Simulasi best/base/worst case |
| Driver analysis | Menghubungkan angka ke penyebab bisnis |
| Narrative reporting | Membuat cerita eksekutif dari data |
| Risk detection | Mendeteksi anomali transaksi atau piutang |

Pola sistemnya:

```text
Financial data
→ clean data
→ calculate metrics
→ detect variance
→ identify drivers
→ generate insight
→ recommend action
→ compose report
```

---

## 7. Produk AI

Produk adalah alat yang dipakai user atau developer.

---

### A. General AI Assistant

| Produk | Fungsi utama |
|---|---|
| ChatGPT | General assistant, reasoning, coding, writing, analysis |
| Claude | Reasoning, writing, coding, long context |
| Gemini | Google ecosystem, multimodal, search/workspace integration |
| Copilot | Microsoft Office, coding, productivity |
| Perplexity | AI search and research |

---

### B. Developer Platform

| Platform | Fungsi |
|---|---|
| OpenAI API | Membangun aplikasi AI berbasis model OpenAI |
| Anthropic API | Membangun aplikasi dengan Claude |
| Google Vertex AI | Membangun, deploy, dan scale model ML/GenAI |
| Azure AI Foundry | Membangun aplikasi dan agent AI enterprise |
| AWS Bedrock | Membangun aplikasi GenAI dengan berbagai foundation model |

---

### C. Image / Video Generation

| Produk | Fungsi |
|---|---|
| Midjourney | Image generation |
| Stable Diffusion | Open-source image generation |
| DALL·E | Image generation/editing |
| Adobe Firefly | Creative generation |
| Runway | Video generation/editing |
| Pika | Video generation |

---

### D. Coding AI

| Produk | Fungsi |
|---|---|
| GitHub Copilot | Coding assistant |
| Cursor | AI code editor |
| Claude Code | Agentic coding |
| Replit AI | Coding in browser |
| Codeium/Windsurf | AI coding workflow |

---

### E. Enterprise AI / Business AI

| Produk | Fungsi |
|---|---|
| Microsoft Copilot | Office productivity |
| Salesforce Einstein | CRM AI |
| ServiceNow AI | Workflow automation |
| SAP Joule | ERP AI |
| Workday AI | HR and finance AI |
| Databricks Mosaic AI | Data + AI platform |
| Snowflake Cortex AI | AI in data cloud |

---

## 8. Hirarki Lengkap AI

```text
AI
│
├── Symbolic AI
│   ├── Rule-based system
│   ├── Expert system
│   └── Knowledge graph
│
├── Machine Learning
│   ├── Supervised Learning
│   │   ├── Regression
│   │   └── Classification
│   │
│   ├── Unsupervised Learning
│   │   ├── Clustering
│   │   ├── Dimensionality reduction
│   │   └── Anomaly detection
│   │
│   ├── Semi-supervised Learning
│   ├── Self-supervised Learning
│   └── Reinforcement Learning
│
├── Deep Learning
│   ├── CNN
│   ├── RNN / LSTM
│   ├── Transformer
│   ├── Autoencoder
│   ├── GAN
│   ├── Diffusion Model
│   └── Graph Neural Network
│
├── Generative AI
│   ├── Text generation
│   ├── Image generation
│   ├── Audio generation
│   ├── Video generation
│   ├── Code generation
│   └── Multimodal generation
│
├── Foundation Models
│   ├── LLM
│   ├── Vision-language model
│   ├── Speech model
│   ├── Multimodal model
│   └── Embedding model
│
└── Agentic AI
    ├── Tool-using agent
    ├── Workflow agent
    ├── Multi-agent system
    ├── Autonomous coding agent
    └── Business process agent
```

---

## 9. Posisi Istilah-Istilah Populer

| Istilah | Masuk kategori apa? |
|---|---|
| AI | Payung besar |
| Machine Learning | Metode di bawah AI |
| Deep Learning | Metode di bawah ML |
| NLP | Domain AI untuk bahasa |
| Computer Vision | Domain AI untuk gambar/video |
| LLM | Foundation model untuk bahasa |
| Transformer | Architecture |
| GPT | Keluarga model |
| ChatGPT | Produk |
| RAG | Architecture aplikasi |
| AI Agent | Architecture/workflow system |
| Copilot | Produk/aplikasi assistant |
| Generative AI | Pendekatan AI yang menghasilkan konten baru |
| Predictive AI | AI untuk prediksi |
| Recommendation System | Aplikasi/domain |
| Robotics | Domain/aplikasi fisik |

---

## 10. Peta dari Teknologi ke Produk

### Contoh 1: ChatGPT

```text
Produk: ChatGPT
Aplikasi: conversational assistant
Domain: NLP, reasoning, coding, multimodal
Architecture: Transformer-based LLM
Metode: Deep Learning, Generative AI, instruction tuning
```

### Contoh 2: Midjourney

```text
Produk: Midjourney
Aplikasi: image generation
Domain: Computer Vision / Generative Image
Architecture: Diffusion-like generative architecture
Metode: Deep Learning, Generative AI
```

### Contoh 3: Fraud Detection Bank

```text
Produk: internal fraud system
Aplikasi: fraud detection
Domain: tabular data, transaction analytics
Architecture: tree model / neural network / graph model
Metode: supervised learning, anomaly detection
```

### Contoh 4: Finance Management Report Agent

```text
Produk: internal finance AI assistant
Aplikasi: automated management reporting
Domain: finance, tabular data, document intelligence
Architecture: RAG + LLM + tool-using agent
Metode: ML, LLM, rule-based calculation, generative AI
```

---

## 11. Cara Memahami AI Secara Sistemik

Gunakan 5 pertanyaan ini setiap melihat teknologi AI baru.

### 1. Ini menyelesaikan masalah apa?

Contoh:

- Memprediksi?
- Mengklasifikasi?
- Memahami bahasa?
- Membaca gambar?
- Membuat konten?
- Mengambil keputusan?
- Menjalankan workflow?

### 2. Domain datanya apa?

Contoh:

- Teks
- Angka/tabel
- Gambar
- Suara
- Video
- Dokumen
- Sensor
- Transaksi

### 3. Metode yang dipakai apa?

Contoh:

- Rule-based
- Machine Learning
- Deep Learning
- Reinforcement Learning
- Generative AI
- Agentic AI

### 4. Architecture-nya apa?

Contoh:

- Transformer
- CNN
- Diffusion
- Graph Neural Network
- RAG
- Agent workflow

### 5. Bentuk produknya apa?

Contoh:

- Chatbot
- Dashboard
- API
- Copilot
- Automation tool
- Decision support system
- Enterprise platform

---

## 12. Ringkasan Paling Penting

```text
AI = payung besar kecerdasan mesin

Machine Learning = AI yang belajar dari data

Deep Learning = ML dengan neural network besar

NLP = domain bahasa

Computer Vision = domain gambar/video

LLM = model besar untuk bahasa dan reasoning

Transformer = architecture utama LLM modern

Generative AI = AI yang membuat output baru

RAG = cara menghubungkan LLM dengan dokumen/data

AI Agent = AI yang bisa merencanakan, memakai tools, dan menjalankan workflow

Produk = ChatGPT, Claude, Gemini, Copilot, Vertex AI, Azure AI, AWS AI
```

Bagian paling penting untuk seorang AI Engineer bukan sekadar hafal istilah, tetapi bisa memetakan:

```text
Business problem
→ data domain
→ AI method
→ model architecture
→ application design
→ product implementation
→ business impact
```

Untuk konteks bisnis dan finance, nilai AI paling besar bukan hanya membuat jawaban, tetapi mengubah alur kerja:

```text
manual reporting
→ automated analysis
→ structured insight
→ decision recommendation
→ action monitoring
```

---

## 13. Catatan untuk Repository GitHub

Rekomendasi nama file:

```text
memahami-ai-secara-sistemik.md
```

Rekomendasi struktur folder:

```text
ai-learning-notes/
│
├── README.md
└── memahami-ai-secara-sistemik.md
```

Rekomendasi deskripsi repository:

> Catatan belajar sistemik tentang Artificial Intelligence, mencakup metode, domain, arsitektur, aplikasi, dan produk AI agar mudah dipahami dari fondasi hingga implementasi praktis.

---

## 14. One-Line Summary

> AI perlu dipahami sebagai sistem berlapis: dimulai dari masalah bisnis, jenis data, metode pembelajaran, arsitektur model, aplikasi nyata, lalu dikemas menjadi produk yang memberi dampak.
