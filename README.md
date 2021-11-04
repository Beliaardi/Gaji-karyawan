# Gaji-karyawan
membuat data gaji karyawan menggunakan python

print("Program Hitung Gaji Karywan")
print("===============================================")
NamaKaryawan=input("Masukan Nama       :")
Goljab=input("Golongan Jabatan (1,2,3)  :")
Golpen=input("Pendidikan (SMA/D1/D3/S1) :")
JamKer=int(input("Masukan jumlah Jam Kerja  :"))


# Menghitung golongan Jabatan
gajipokok=300000
if Goljab==("1"):
    Tunjanganjabatan=0.05*gajipokok
elif Goljab==("2"):
        Tunjanganjabatan=0.10*gajipokok
elif Goljab==("3"):
         Tunjanganjabatan=0.15*gajipokok  
else:
    Tunjanganjabatan=0


# Menghitung golongan Pendidikan 
if Golpen=="SMA":   
    Tunjanganpendidikan=0.025*gajipokok
elif Golpen=="D1":
    Tunjanganpendidikan=0.5*gajipokok
elif Golpen=="D3":
    Tunjanganpendidikan=0.2*gajipokok
elif Golpen=="S1":
    Tunjanganpendidikan=0.3*gajipokok
else:
    Tunjanganpendidikan=0

# rumus
if(JamKer >= 8):
    UpahLembur= (JamKer-8)*3500
else:
    UpahLembur= 0

totalgaji= gajipokok + Tunjanganjabatan + Tunjanganpendidikan + UpahLembur

print("")
print("Karyawan yang bernama    ",NamaKaryawan)
print("Honor yang diterima")
print("     Tunjangan Jabatan        Rp.",Tunjanganjabatan)
print("     Tunjangan Pendididkan    Rp.",Tunjanganpendidikan)
print("     Honor lembur             Rp.",UpahLembur)
print("                         Rp,========================+")
print("Total Gaji               Rp.",totalgaji)
