# Praktikum4

## Latihan

```java
public class Mahasiswa {

    // Attributes
    private String nim;
    private String nama;
    private String jurusan;
    private double ipk;

    // Constructor
    public Mahasiswa(String nim, String nama, String jurusan, double ipk) {
        this.nim = nim;
        this.nama = nama;
        this.jurusan = jurusan;
        this.ipk = ipk;
    }

    // Getter and Setter for nim
    public String getNim() {
        return nim;
    }

    public void setNim(String nim) {
        this.nim = nim;
    }

    // Getter and Setter for nama
    public String getNama() {
        return nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    // Getter and Setter for jurusan
    public String getJurusan() {
        return jurusan;
    }

    public void setJurusan(String jurusan) {
        this.jurusan = jurusan;
    }

    // Getter and Setter for ipk
    public double getIpk() {
        return ipk;
    }

    public void setIpk(double ipk) {
        if(ipk >= 0.0 && ipk <= 4.0) {
            this.ipk = ipk;
        } else {
            System.out.println("IPK harus antara 0.0 hingga 4.0");
        }
    }

    // Method untuk menampilkan informasi mahasiswa
    public void tampilkanInfo() {
        System.out.println("NIM: " + nim);
        System.out.println("Nama: " + nama);
        System.out.println("Jurusan: " + jurusan);
        System.out.println("IPK: " + ipk);
    }
    
    public static void main(String[] args) {
        // Membuat objek Mahasiswa
        Mahasiswa mahasiswa = new Mahasiswa("12345", "Mina", "Informatika", 3.75);
        
        // Menampilkan informasi awal mahasiswa
        mahasiswa.tampilkanInfo();
        
        // Mengubah nilai nama dan ipk menggunakan setter
        mahasiswa.setNama("Mina");
        mahasiswa.setIpk(3.9);
        
        // Menampilkan informasi setelah perubahan
        System.out.println("\nSetelah perubahan:");
        mahasiswa.tampilkanInfo();
    }
}
```

![Code Mahasiswa](Screenshot/Mahasiswa/Mahasiswa%201.png)
![Code Mahasiswa](Screenshot/Mahasiswa/Mahasiswa%202.png)
![Code Mahasiswa](Screenshot/Mahasiswa/Mahasiswa%203.png)

### Output
![Output Mahasiswa](Screenshot/Mahasiswa/Output%20Mahasiswa.png)

## Praktikum 4

### Class Main

```java
public class Main {
    public static void main(String[] args) {
        Programmer prog = new Programmer();
        prog.setNama("Kii");
        prog.setGajiPokok(7000000);
        prog.setTunjangan(2000000);
        prog.setBonus(1500000);

        prog.cetakInfo();
        prog.cetakTunjangan();
        prog.cetakBonus();

        System.out.println();

        Manager mgr = new Manager();
        mgr.setNama("Chiuuu");
        mgr.setGajiPokok(9000000);
        mgr.setTunjangan(3000000);
        mgr.setBonus(2500000);

        mgr.cetakInfo();
        mgr.cetakTunjangan();
        mgr.cetakBonus();
    }
}
```

![Implementasi Class Main](Screenshot/Main%20n%203%20Class/Class%20Main.png)

### Class Pegawai

```java
public class Pegawai {
    private String nama;
    private double gajiPokok;

    // Setter untuk nama
    public void setNama(String nama) {
        this.nama = nama;
    }

    // Getter untuk nama
    public String getNama() {
        return nama;
    }

    // Setter untuk gaji pokok
    public void setGajiPokok(double gajiPokok) {
        this.gajiPokok = gajiPokok;
    }

    // Getter untuk gaji pokok
    public double getGajiPokok() {
        return gajiPokok;
    }

    // Metode untuk mencetak informasi pegawai
    public void cetakInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("Gaji Pokok: " + gajiPokok);
    }
}
```

![Implementasi Code Pegawai](Screenshot/Main%20n%203%20Class/Class%20Pegawai%201.png)
![Implementasi Code Pegawai](Screenshot/Main%20n%203%20Class/Class%20Pegawai%202.png)

### Class Programmer

```java
public class Programmer extends Pegawai {
    private double tunjangan;
    private double bonus;

    // Setter untuk tunjangan
    public void setTunjangan(double tunjangan) {
        this.tunjangan = tunjangan;
    }

    // Getter untuk tunjangan
    public double getTunjangan() {
        return tunjangan;
    }

    // Setter untuk bonus
    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    // Getter untuk bonus
    public double getBonus() {
        return bonus;
    }

    // Metode untuk mencetak informasi programmer
    @Override
    public void cetakInfo() {
        super.cetakInfo();
        System.out.println("Tunjangan: " + tunjangan);
        System.out.println("Bonus: " + bonus);
    }

    // Metode untuk mencetak tunjangan
    public void cetakTunjangan() {
        System.out.println("Tunjangan Programmer: " + tunjangan);
    }

    // Metode untuk mencetak bonus
    public void cetakBonus() {
        System.out.println("Bonus Programmer: " + bonus);
    }
}
```

![Implementasi Code Class Programmer](Screenshot/Main%20n%203%20Class/Class%20Programmer%20%201.png)
![Implementasi Code Class Programmer](Screenshot/Main%20n%203%20Class/Class%20Programmer%202.png)

### Class Manager

```java
    // Kelas Manager yang merupakan turunan dari Pegawai
public class Manager extends Pegawai {
    private double tunjangan;
    private double bonus;

    // Setter untuk tunjangan
    public void setTunjangan(double tunjangan) {
        this.tunjangan = tunjangan;
    }

    // Getter untuk tunjangan
    public double getTunjangan() {
        return tunjangan;
    }

    // Setter untuk bonus
    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    // Getter untuk bonus
    public double getBonus() {
        return bonus;
    }

    // Metode untuk mencetak informasi manager
    @Override
    public void cetakInfo() {
        super.cetakInfo();
        System.out.println("Tunjangan: " + tunjangan);
        System.out.println("Bonus: " + bonus);
    }

    // Metode untuk mencetak tunjangan
    public void cetakTunjangan() {
        System.out.println("Tunjangan Manager: " + tunjangan);
    }

    // Metode untuk mencetak bonus
    public void cetakBonus() {
        System.out.println("Bonus Manager: " + bonus);
    }

}
```

![Implementasi Code Class Manager](Screenshot/Main%20n%203%20Class/Class%20Manager%201.png)
![Implementasi Code Class Manager](Screenshot/Main%20n%203%20Class/Class%20Manager%202.png)

## Output Praktikum

Output dari 3 class yang berbeda dalam 1 package 

![Output Praktikum](Screenshot/Main%20n%203%20Class/Output%202.png)