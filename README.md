i#include <iostream>
using namespace std;

int a, b, pil, hasil;

int Penjumlahan ();
int Perkalian();
int Pengurangan ();
int Pembagian ():

int Penjumlahan () {
   cout<<endl<<endl;
   cout<<"--Anda Memilih Penjumlahan==\n"<<endl;
   cout<<"Masukkan Nilai Pertama : "; cin>>a;
   cout<<"Masukkan Nilai Kedua : "; cin>>b;
   
   hasil=a+b;
   
   cout<<"\nHasil Penjumlahan : "<<hasil<<endl<<endl;
}

int Perkalian () {
   cout<<endl<<endl;
   cout<<"--Anda Memilih perkalian==\n"<<endl;
   cout<<"Masukkan Nilai Pertama : "; cin>>a;
   cout<<"Masukkan Nilai Kedua : "; cin>>b;
   
   hasil=a*b;
   
   cout<<"\nHasil Perkalian : "<<hasil<<endl<<endl;
}

int Pengurangan () {
   cout<<endl<<endl;
   cout<<"--Anda Memilih Pengurangan==\n"<<endl;
   cout<<"Masukkan Nilai Pertama : "; cin>>a;
   cout<<"Masukkan Nilai Kedua : "; cin>>b;
   
   hasil=a-b;
   
   cout<<"\nHasil Penjumlahan : "<<hasil<<endl<<endl;

}

int Pembagian () {
	cout<<"\n\n";
	cout<<"--Anda Memilih Pembagian==\n"<<endl;
	cout<<"Masukan Nilai Pertama : "; cin>>a;
	cout<<"Masukan NIlai Kedua : "; cin>>b;
	
	hasil = a / b;
	
	cout<<"\nHasil Pembagian : "<<hasil<<endl<<endl;
}

int main () {
   cout<<"Kalkulator Sederhana : "<<endl;
   cout<<"1. Penjumlahan"<<endl;
   cout<<"2. Perkalian"<<endl;
   cout<<"3. Pengurangan"<<endl;
   cout<<"4. Pembagian"<<endl;
   
   cout<<"Pilihan : ";
   cin>>pil;
   
   switch (pil) {
      case 1: Penjumlahan (); break;
      case 2: Perkalian ();break;
      case 3: Pengurangan (); break;
      case 4: Pembagian (); break;
      
      default: cout<<"Pilihan Tidak Tersedia !!";
   }
}
