<!DOCTYPE html>
<html lang="id">

<head>
    <meta charset="UTF-8">
    <title>Enkripsi dan Dekripsi</title>
    <!-- Pustaka CryptoJS -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
</head>

<body>
    <h1>Enkripsi dan Dekripsi</h1>

    <!-- Formulir enkripsi -->
    <form id="encryption-form">
        <textarea id="input-text" placeholder="Masukkan teks di sini..." required></textarea>
        <button type="submit">Enkripsi</button>
    </form>

    <!-- Formulir dekripsi -->
    <form id="decryption-form">
        <textarea id="encrypted-text" placeholder="Masukkan teks terenkripsi di sini..." required></textarea>
        <button type="submit">Dekripsi</button>
    </form>

    <h2>Hasil:</h2>
    <textarea id="output-text" readonly placeholder="Hasil akan ditampilkan di sini..." style="width: 100%; height: 100px;"></textarea>

    <script>
        // Panjang kunci dan IV
        const keyLength = 32; // 256-bit
        const ivLength = 16; // 128-bit

        // Daftar karakter spesial dan simbol ASCII untuk disisipkan ke teks terenkripsi
        const specialCharacters = [
            '¶', '∆', '÷', '•', '√', 'π', '§', '£', '¢', '∞', '±', 'Ω', 'µ', '™', '©', '®', '¥', '†', '‡', '‰', '√', '∞'
        ];

        // Fungsi untuk menyisipkan karakter spesial dan simbol ASCII ke dalam teks terenkripsi
        function injectSpecialCharacters(text) {
            const numberOfCharacters = Math.floor(Math.random() * 10) + 1; // Tentukan jumlah karakter yang disisipkan

            for (let i = 0; i < numberOfCharacters; i++) {
                const randomIndex = Math.floor(Math.random() * specialCharacters.length);
                const randomPosition = Math.floor(Math.random() * text.length);

                // Sisipkan karakter spesial ke dalam teks
                text = text.slice(0, randomPosition) + specialCharacters[randomIndex] + text.slice(randomPosition);
            }

            return text;
        }

        // Fungsi untuk menghapus karakter spesial dari teks
        function removeSpecialCharacters(text) {
            // Menghapus karakter spesial dari teks
            const specialCharPattern = /[¶∆÷•√π§£¢∞±Ωµ™©®¥†‡‰√∞]/g;
            return text.replace(specialCharPattern, '');
        }

        // Fungsi untuk enkripsi
        function encrypt(text) {
            const key = CryptoJS.lib.WordArray.random(keyLength);
            const iv = CryptoJS.lib.WordArray.random(ivLength);
            const encrypted = CryptoJS.AES.encrypt(text, key, { iv: iv });

            // Gabungkan IV, kunci, dan data terenkripsi
            let output = iv.toString() + key.toString() + encrypted.toString();

            // Sisipkan karakter spesial ke dalam teks terenkripsi
            output = injectSpecialCharacters(output);

            return output;
        }

        // Fungsi untuk dekripsi
        function decrypt(text) {
            // Buang karakter spesial dari teks
            text = removeSpecialCharacters(text);

            // Ekstrak IV, kunci, dan data terenkripsi
            const ivString = text.slice(0, ivLength * 2);
            const keyString = text.slice(ivLength * 2, ivLength * 2 + keyLength * 2);
            const encryptedData = text.slice(ivLength * 2 + keyLength * 2);

            // Konversi IV dan kunci ke format WordArray
            const iv = CryptoJS.enc.Hex.parse(ivString);
            const key = CryptoJS.enc.Hex.parse(keyString);

            // Dekripsi data
            const decrypted = CryptoJS.AES.decrypt(encryptedData, key, { iv: iv });

            return decrypted.toString(CryptoJS.enc.Utf8);
        }

        // Event listener untuk formulir enkripsi
        document.getElementById('encryption-form').addEventListener('submit', function (event) {
            event.preventDefault();
            const inputText = document.getElementById('input-text').value;
            const encryptedText = encrypt(inputText);
            document.getElementById('output-text').value = encryptedText;
        });

        // Event listener untuk formulir dekripsi
        document.getElementById('decryption-form').addEventListener('submit', function (event) {
            event.preventDefault();
            const encryptedText = document.getElementById('encrypted-text').value;
            const decryptedText = decrypt(encryptedText);
            document.getElementById('output-text').value = decryptedText;
        });
    </script>
</body>

</html>
