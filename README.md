# <h1> 🚀 Simple Multi-Threaded Port Scanner (Python) </h1>
<h3> 📌 Deskripsi </h3>
<p> Simple Port Scanner adalah project Python yang digunakan untuk memindai port jaringan pada sebuah host (IP address atau domain) untuk mengetahui port mana yang terbuka (open) atau tertutup (closed). </p>

 Project ini dibuat menggunakan:
  <li> Socket Programming </li>
  <li>Multithreading </li>
  <li>Queue & Lock</li>
  <li>CLI (Command Line Interface)</li>
<br>

<h3>✨ Fitur Utama</h3>

<li> ✅ Scan port TCP </li>
<li>✅ Multi-threaded scanning (lebih cepat)</li>
<li>✅ Output berwarna (open / closed)</li>
<li>✅ Support custom port range</li>
<li>✅ CLI friendly (argparse)</li>
<li>✅ Aman untuk environment pembelajaran</li>
<h3>🧠 Cara Kerja</h3>
<ol>User memasukkan host dan rentang port</ol>
<ol>Port dimasukkan ke dalam Queue</ol>
<ol>Beberapa thread bekerja secara paralel</ol>
<br>
<h4> Setiap thread: </h4>
<li> Mencoba Koneksi socket ke port </li>
<li>Menentukan status port (open / closed)</li>
<li>Hasil ditampilkan secara realtime</li>
<br>
<h3>🛠 Teknologi yang Digunakan</h3>
<li>Python 3</li>
<li>socket</li>
<li>threading</li>
<li>queue</li>
<li>argparse</li>
<li>colorama</li>

<h3>📂 Struktur Project</h3>
<ol>port-scanner/</ol>
<ol>|</ol>
<ol>├── port_scanner.py</ol>
<ol>└── README.md </ol>


<h3>▶️ Cara Menjalankan Program</h3>
<ul> 
  Scan semua port (default)
      <li>python port_scanner.py example.com</li>
 </ul>
<ul>
  Scan port tertentu
  <li> python port_scanner.py example.com -p 1-1024 </li>
</ul>

<ul>
  Scan IP Address
 <li> python port_scanner.py 192.168.1.1 -p 20-100 </li>
</ul>


🖥 Contoh Output



🟢 Hijau → Port OPEN

⚫ Abu-abu → Port CLOSED


<h4>
  ⚙️ Penjelasan Kode Inti
</h4>
<ol>
  <li>Multithreading</li>
N_THREADS = 200
<p>Program menggunakan 200 thread agar scanning lebih cepat.</p>
 <li>Queue</li>
  q = Queue()
 <p>Queue digunakan untuk membagi port ke setiap thread secara aman.</p>
<li>Socket Scan</li>
  s.connect((host, port))
<li>Lock</li>
  print_lock = Lock()
  <p>Digunakan agar output terminal tidak tumpang tindih antar thread.</p>
</ol>





