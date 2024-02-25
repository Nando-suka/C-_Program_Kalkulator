// tantangan2.cpp
// Membuat Program batu,gunting, dan kertas
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main ()
  {

     cout << "Selamat datang dalam permainan batu, gunting, kertas! \n";
     while (true) {
     srand (time (0));
     // Memasukkan tipe data yang dibutuhkan
     int n;
     string pilihan,konfirmasi;
     string daftar [4] = {"","batu","gunting","kertas"};
     n = rand () % 3 + 1;

     cout << endl;
     cout << endl;

     cout << "Silahkan pilih (batu, gunting, atau kertas): ";
     cin  >> pilihan;
     cout << endl;

     cout << "Anda memilih: " << pilihan;
     cout << endl;
     cout << "Komputer memilih: " << daftar [n];
     cout << endl;
     cout << endl;

    if (daftar [n] == "batu" && pilihan == "kertas")
      {
        cout << "Anda menang! Kertas mengalahkan Batu\n";
      }
    else if (daftar [n] == "kertas" && pilihan == "batu")
     {
       cout << "Komputer menang! Kertas mengalahkan Batu\n";
     }
    else if (daftar [n] == "gunting" && pilihan == "kertas")
     {
       cout << "Komputer menang! Gunting mengalahkan Kertas\n";
     }
    else if (daftar [n] == "kertas" && pilihan == "gunting")
     {
       cout << "Anda menang! Gunting mengalahkan Kertas\n";
     }
    else if  (daftar [n] == "batu" && pilihan == "gunting")
     {
       cout << "Komputer menang! Batu mengalahkan Gunting\n";
     }
    else if (daftar [n] == "gunting" && pilihan == "batu")
     {
       cout << "Anda Menang! Batu mengalahkan Gunting\n";
     }
    else if (daftar [n] == "batu" && pilihan == "batu")
     {
      cout << "Hasilnya adalah seri! " << endl;
     }
    else if (daftar [n] == "kertas" && pilihan == "kertas")
     {
      cout << "Hasilnya adalah seri! " << endl;
     }
    else if (daftar [n] == "gunting" && pilihan ==" gunting")
     {
       cout << "Hasilnya adalah seri " << endl;
     }
    else {}
    cout << "\n\n";

    cout << "Apakah Anda ingin bermain lagi? (ya/tidak): ";
    cin  >> konfirmasi;
    if (konfirmasi != "ya" && konfirmasi != "Ya")
     {
         cout << endl;
         cout << "Terimaasih telah bermain!";
         cout << endl;
         break;
     }
     else {}
  }


     return 0;
  }

