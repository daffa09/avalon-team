<!-- portfolio -->
<!-- slug: avalon-team-todo-list -->
<!-- title: Avalon Team - Daftar Tugas Spring Boot -->
<!-- description: Aplikasi web daftar tugas yang dibangun dengan Spring Boot, JPA, Thymeleaf, dan Spring Security untuk proyek mata kuliah PBO -->
<!-- image: https://github.com/user-attachments/assets/e0397bbb-2687-4cb1-a629-3a60c095d241 -->
<!-- tags: java, spring-boot, jpa, thymeleaf, spring-security, aplikasi-todo, maven -->

# Tim Avalon - Aplikasi Daftar Tugas Spring Boot

<img width="1536" height="1024" alt="avalon-team" src="https://github.com/user-attachments/assets/e0397bbb-2687-4cb1-a629-3a60c095d241" />

Aplikasi web daftar tugas (todo list) fitur lengkap yang dibangun dengan framework Spring Boot. Proyek ini dikembangkan sebagai tugas kelompok untuk mata kuliah Pemrograman Berbasis Objek (PBO), mendemonstrasikan praktik pengembangan web Java modern.

## 📋 Ringkasan

Aplikasi daftar tugas ini menampilkan ekosistem Spring Boot yang kuat, mengimplementasikan operasi CRUD dengan JPA untuk manajemen database, Thymeleaf untuk templating sisi server, Spring Security untuk autentikasi, dan Bootstrap untuk desain UI yang responsif.

## 👥 Anggota Tim (Tim Avalon)

- **Daffa Fathan** (4522210082) - [GitHub](https://github.com/daffa09)
- **Antonius Valentino** (4522210109) - [GitHub](https://github.com/AtroxMedaTic)
- **Tegar Gemilang** (4522210095) - [GitHub](https://github.com/TegarGemilang02)
- **Naufal Rizky** (4522210112) - [GitHub](https://github.com/TruePal09)

## ✨ Fitur

### Manajemen Tugas Inti
- **Buat Tugas**: Menambah item tugas baru dengan judul dan deskripsi.
- **Lihat Tugas**: Menampilkan semua tugas dalam daftar yang terorganisir.
- **Perbarui Tugas**: Mengedit detail tugas yang sudah ada.
- **Hapus Tugas**: Menghapus tugas yang sudah selesai atau tidak diinginkan.
- **Tandai Selesai**: Mengalihkan status penyelesaian tugas.

### Fitur Lanjutan
- **Autentikasi Pengguna**: Login/logout yang aman dengan Spring Security.
- **Manajemen Pengguna**: Daftar tugas individual untuk setiap pengguna.
- **Penyimpanan Persisten**: Integrasi database H2 dengan JPA.
- **Desain Responsif**: Antarmuka ramah seluler dengan Bootstrap 5.
- **Pembaruan Real-time**: Konten dinamis dengan jQuery.
- **Validasi Formulir**: Validasi sisi klien dan server.

## 🛠️ Tech Stack

| Teknologi | Versi | Tujuan |
|------------|---------|---------|
| **Spring Boot** | 2.2.2.RELEASE | Framework aplikasi |
| **Spring Data JPA** | - | ORM Database |
| **Spring Security** | - | Autentikasi & otorisasi |
| **Thymeleaf** | - | Mesin template sisi server |
| **H2 Database** | - | Database in-memory/file |
| **Bootstrap** | 5.3.2 | Framework frontend |
| **jQuery** | 2.1.4 | Library JavaScript |
| **Maven** | - | Otomasi build |
| **Java** | 11 | Bahasa pemrograman |

## 📁 Struktur Proyek

```
avalon-team/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── guru/springframework/
│   │   │       ├── config/          # Konfigurasi keamanan
│   │   │       ├── controllers/     # Controller MVC
│   │   │       ├── domain/          # Model entitas
│   │   │       ├── repositories/    # Repositori JPA
│   │   │       └── services/        # Logika bisnis
│   │   └── resources/
│   │       ├── templates/           # Template Thymeleaf
│   │       ├── static/             # CSS, JS, gambar
│   │       └── application.properties
│   └── test/                        # Unit test
├── pom.xml                          # Dependensi Maven
├── .editorconfig                    # Konfigurasi editor
└── README.md
```

## 🚀 Memulai

### Prasyarat

- **Java JDK 11** atau lebih baru.
- **Maven 3.6+** (atau gunakan Maven wrapper yang disertakan).
- **Git** untuk kontrol versi.
- **IDE** (IntelliJ IDEA, Eclipse, atau VS Code dengan ekstensi Java).

### Langkah Instalasi

1. **Clone Repositori**
   ```bash
   git clone <repository-url>
   cd avalon-team
   ```

2. **Build dengan Maven**
   
   Menggunakan Maven wrapper (disarankan):
   ```bash
   ./mvnw clean install
   ```
   
   Atau menggunakan Maven yang terinstal:
   ```bash
   mvn clean install
   ```

3. **Jalankan Aplikasi**
   
   Menggunakan Maven wrapper:
   ```bash
   ./mvnw spring-boot:run
   ```
   
   Atau menggunakan Maven:
   ```bash
   mvn spring-boot:run
   ```

4. **Akses Aplikasi**
   
   Buka browser Anda dan navigasi ke:
   ```
   http://localhost:8080
   ```

### Konfigurasi Database

Aplikasi menggunakan database H2 secara default:

**Akses Konsol H2:**
- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (biarkan kosong)

Untuk menggunakan database berbasis file, perbarui `application.properties`:
```properties
spring.datasource.url=jdbc:h2:file:./data/tododb
spring.jpa.hibernate.ddl-auto=update
```

## 💻 Panduan Penggunaan

### Registrasi & Login

1. **Daftar Pengguna Baru** (jika registrasi diaktifkan)
   - Navigasi ke halaman registrasi.
   - Masukkan nama pengguna dan kata sandi.
   - Kirim untuk membuat akun.

2. **Login**
   - Gunakan halaman login Spring Security.
   - Masukkan kredensial.
   - Akses daftar tugas pribadi Anda.

### Mengelola Tugas

#### Menambah Tugas
1. Klik tombol "Add New Todo".
2. Masukkan judul tugas.
3. Tambahkan deskripsi (opsional).
4. Atur prioritas (jika diimplementasikan).
5. Klik "Save".

#### Melihat Tugas
- Semua tugas ditampilkan di dashboard utama.
- Filter berdasarkan status: Semua, Aktif, Selesai.
- Urutkan berdasarkan tanggal, prioritas, atau alfabet.

#### Mengedit Tugas
1. Klik tombol "Edit" pada item tugas.
2. Ubah judul atau deskripsi.
3. Perbarui prioritas/tanggal jatuh tempo.
4. Klik "Update".

#### Menyelesaikan Tugas
- Klik kotak centang untuk menandai sebagai selesai.
- Tugas yang selesai ditampilkan dengan coretan.

#### Menghapus Tugas
1. Klik tombol "Delete".
2. Konfirmasi penghapusan di modal.
3. Tugas dihapus dari daftar.

## 🎨 Komponen UI

### Dashboard Utama
- Tampilan daftar tugas.
- Tombol tambah tugas.
- Kontrol filter/sortir.
- Menu pengguna.

### Kartu Tugas
- Judul dan deskripsi.
- Kotak centang penyelesaian.
- Tombol edit dan hapus.
- Indikator prioritas.
- Tanggal pembuatan.

### Formulir
- Formulir tambah/edit tugas.
- Validasi input.
- Pesan kesalahan.
- Notifikasi sukses.

## 🔒 Fitur Keamanan

Spring Security menyediakan:
- **Autentikasi**: Sistem login pengguna.
- **Otorisasi**: Kontrol akses berbasis peran.
- **Perlindungan CSRF**: Pencegahan pemalsuan permintaan antar situs.
- **Encoding Kata Sandi**: Hashing kata sandi BCrypt.
- **Manajemen Sesi**: Penanganan sesi yang aman.

## 🗄️ Skema Database

### Entitas Todo
```java
@Entity
public class Todo {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String title;
    private String description;
    private boolean completed;
    private LocalDateTime createdAt;
    private LocalDateTime updatedAt;
    
    @ManyToOne
    private User user;
    
    // Getter dan setter
}
```

### Entitas User
```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String username;
    private String password;
    private String role;
    
    @OneToMany(mappedBy = "user")
    private List<Todo> todos;
    
    // Getter dan setter
}
```

## 🎓 Tujuan Pembelajaran

Proyek ini mendemonstrasikan:

### Pemrograman Berbasis Objek
- Desain kelas dan enkapsulasi.
- Pewarisan dan polimorfisme.
- Implementasi antarmuka (Interface).
- Pola desain (MVC, Repository, Service).

### Framework Spring
- Dependency Injection.
- Arsitektur Spring MVC.
- Spring Data JPA.
- Dasar-dasar Spring Security.
- Manajemen konfigurasi.

### Pengembangan Web
- Prinsip RESTful.
- Mesin template (Thymeleaf).
- Penanganan formulir.
- Manajemen sesi.
- Integrasi frontend.

## 🔧 Konfigurasi

### Properti Aplikasi (Application Properties)

```properties
# Konfigurasi Server
server.port=8080

# Database
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# Konsol H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# JPA
spring.jpa.hibernate.ddl-auto=create-drop
spring.jpa.show-sql=true

# Thymeleaf
spring.thymeleaf.cache=false
```

## 🐛 Pemecahan Masalah

**Port Sudah Digunakan**
```bash
# Ubah port di application.properties
server.port=8081
```

**Build Maven Gagal**
```bash
# Bersihkan cache Maven
./mvnw clean
rm -rf ~/.m2/repository
./mvnw install
```

**Masalah Koneksi Database**
- Periksa pengaturan konsol H2.
- Verifikasi JDBC URL.
- Pastikan tidak ada instansi lain yang berjalan.

**Login Tidak Berhasil**
- Periksa konfigurasi Spring Security.
- Verifikasi pengguna ada di database.
- Periksa encoding kata sandi.

## 🚀 Deployment

### File JAR
```bash
./mvnw clean package
java -jar target/spring-boot-web-0.0.1-SNAPSHOT.jar
```

### Docker
```dockerfile
FROM openjdk:11-jre-slim
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

Build dan jalankan:
```bash
docker build -t avalon-todo .
docker run -p 8080:8080 avalon-todo
```

## 📚 Resource

- [Dokumentasi Spring Boot](https://spring.io/projects/spring-boot)
- [Panduan Spring Data JPA](https://spring.io/guides/gs/accessing-data-jpa/)
- [Dokumentasi Thymeleaf](https://www.thymeleaf.org/documentation.html)
- [Spring Framework Guru](https://springframework.guru) - Inspirasi tutorial.

## 🙏 Ucapan Terima Kasih

Proyek ini terinspirasi oleh tutorial dari [Spring Framework Guru](https://springframework.guru) dan dibuat sebagai bagian dari mata kuliah Pemrograman Berbasis Objek di Universitas Pancasila.

## 🤝 Kontribusi

Ini adalah proyek kelompok akademik. Kontribusi anggota tim:
- Peninjauan kode melalui pull request.
- Mengikuti konvensi pengkodean Java.
- Dokumentasi yang komprehensif.
- Cakupan unit test.

##  📄 Lisensi

Dibuat untuk tujuan pendidikan sebagai proyek mata kuliah PBO.

## 💭 Catatan Tim

Dikembangkan secara kolaboratif oleh Tim Avalon untuk mata kuliah Pemrograman Berbasis Objek. Proyek ini membantu kami memahami ekosistem Spring Boot, kolaborasi tim, dan praktik pengembangan web Java di dunia nyata.

---

**Dikembangkan oleh Tim Avalon** ✅📝  
Daftar Tugas Spring Boot untuk Proyek Mata Kuliah PBO!
