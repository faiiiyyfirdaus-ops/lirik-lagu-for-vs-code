import time
import sys

delay_per_huruf = 0.09  
delay_per_baris = 1.5  

def ketik_per_huruf(teks, delay):
    for huruf in teks:
        sys.stdout.write(huruf)
        sys.stdout.flush()
        time.sleep(delay)
    print()

def tampilkan_transisi(teks="Transisi masuk...", titik=5, delay=0.4):
    print()
    ketik_per_huruf(f"[{teks}]", 0.07)
    for _ in range(titik):
        sys.stdout.write(".")
        sys.stdout.flush()
        time.sleep(delay)
    print("\n")
    time.sleep(1.2)  # jeda setelah transisi

def tampilkan_lirik(lirik, default_huruf, default_baris):
    for baris in lirik:
        huruf_delay = baris.get("huruf_delay", default_huruf)
        baris_delay = baris.get("baris_delay", default_baris)
        ketik_per_huruf(baris["teks"], huruf_delay)
        time.sleep(baris_delay)

lirik_bagian = [
    {"teks": "Dunia pasti ada akhirnya", "huruf_delay": 0.13, "baris_delay": 2.7},
    {"teks": "Bintang-bintang pun ada umurnya", "huruf_delay": 0.12, "baris_delay": 2.7},
    {"teks": "Maka tenang saja, kita di sini berdua", "huruf_delay": 0.11, "baris_delay": 4.5},
    {"teks": "Nikmati sementara yang ada", "huruf_delay": 0.13, "baris_delay": 3.5}
]

if __name__ == "__main__":
    print("\n" + "" * 60 + "\n")
    tampilkan_transisi("")
    tampilkan_lirik(lirik_bagian, delay_per_huruf, delay_per_baris)
    print("\n" + "" * 60 + "\n")
