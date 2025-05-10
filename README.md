# Menyelesaikan Permasalahan Human Resources

## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.


## Business Problem

Untuk mencegah masalah ini memburuk, manajer departemen HR meminta bantuan Saya untuk mengidentifikasi berbagai faktor yang berkontribusi terhadap tingginya attrition rate. Selain itu, ia juga meminta Saya membuat sebuah business dashboard untuk memonitori faktor-faktor tersebut secara berkala.


## Project Scope
- Melakukan persiapan data dan pembersihan data awal.
- Melaksanakan Exploratory Data Analysis (EDA) untuk mengidentifikasi faktor-faktor penyebab tingginya attrition rate melalui visualisasi data.
- Membuat business dashboard yang menampilkan faktor-faktor utama penyebab tingginya tingkat attrition.
- Membangun model machine learning untuk memprediksi status karyawan berdasarkan variabel-variabel yang berkaitan dengan penyebab attrition.


**Dataset source:** [Employee data](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee 'Dicoding GitHub - Employee data')

## Setup Environment - Anaconda

1. Clone Repository
   ```bash
   git clone https://github.com/RozyRangkuti/Employee-Attrition-Analysis.git
   ```

2. Buka Terminal Anaconda, jalankan perintah berikut untuk membuat environment baru
   ```bash
   conda create --name main-ds python=3.11
   ```

3. Aktifkan virtual environment dengan menjalankan perintah berikut ini
   ```bash
   conda activate main-ds
   ```

4. Install semua requirements di dalam file "requirements.txt"
   ```bash
   pip install -r requirements.txt
   ```

## Menjalankan Dashboard
 Untuk melihat isi dashboard secara langsung, kita dapat menggunakan metabase dengan bantuan Docker (pastikan Docker sudah terinstall).

1. Jalankan perintah berikut
   ```bash
   docker pull metabase/metabase:v0.46.4
   ```

2. Jalankan container Metabase menggunakan perintah
   ```bash
   docker run -p 3000:3000 --name metabase metabase/metabase
   ```

3. Login ke Metabase menggunakan username dan password berikut
   ```bash
   Username : muhammadrozy37@gmail.com
   Pass     : mrozys123
   ```
 
## Bussiness Dashbord Using Metabase
Jaya Jaya Maju Employees Dashboard ini dirancang seefisien mungkin untuk memberikan wawasan kepada para manajer HR Departemen mengenai tingkat attrition yang cukup tinggi, yakni lebih dari 10%. Berikut tampilan Dashboard menggunakan Metabase.

<img width="439" alt="muhammadrozy-dashboard" src="https://github.com/user-attachments/assets/32523bee-3b1b-4fa9-9e80-3c5929ed6695" />

## Penjelasan Bussiness Dashboard Jaya Jaya Maju Employees

1. Grafik Bar Chart (Attrition)
   
   <img width="229" alt="Attrition" src="https://github.com/user-attachments/assets/1952f325-96fe-402a-83c5-e7974333c45b" />
   
   Grafik ini menjelaskan tentang jumlah karyawan yang melakukan attirion (Yes) sebanyak 179 Karyawab dan yang tidak melakukan attrition (No) sebanyak 879 Karyawan.

2.  Grafik Average of Monthly Income
   
    <img width="197" alt="average of monthly income" src="https://github.com/user-attachments/assets/5729f688-0ce9-4e52-86c6-85793674db3c" />
    
    Grafik ini menjelaskan tentang rata-rata gaji perbulan karyawan yaitu sebesar $6,625.95.

3.  Grafik Average of Years At Company
   
    <img width="197" alt="average of years at company" src="https://github.com/user-attachments/assets/cad1a9f9-379d-4748-822c-e79a76fe3a66" />

    Grafik ini menjelaskan tentang rata-rata tahun Karyawan bekerja di perusahaan, yaitu sebanyak 7.07 Tahun.

4.  Grafik  Average of Daily Rate

    <img width="165" alt="average of daily rate" src="https://github.com/user-attachments/assets/fff126fc-a664-44cb-8f3a-bb539c8b6710" />

    Grafik ini menjelaskan tentang rata-rata gaji perhari karyawan yaitu sebesar $809.54.

5.  Grafik Area Chart (Attrition By Age)

    ![Attrition By Age-5_3_2025, 4_28_42 PM](https://github.com/user-attachments/assets/f9186a9b-a626-469f-a0bd-a21d866efe1d)

    Grafik ini menjelaskan tentang Karyawan yang melakukan attrition atau tidak berdasarkan usia, Seperti yang terlihat pada grafik di atas, attrition maksimum terjadi pada     kelompok usia 28-32 tahun. Tingkat attrition terus menurun seiring dengan bertambahnya usia, karena orang-orang mencari stabilitas dalam pekerjaan mereka pada masa-masa     ini. Juga pada usia yang sangat muda, yaitu dari 18-20 tahun, kemungkinan seorang karyawan meninggalkan organisasi jauh lebih banyak - karena mereka sedang menjelajah       pada saat itu. Mencapai titik impas pada usia 21 tahun.

6.  Grafik Row Chart (Attrition by Department)

    ![Attrition by Department-5_3_2025, 4_31_07 PM](https://github.com/user-attachments/assets/93721453-6f43-491b-8bb5-f2e18bebca4e)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan departemen mereka bekerja, Data ini hanya terdiri dari 3 departemen utama, di   
    antaranya departemen Sales memiliki tingkat attrition tertinggi (20,69%), diikuti oleh Departemen Human Resources (15,79%). Departemen Research & Development memiliki 
    tingkat attrition paling rendah, yang menunjukkan stabilitas dan isi dari departemen tersebut seperti yang dapat dilihat dari grafik di atas (15,26%).

7.  Grafik Area Chart (Attrition by Monthly Income)

    ![Attrition by Monthly Income-5_3_2025, 4_41_11 PM](https://github.com/user-attachments/assets/5db06365-6544-432d-b4f3-8b9bf2dd715e)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan gaji yang mereka terima setiap bulan, seperti yang ditunjukkan oleh grafik,          tingkat attrition cenderung tinggi pada kelompok dengan pendapatan bulanan sangat rendah, yaitu di bawah 5 ribu. Seiring meningkatnya pendapatan, tingkat attrition          menurun, meskipun terdapat sedikit kenaikan di sekitar angka 10 ribu—yang mencerminkan kelompok kelas menengah. Kelompok ini cenderung mencari pekerjaan lain demi           mencapai standar hidup yang lebih baik. Sementara itu, pada tingkat pendapatan yang lebih tinggi, kecenderungan karyawan untuk keluar dari perusahaan menjadi rendah,        seperti yang tergambarkan oleh bagian grafik yang mendatar.

8.  Grafik Row Chart (Attrition By Job Role)

    ![Attrition by Job Role-5_3_2025, 4_56_47 PM](https://github.com/user-attachments/assets/744eb1f4-b04f-47f8-b548-64f91b43d5f4)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan Job Role mereka, Sales Representative memiliki tingkat attrition tertinggi           (43,10%), diikuti oleh Job Role Laboratory Technician (26,06%), Human Resources (20%), Research Scientist (17,76%) dan Sales Executive (16,81%). Research Director dan       Manufacturing Director memiliki tingkat attrition yang sangat rendah, hampir seluruh karyawan dalam job role ini tetap bertahan. Posisi seperti Sales Representative dan 
    Laboratory Technician mungkin menghadapi tekanan kerja tinggi, kompensasi yang tidak memadai, atau peluang karir terbatas—perlu evaluasi ulang terkait kondisi kerja dan 
    jalur pengembangan karier mereka. Sebaliknya, posisi seperti Research Director cenderung stabil, yang bisa mencerminkan kepuasan kerja tinggi, gaji yang baik, atau 
    peran strategis dengan mobilitas eksternal yang lebih rendah.

9.  Grafik Area Chart (Attrition by Num Companies Worked)

    ![Attrition by NumCompaniesWorked-5_3_2025, 5_25_58 PM](https://github.com/user-attachments/assets/d2b4b175-9ab0-4bc1-a8e4-5cb1e5f7a5c0)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan pengalaman karyawan dari jumlah perusahaan yang sudah rekrut mereka, seperti 
    yang terlihat dari grafik di atas, jelas bahwa karyawan yang memulai karir mereka dengan perusahaan, atau telah beralih ke perusahaan pada tahun-tahun awal karir 
    mereka, memiliki peluang lebih tinggi untuk meninggalkan perusahaan ini ke perusahaan lain. Orang-orang yang telah mendapatkan banyak pengalaman bekerja di beberapa 
    perusahaan cenderung bertahan di perusahaan tempat mereka bergabung.

10. Grafik Row Chart (Attrition by WorkLifeBalance)

    ![Attrition by WorkLifeBalance-5_3_2025, 5_32_23 PM](https://github.com/user-attachments/assets/fdb2a613-2d11-450a-86cb-a3b5e0df4645)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan work life balance mereka. Karyawan dengan tingkat work life balance yang buruk 
    telah menyesuaikan diri dengan pekerjaan mereka, tetapi seperti yang terlihat pada parameter di atas dengan skor kehidupan kerja yang lebih baik, orang-orang lebih 
    terbiasa dengan kehidupan yang lebih baik dan lebih ingin melakukan attrition. Namun tren ini akan hilang ketika work life balance benar-benar baik, dan orang merasa 
    puas dengan pekerjaan yang mereka lakukan.

11. Grafik Area Chart (Attrition by Years In Current Role)

    ![Attrition by YearsInCurrentRole-5_3_2025, 6_25_44 PM](https://github.com/user-attachments/assets/a2fe715d-e328-4a74-ab61-e38e6cd5c43c)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan berapa lama (tahun) mereka bekerja di role tersebut, pada grafik diatas terlihat 
    bahwa karyawab lebih cenderung meninggalkan perusahaan pada tahun-tahun awal dalam peran mereka. Ketika karyawan berada dalam peran yang sama untuk jangka waktu yang 
    lama, mereka cenderung bertahan lebih lama untuk naik jabatan.

12. Grafik Row Chart (Attrition by Job Involvement)

    ![Attrition by JobInvolvement-5_3_2025, 6_32_00 PM](https://github.com/user-attachments/assets/562a3120-92b0-426e-90dd-69ad4bc06664)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan keterlibatan mereka dalam pekerjaan, terlihat pada grafik tingkat attrition          tertinggi yaitu karyawan yang memiliki job involvment yang Low (rendah) sebesar 40%, diikuti tingkat Medium sebesar 20,15%, high 14,72% dan very high 9,52%.

13. Grafik Area Chart (Attrition by Percent Salary Hike)

    ![Attrition by PercentSalaryHike-5_4_2025, 12_05_52 AM](https://github.com/user-attachments/assets/8168be95-96fa-4b62-88b8-4fa09ccdd575)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan persentase kenaikan gaji. Kenaikan gaji yang lebih tinggi memotivasi karyawan 
    untuk bekerja lebih baik, dan bertahan dalam perusahaan. Oleh karena itu, Saya melihat kemungkinan karyawan meninggalkan perusahaan yang memberikan kenaikan gaji lebih 
    rendah, jauh lebih besar daripada perusahaan yang memberikan kenaikan gaji yang baik.

14. Grafik Row Chart (Attrition by Job Satisfaction)

    ![Attrition by Job Satisfaction-5_4_2025, 12_13_11 AM](https://github.com/user-attachments/assets/8204f3b1-1c36-4705-97a8-7177a0ceb236)

    Grafik ini menjelaskan tentang karyawan yang melakukan attrition atau tidak berdasarkan kepuasan karyawan dalam bekerja. Dengan meningkatnya kepuasan kerja, tingkat 
    Attrition menurun seperti yang terlihat pada grafik di atas. Juga dari rentang Low ke Medium kita dapat menyimpulkan tingkat attrition turun, tetapi meningkat dari 
    Medium ke High, di mana karyawan cenderung memilih peluang yang lebih baik.

15. Grafik Pie Chart (Gender)

    ![Gender-5_4_2025, 12_20_33 AM](https://github.com/user-attachments/assets/f0ea76d1-4afb-483e-b197-5efb36ccd5e9)

    Grafik ini menjelaskan tentang jumlah karyawan berdasarkan jenis kelamin, diketahui bahwa Laki-Laki sebesar 58,6% (620) dan perempuan sebesar 41,4% (438).

16. Grafik Pie Chart (Marital Status)

    ![MaritalStatus-5_4_2025, 12_24_30 AM](https://github.com/user-attachments/assets/21240b1d-9600-4279-985d-af298c56c77f)

    Grafik ini menjelaskan tentang status pernikahan karyawan, Married sebesar 43,9% (464), Single sebesar 33,3% (352) dan Divorced sebesar 22,9% (242).

17. Grafik Pie Chart (Education)

    ![Education-5_4_2025, 12_27_49 AM](https://github.com/user-attachments/assets/179ed72b-58c2-4a10-8ede-ffa5e9c2d8dd)

    Grafik ini menjelaskan tentang jenjang pendidikan yang ditempuh karyawan, Bachelor tertinggi dengan 38,75% (410), diikuti oleh gelar Master dengan 26,09% (276), College     sebesar 19,66% (208), Below College sebesar 12,38% (131) dan gelar doctor yang paling sedikit dengan 3,12% (33).


## Conclusion
1. Pada tahap awal karier, karyawan cenderung lebih sering berpindah pekerjaan. Namun, setelah mereka membangun keluarga atau mencapai stabilitas dalam karier, mereka cenderung menetap lebih lama di satu perusahaan dan melakukan perpindahan secara vertikal di dalam perusahaan tersebut.
2. Gaji merupakan faktor motivasi yang kuat bagi karyawan, di mana peningkatan gaji berkontribusi pada menurunnya tingkat turnover. Karyawan dengan kompensasi yang lebih tinggi cenderung menunjukkan loyalitas yang lebih besar terhadap perusahaan.
3. Work Life Balance merupakan salah satu faktor motivasi utama bagi karyawan. Namun demikian, karyawan yang telah memiliki keseimbangan kerja dan kehidupan pribadi yang baik tetap cenderung mencari peluang baru untuk meningkatkan standar hidup mereka.
4. Departemen yang menuntut pencapaian target tinggi, seperti Sales, cenderung memiliki tingkat turnover yang lebih tinggi dibandingkan dengan departemen yang bersifat administratif, seperti Human Resources.
5. Karyawan yang merasakan kepuasan kerja dan menikmati lingkungan kerja yang positif cenderung menunjukkan loyalitas tinggi terhadap perusahaan, yang tentunya berdampak baik bagi keberlangsungan perusahaan. Sebaliknya, karyawan yang kurang puas dengan proyek yang sedang mereka jalani lebih cenderung meninggalkan perusahaan.


## Recommendation Action
Berikut beberapa rekomendasi yang dapat diimplementasikan perusahaan untuk mengatasi masalah tingginya attrition rate:
1. Terkait dengan keterlibatan karyawan, sangat penting untuk membangun lingkungan kerja yang lebih inklusif dan mendukung perkembangan karier.
2. Mengingat tingginya attrition rate pada rentang usia 19-30 tahun, perusahaan dapat merancang program khusus untuk mempertahankan karyawan muda, seperti mentorship, peluang untuk pengembangan karier yang cepat, atau penghargaan atas kontribusi mereka.
3. Fokus pada peningkatan kepuasan kerja dengan memberikan lebih banyak apresiasi positif, pengakuan terhadap pencapaian, serta kesempatan untuk meningkatkan kesejahteraan karyawan.
4. Bangun budaya kerja yang mendorong keseimbangan antara pekerjaan dan kehidupan pribadi. Terapkan lingkungan kerja seperti fleksibilitas waktu kerja, bekerja dari rumah, dan cuti yang fleksibel untuk membantu mengurangi kejenuhan dan stres yang terkait dengan pekerjaan mereka, karena karyawan dengan work life balance yang buruk cenderung memiliki tingkat attrition yang lebih tinggi. Hal ini penting untuk menjaga keseimbangan dan membantu mengurangi angka perputaran karyawan.
6. Lakukan pemantauan secara terus-menerus terhadap tingkat attrition dan lakukan analisis mendalam untuk mengidentifikasi tren serta faktor risiko lebih awal. Langkah ini akan memungkinkan perusahaan untuk mengantisipasi potensi masalah dan mengambil tindakan pencegahan yang tepat.
7. Tingkatkan komunikasi antara manajemen dan karyawan untuk lebih memahami kebutuhan dan harapan mereka.
