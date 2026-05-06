# Mengatasi Batas Context Window: Dari Chatbot ke Sistem yang Bisa “Berpikir Berkelanjutan”

## 1. Problem Framing

Banyak implementasi AI gagal bukan karena modelnya lemah, tapi karena **tidak mampu menjaga konteks**.

Di use case nyata:
- analisis berjalan multi-step  
- keputusan butuh referensi historis  
- proses tidak selesai dalam satu prompt  

Namun LLM bekerja seperti “memori jangka pendek”.  
Saat konteks penuh → informasi lama hilang → keputusan jadi tidak konsisten.

**Masalah utamanya bukan AI tidak pintar.  
Masalahnya: AI tidak “ingat”.**

---

## 2. Apa yang Berubah

Kita sedang bergerak dari:
- chatbot → menjawab  
- menjadi agen → menyelesaikan tugas  

Perbedaannya fundamental:

| Chatbot | Agen Otonom |
|--------|-------------|
| 1x input → 1x output | Multi-step loop |
| Stateless | Stateful |
| Reaktif | Proaktif |
| Fokus jawaban | Fokus outcome |

Implikasinya:
→ AI tidak lagi cukup “menjawab benar”  
→ AI harus **menyelesaikan proses sampai tuntas**

Di sinilah muncul bottleneck: **context window**

---

## 3. Core Insight

Selama ini fokusnya:
> “Bagaimana memperbesar context window?”

Pendekatan ini mahal dan tidak scalable.

Perubahan cara berpikir yang lebih relevan:
> **Bukan memperbesar memori, tapi mengelola memori**

Inilah yang disebut:
### → Context Engineering

---

## 4. Breakdown: Cara Kerja Agen (Simplified)

Agen bekerja dalam loop:

1. Perceive → menerima input  
2. Reason → memahami situasi  
3. Plan → memecah tugas  
4. Act → menjalankan aksi  
5. Observe → melihat hasil  

Loop ini terus berulang sampai tujuan tercapai.

Masalahnya:
- setiap loop menambah konteks  
- konteks makin panjang  
- kualitas reasoning menurun  

Tanpa manajemen memori:
→ agen kehilangan arah

---

## 5. Solusi: Dua Layer Memori

### A. Short-Term Memory (Working Memory)

Fungsi:
- menjaga konteks selama proses berjalan

Teknik utama:
- **Sliding window** → hanya simpan konteks terbaru  
- **Summarization** → ringkas iterasi sebelumnya  
- **State tracking** → simpan status penting saja  

Prinsip:
> tidak semua informasi harus disimpan, hanya yang relevan untuk langkah berikutnya

---

### B. Long-Term Memory (Persistent Memory)

Fungsi:
- menyimpan pengetahuan di luar sesi aktif

Implementasi umum:
- **RAG (Retrieval-Augmented Generation)**
- **Vector Database**

Perbedaan penting:

| Traditional DB | Vector DB |
|---------------|----------|
| Exact match | Semantic search |
| Structured | Unstructured |
| SQL query | Similarity search |

Implikasi:
→ AI tidak perlu “ingat semua”  
→ cukup **tahu cara mencari kembali**

---

## 6. Application (Use Case Finance)

Bayangkan use case sederhana:

**Analisis kinerja cabang (multi-step):**
1. tarik data performa  
2. identifikasi anomali  
3. bandingkan historis  
4. generate insight  
5. rekomendasi aksi  

Tanpa context engineering:
- tiap step berdiri sendiri  
- insight tidak nyambung  
- rekomendasi bias  

Dengan context engineering:
- short-term memory → menjaga alur analisis  
- long-term memory → tarik histori relevan  

Hasilnya:
→ bukan sekadar “analisis cepat”  
→ tapi **analisis yang konsisten dan bisa dipakai ambil keputusan**

---

## 7. Real Constraint (Production Reality)

Masalah nyata bukan hanya teknis, tapi ekonomi:

- agent loop = token 4–15x lebih besar  
- tanpa kontrol → biaya meledak  
- risiko “runaway loop” (loop tanpa akhir)

Yang harus dikontrol:

**1. Iteration limit**  
→ batasi jumlah loop  

**2. No-progress detection**  
→ stop jika tidak ada insight baru  

**3. Budget per task**  
→ kontrol biaya per proses  

**4. Observability (logging)**  
→ semua step harus bisa dilacak  

Tanpa ini:
→ sistem tidak bisa di-debug  
→ tidak bisa dipercaya  

---

## 8. Action: Apa yang Perlu Diubah

Jika kamu membangun atau menggunakan AI:

### Stop:
- hanya fokus ke prompt  
- mengandalkan satu kali response  
- menganggap AI = chatbot  

### Start:
- desain proses, bukan hanya output  
- pisahkan short vs long-term memory  
- pikirkan cost sejak awal  

### Rethink:
> AI bukan alat jawab  
> tapi sistem untuk menyelesaikan masalah

---

## 9. Key Takeaways

- Context window adalah bottleneck utama di sistem AI nyata  
- Solusinya bukan scale up, tapi **design better memory**  
- Short-term memory menjaga alur berpikir  
- Long-term memory menjaga relevansi pengetahuan  
- Nilai AI bergeser:  
  → dari “jawaban benar”  
  → ke “proses yang menghasilkan keputusan”

---

## 10. Closing

Jika AI tidak bisa menjaga konteks,  
maka ia tidak bisa menjaga kualitas keputusan.

Dan di bisnis,  
**yang mahal bukan salah analisis—  
tapi keputusan yang tidak konsisten.**
