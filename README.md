# Module 07: Java Profiling

# JMETER GUI

## all-student-name
### 1. View Results Tree
![tree](test_plan/test_plan_2/tree_result.png)

### 2. View Results in Table
![table](test_plan/test_plan_2/table_result.png)

### 3. Summary Report
![summary](test_plan/test_plan_2/summary_report.png)

### 4. Graph Results
![graph](test_plan/test_plan_2/graph_result.png)

## highest-gpa
### 1. View Results Tree
![tree](test_plan/test_plan_3/tree_result.png)

### 2. View Results in Table
![table](test_plan/test_plan_3/table_result.png)

### 3. Summary Report
![summary](test_plan/test_plan_3/summary_report.png)

### 4. Graph Results
![graph](test_plan/test_plan_3/graph_result.png)

# JMETER CLI

## all-student-name
![student_cli](test_plan/test_plan_2/cli_result.png)

## highest-gpa
![gpa_cli](test_plan/test_plan_3/cli_result.png)

# Kesimpulan JMeter

Setelah dilakukan profiling dan optimisasi kode, JMeter menunjukkan adanya peningkatan performance dibandingkan dengan pengukuran pertama. Endpoint yang dioptimisasi memiliki response time lebih cepat karena adanya pengurangan query database yang tidak penting serta pemrosesan memory yang tidak efisien. Pada kasus ini, aplikasi menjadi lebih cepat dan efisien ketika hanya melakukan query data yang benar-benar dibutuhkan dan membiarkan database menangani beberapa operasi seperti mencari GPA tertinggi. Sejauh ini, optimisasi telah meningkatkan performance aplikasi dan membantu menurunkan processing time pada endpoint yang diuji.

# Reflection Module-7

### 1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
JMeter lebih fokus untuk melihat performa aplikasi dari sisi pengguna, misalnya response time, throughput, dan error rate saat endpoint diakses berkali-kali. Sementara itu, IntelliJ Profiler lebih fokus ke bagian dalam aplikasi, seperti method mana yang paling banyak memakai CPU atau memori. Jadi, JMeter membantu melihat “gejalanya”, sedangkan profiler membantu mencari “penyebabnya”.

### 2. How does the profiling process help you in identifying and understanding the weak points in your application?
Profiling membantu saya melihat bagian kode yang paling berat ketika aplikasi berjalan. Dari hasil profiler, saya bisa tahu method mana yang memakan waktu paling lama atau dipanggil terlalu sering. Dengan begitu, optimasi tidak dilakukan secara asal, tetapi berdasarkan data dari proses eksekusi aplikasi.

### 3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
Menurut saya IntelliJ Profiler cukup efektif karena hasilnya langsung menunjukkan method yang paling berpengaruh terhadap waktu proses aplikasi. Dari situ saya bisa lebih mudah menemukan bottleneck, misalnya query yang terlalu banyak atau proses looping yang kurang efisien. Tampilannya juga cukup membantu karena terintegrasi langsung dengan IDE.

### 4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
Tantangan utamanya adalah hasil pengukuran kadang tidak stabil, terutama karena kondisi komputer, database, atau proses lain yang sedang berjalan. Selain itu, run pertama aplikasi biasanya lebih lambat karena JVM masih melakukan warm-up. Cara saya mengatasinya adalah menjalankan endpoint beberapa kali, tidak memakai hasil pertama, lalu membandingkan hasil rata-rata sebelum dan sesudah optimasi.

### 5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
Manfaat utama IntelliJ Profiler adalah membantu saya memahami bagian mana dari kode yang benar-benar perlu diperbaiki. Saya jadi tidak hanya menebak-nebak penyebab lambatnya aplikasi. Selain itu, profiler juga memudahkan proses analisis karena bisa langsung dikaitkan dengan source code yang sedang dikerjakan.

### 6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
Kalau hasil dari IntelliJ Profiler dan JMeter tidak sepenuhnya sama, saya melihat keduanya dari sudut pandang yang berbeda. JMeter menunjukkan performa endpoint secara keseluruhan, sedangkan profiler menunjukkan detail proses di dalam aplikasi. Jadi, saya akan mengecek ulang skenario test, menjalankan pengukuran beberapa kali, lalu mencari pola yang paling konsisten dari kedua hasil tersebut.

### 7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
Setelah melihat hasil performance testing dan profiling, strategi saya adalah memperbaiki bagian yang paling besar dampaknya terlebih dahulu, misalnya mengurangi query yang berulang, mengambil data yang hanya diperlukan, atau mengganti proses yang kurang efisien. Untuk memastikan fitur tetap berjalan, saya menjalankan ulang aplikasi, mencoba endpoint yang sama, dan memastikan hasil response-nya tetap sesuai sebelum dan sesudah optimasi.