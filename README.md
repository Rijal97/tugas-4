# tugas-4

**CODE PYTHON**

# Definisikan dua matriks 3x3
A = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

B = [
    [9, 8, 7],
    [6, 5, 4],
    [3, 2, 1]
]

# Fungsi untuk mengalikan dua matriks
def multiply_matrices(A, B):
    # Memeriksa ukuran matriks
    if len(A[0]) == len(B):  # Mengecek apakah kolom A sama dengan baris B
        # Inisialisasi matriks hasil C dengan nol
        C = [[0 for _ in range(len(B[0]))] for _ in range(len(A))]
        
        # Melakukan perkalian matriks
        for i in range(len(A)):
            for j in range(len(B[0])):
                for k in range(len(B)):
                    C[i][j] += A[i][k] * B[k][j]
        
        return C
    else:
        return "Perkalian matriks tidak dapat dilakukan"

# Eksekusi perkalian matriks
result = multiply_matrices(A, B)

# Menampilkan hasil
if isinstance(result, str):
    print(result)
else:
    print("Hasil perkalian matriks A dan B adalah:")
    for row in result:
        print(row)

**PSEUDOOCODE**

matriks A[3][3]
matriks B[3][3]
matriks C[3][3]

jumlah_kolom_A = 3
jumlah_baris_B = 3

Jika (jumlah_kolom_A == jumlah_baris_B) maka
    Untuk i dari 0 hingga 2 lakukan
        Untuk j dari 0 hingga 2 lakukan
            C[i][j] = 0
            Untuk k dari 0 hingga 2 lakukan
                C[i][j] += A[i][k] * B[k][j]
            Akhir Untuk
        Akhir Untuk
    Akhir Untuk
    tampilkan "Hasil perkalian matriks A dan B adalah: "
    tampilkan C
Jika tidak,
    tampilkan "Perkalian matriks tidak dapat dilakukan"


