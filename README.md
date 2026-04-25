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