<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    <h1>OCR Uygulaması</h1>
    <p>Bu uygulama, resim dosyalarındaki metinleri OCR (Optik Karakter Tanıma) işlemi ile okuyarak bir Word dosyasına kaydeder.</p>
    <div class="section">
        <h2>Gereksinimler</h2>
        <ul>
            <li>Python 3.x</li>
            <li>Gerekli Python kütüphaneleri:
                <ul>
                    <li><code>pytesseract</code></li>
                    <li><code>Pillow</code></li>
                    <li><code>tkinter</code></li>
                    <li><code>python-docx</code></li>
                </ul>
            </li>
            <li><a href="https://github.com/tesseract-ocr/tesseract" target="_blank">Tesseract OCR</a> kurulu olmalıdır.</li>
        </ul>
    </div>
    <div class="section">
        <h2>Kurulum</h2>
        <ol>
            <li>Gerekli Python kütüphanelerini yükleyin:
                <pre><code>pip install pytesseract Pillow python-docx</code></pre>
            </li>
            <li>Tesseract OCR yazılımını indirin ve kurun. 
                <ul>
                    <li>Windows için: <a href="https://github.com/tesseract-ocr/tesseract/releases" target="_blank">Tesseract Releases</a></li>
                </ul>
            </li>
            <li><code>pytesseract.pytesseract.tesseract_cmd</code> değişkenini Tesseract'ın kurulu olduğu dizine göre ayarlayın.</li>
        </ol>
    </div>
    <div class="section">
        <h2>Kullanım</h2>
        <ol>
            <li>Uygulamayı çalıştırın:
                <pre><code>python ocr_app.py</code></pre>
            </li>
            <li>OCR işlemi yapmak istediğiniz resim dosyalarını seçin.</li>
            <li>İşlem tamamlandığında, sonuçları kaydetmek için bir Word dosyası seçin.</li>
            <li>OCR sonuçları seçtiğiniz Word dosyasına kaydedilecektir.</li>
        </ol>
    </div>
    <div class="section">
        <h2>Özellikler</h2>
        <ul>
            <li>Birden fazla resim dosyasını destekler.</li>
            <li>Türkçe ve İngilizce dil desteği (<code>lang="tur"</code> veya <code>lang="eng"</code>).</li>
            <li>OCR sonuçlarını Word formatında kaydeder.</li>
            <li>İlerleme durumu, kullanıcıya bir ilerleme çubuğu ile gösterilir.</li>
        </ul>
    </div>
    <div class="section">
        <h2>Kodun Temel Bölümleri</h2>
        <ul>
            <li><strong>OCR İşlemi:</strong> <code>perform_ocr(image_path)</code> fonksiyonu ile yapılır.</li>
            <li><strong>Dosya Seçimi:</strong> <code>filedialog.askopenfilenames()</code> ile kullanıcıdan dosya seçmesi istenir.</li>
            <li><strong>Sonuçları Kaydetme:</strong> OCR sonuçları Word belgesi olarak kaydedilir (<code>python-docx</code>).</li>
        </ul>
    </div>
    <div class="section">
        <h2>Önemli Notlar</h2>
        <ul>
            <li>Tesseract OCR kurulum dizini doğru bir şekilde belirtilmelidir:
                <pre><code>pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"</code></pre>
            </li>
            <li>Resim dosyaları, desteklenen formatlardan biri olmalıdır: <code>.png</code>, <code>.jpg</code>, <code>.jpeg</code>, <code>.bmp</code>.</li>
            <li>OCR işlemi sırasında doğru dili seçtiğinizden emin olun (<code>lang="tur"</code> veya <code>lang="eng"</code>).</li>
        </ul>
    </div>
<div class="section">
    <h2>Lisans</h2>
    <p>Bu proje açık kaynak olarak paylaşılmaktadır ve herhangi bir lisans ile sınırlandırılmamıştır. Dileyen herkes projeyi kullanabilir, değiştirebilir veya dağıtabilir.</p>
</div>

</body>
</html>
