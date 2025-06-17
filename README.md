# A-Star-8-Puzzle-Solver

Repositori ini berisi sebuah Jupyter Notebook (`.ipynb`) yang merupakan implementasi dari algoritma pencarian A* (A-Star) untuk menyelesaikan permainan klasik 8-Puzzle. Proyek ini dibuat sebagai bagian dari tugas mata kuliah Kecerdasan Buatan (AI).

---

## Deskripsi Proyek

Tujuan dari proyek ini adalah untuk menerapkan algoritma *informed search* A* dalam menemukan solusi paling efisien (jumlah langkah terpendek) untuk permainan 8-Puzzle dari sebuah konfigurasi awal (*initial state*) ke konfigurasi tujuan (*goal state*).

### Tentang Algoritma A*
A* adalah salah satu algoritma pencarian graf yang paling populer dan efisien. Algoritma ini mencari rute terpendek dari satu titik ke titik lain dengan menggabungkan biaya yang telah ditempuh dengan estimasi biaya ke depan (heuristik). Evaluasi setiap *node* dilakukan menggunakan fungsi:

$$f(n) = g(n) + h(n)$$

- $g(n)$: Biaya sebenarnya dari *node* awal ke *node* saat ini `n`.
- $h(n)$: Biaya estimasi (heuristik) dari *node* saat ini `n` ke *node* tujuan.

Dalam kasus 8-Puzzle, heuristik yang umum digunakan adalah *Manhattan Distance* atau jumlah ubin yang salah tempat.

---

## Isi Notebook (`tugas1 AI.ipynb`)

Notebook ini berisi langkah-langkah implementasi yang terstruktur dan terdokumentasi dengan baik:

- **Penjelasan Masalah:** Deskripsi tentang apa itu 8-Puzzle dan bagaimana algoritma A* dapat digunakan untuk menyelesaikannya.
- **Implementasi Kode:**
    - Definisi kelas atau struktur data untuk merepresentasikan *state* dari puzzle (posisi ubin).
    - Fungsi untuk menghasilkan langkah-langkah yang mungkin (atas, bawah, kiri, kanan) dari *state* saat ini.
    - Implementasi fungsi heuristik untuk menghitung nilai $h(n)$.
    - Logika utama dari algoritma A* yang menggunakan *priority queue* untuk mengelola daftar simpul yang akan dieksplorasi (*open list*).
- **Eksekusi dan Hasil:**
    - Contoh penggunaan dengan *initial state* dan *goal state* yang telah ditentukan.
    - Output yang menunjukkan langkah-langkah solusi dari awal hingga akhir, serta jumlah langkah yang dibutuhkan untuk mencapai solusi.

---

## Cara Menggunakan

Untuk menjalankan notebook ini, Anda memerlukan lingkungan Python dengan Jupyter Notebook atau JupyterLab terinstal.

1.  **Clone Repositori:**
    ```bash
    git clone https://github.com/Mystery230/A-Star-8-Puzzle-Solver.git

    cd A-Star-8-Puzzle-Solver
    ```

2.  **Buka Jupyter Notebook:**
    Jalankan perintah berikut di terminal Anda:
    ```bash
    jupyter notebook "A-Star-8-Puzzle-Solver.ipynb"
    ```
    Atau, buka aplikasi Jupyter Notebook/JupyterLab dan navigasikan secara manual ke file `tugas1 AI.ipynb`.

3.  **Jalankan Sel:**
    Anda dapat menjalankan setiap sel kode secara berurutan dari atas ke bawah untuk melihat proses dan hasil dari implementasi algoritma A*.
