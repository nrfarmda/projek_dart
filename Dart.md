# program
```dart
// Operator Logika
void main() {

  // Map
  Map<String, int> nilaiSiswa = {
    "Ahmad": 80,
    "Budi": 70,
    "Cici": 90
  };

  // Function Opsional
  void cetakNilai(String nama, [int? nilai]) {
    if (nilai != null) {
      print("$nama memiliki nilai $nilai");
    } else {
      print("$nama tidak memiliki nilai");
    }
  }

  // Function Return Value
  int hitungRataRata(Map<String, int> nilaiSiswa) {
    int total = 0;
    for (var nilai in nilaiSiswa.values) {
      total += nilai;
    }
    return total ~/ nilaiSiswa.length;
  }

  // Anonymous Function
  var sapa = (String nama) => print("Halo, $nama!");
  
  // Closure
  Function tambah(int x) {
    return (int y) => x + y;
  }

  // Percabangan
  if (hitungRataRata(nilaiSiswa) >= 80) {
    print("Rata-rata nilai siswa adalah baik");
  } else {
    print("Rata-rata nilai siswa adalah kurang");
  }
  
  // Perulangan
  for (var siswa in nilaiSiswa.keys) {
    cetakNilai(siswa, nilaiSiswa[siswa]);
    sapa(siswa);
    var tambahDua = tambah(2);
    print("Hasil tambah dua: ${tambahDua(nilaiSiswa[siswa]!)}");
  }
}
```