1. Buat projectnya
-klik “New Project”
-pilih template yang di inginkan, contoh yang “Empty Views Activity”
-ubah namanya menjadi “IF Unsoed Mobile”
-klik “Finish”

2. Tampilan awal
-klik “Project”
-klik “app”, “src”, “main”, “res” nah pada bagian inilah akan memasukkan codingan dan eksekusi lebih lanjut

3. Memasukkan foto, icon, atau gambar
-install icon dan gambarnya di link https://drive.google.com/drive/folders/1-Im9Zaa6t_BAbBz2MvomcQNHZMAsIWRi?usp=drive_link dan https://drive.google.com/drive/folders/1TX28wk-Qmg-h1IaZNfmDyTmSTh-67aOO?usp=drive_link 

Maukkan Icon
-masuk ke tool window pilih yang “Resource Manager”
-klik tambah +
-klik “Image Asset”
-masukkan foto atau icon yang sudah di download pada link https://drive.google.com/drive/folders/1-Im9Zaa6t_BAbBz2MvomcQNHZMAsIWRi?usp=drive_link dengan cara klik “path” dan cari foto yang sudah di download
-ubah juga bagian “resize” menjadi 69% sesuai modul
-klik “Next”

Masukkan Gambar FT
-masuk ke tool window pilih yang “Resource Manager”
-klik tambah +
-klik “Import Drawables”
-masukkan gambar yang sudah di download pada link https://drive.google.com/drive/folders/1TX28wk-Qmg-h1IaZNfmDyTmSTh-67aOO?usp=drive_link 
-klik “Next”

4. Memasukkan teks
-klik “app”, “src”, “main”, “res”, “ values”, “strings.xml” pada bagian ini diisikan dengan sesuai perintah

Nama aplikasi  
<string name="app_name">IF Unsoed Mobile</string>

Judul
<string name="welcome_text">
    Selamat datang di Prodi Informatika,\nFakultas Teknik, \nUniversitas Jenderal Soedirman
</string>

Deskripsi
<string name="inf_descrition">
    Program Studi Informatika di Universitas Jenderal Soedirman (Unsoed) berdiri pada tahun 2008, berawal dari kebutuhan yang semakin mendesak akan tenaga ahli di bidang teknologi informasi dan komunikasi. Saat itu, perkembangan teknologi yang pesat di Indonesia dan dunia memerlukan adanya program pendidikan tinggi yang mampu mencetak lulusan dengan kompetensi tinggi di bidang informatika. \nPada tahun tersebut, Fakultas Sains dan Teknik (FST) Unsoed mengambil inisiatif untuk mendirikan Program Studi Informatika. Pembentukan program studi ini bertujuan untuk memenuhi tuntutan masyarakat dan industri yang membutuhkan tenaga profesional dalam bidang teknologi informasi. Kurikulum yang disusun dirancang untuk memberikan pendidikan berkualitas, menggabungkan aspek praktis dan teoritis dari informatika, seperti pemrograman, sistem informasi, jaringan komputer, dan kecerdasan buatan.
</string>

Tombol next
<string name="next">Next</string>

5. Ubah Layout
-klik “app”, “src”, “main”, “res”, “layout”, “activity_main.xml” disini akan mengisikan buat tampilannya akan seperti apa 
-hapus dulu isiannya dari bagian <android> hingga </android>
-masukkan sesuai instruksi di modul yaitu masukkan “<LinearLayout>” nanti akan otomatis muncul
-masukkan codingannya 
	android:id="@+id/main"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="16dp">
-kemudian untuk yang imagenya tambahkan codingan
<ImageView
    android:id="@+id/img_gedung_teknik"
    android:layout_width="match_parent"
    android:layout_height="200dp"
    android:adjustViewBounds="true"
    android:scaleType="fitXY"
    android:src="@drawable/gedung_teknik" />
-tambahkan untuk tampilannya dengan codingan
<TextView
    android:id="@+id/tv_welcome"
    style="@style/MaterialAlertDialog.Material3.Body.Text"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="@string/welcome_text"
    android:textAlignment="center"
    android:textStyle="bold"/>

<TextView
    android:id="@+id/tv_description"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="8dp"
    android:justificationMode="inter_word"
    android:text="@string/inf_descrition"/>
Pada bagian text view ini juga kemarin terdapat eror sehingga harus di selesaikan, sehingga menambahkan atau memunculkan codingan xmlns:app="http://schemas.android.com/apk/res-auto"
Di bagian awal setelah <LinearLayout> dan sebelum android:id

-tambahkan button
	<com.google.android.material.button.MaterialButton
	    android:id="@+id/btn_to_page2"
	    android:layout_width="wrap_content"
	    android:layout_height="33dp"
	    android:layout_gravity="right"
	    android:text="@string/next"
	    app:backgroundTint="@color/colorPrimary" />
Pada bagian ini kemarin terjadi sebuah eror karena pada bagian klik “app”, “src”, “main”, “res”, “ values”, “color.xml” belum ada codingan
<color name="colorPrimary">#FF000000</color>
Sehingga harus di tambahkan

6. Coba run dan ketika di run sebisa mungkin di hubungkan dengan kabel USB untuk menampilkan atau memunculkan aplikasi atau project yang berjalan lancar.
