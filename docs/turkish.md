# KT803 KT808 Csv File Description

**Sutün adı**|**Bilgi**|**Tanım**                                                       
--|--|--
id | Parça id|Her parçaya özgün id bulunmaktadır.
code | Profil kodu | Profil sayfasında tanımlanan profil kodu. Revolver pozisyonları profil koduna göre belirlenir Pozisyonları profil koduna göre
DATA2 | Parça barkodu | Benzersiz parça barkodu.Barkod tarandığında bu sütundaki parça ile eşleşir.
DATA11 | Dıştan dışa kanat yüksekliği | Menteşe pozisyonları kanat yüksekliğine göre hesaplanır.2000 mm kanat için DATA11 2000 olmalıdır.
DATA12 | Sağa veya sola açılım, menteşe sayısı | Menteşenin yönü ve pozisyonları değişeceğinden sol veya sağ açılım gereklidir.Menteşe delme ve vidalama pozisyonları operasyon sayfasından ayarlanır.Profilin başından sonuna kadar menteşe pozisyonu operasyon sayfasından belirlenir. H0101XX ve H0102XX makroları sabittir.Sadece aksesuar kodu (XX) değişebilir.
DATA13 | Eşik değer tipi | Threshold tanımlarındaki eşik kodudur. Menteşe konumları eşik yüksekliğine göre değişir.
DATA14 | Kapı kolu konumu | Profilin alt kısmından kol konumuna kadar olan mesafedir.1000 mm kapı kolu konumu için DATA14 değeri 1000 olmalıdır.
DATA15 | Menteşe rengi,ispanyolet tipi  menteşe tipi | Menteşe rengi bilgi amaçlı yazılır. İspanyolet tipi lock gear sayfasında tanımlanır ve sadece  kanat makinalarında bulunur.  Menteşe tipi operasyonlar sayfasında tanımlanır.
DATA16 | Transom | Profilde orta kayıt varsa seçilmelidir. 0:Transom yok, 1:Transom var

## DATA12 Makro Hakkında

Digit | Açıklama | Alınan Değerler
--|--|--
1..3 | Makro Sabit Kodu | H01
4..5 | Pencere açılımı yönü | 01 - Sol açılım, 02 - Sağ açılım
6..7 | Menteşe sayısı | max ?

### DATA12 için örnek

- H010103 : Sol Açılım, 3 Menteşe
- H010104 : Sol Açılım, 4 Menteşe
- H010203 : Sağ Açılım, 3 Menteşe
- H010204 : Sağ Açılım, 4 Menteşe 
  
H : Sabit , 01 : Tool kodu , 02 : Operasyon kodu 01 olursa sol 02 olursa sağ , 03 : Aksesuar kodu 

## DATA15 Hakkında

Sütun içindeki ayraç karakteri şudur: "|"  

Bölge | Açıklama | Kullanım alanı
--|--|--
1 | Menteşe Rengi | Ekranda görünmesi için bilgi
2 | Kilit kodu | Tanımlardaki aynı isimli aksesuardan veri almak için kullanılır.
3 | Menteşe Tipi | Tanımlardaki aynı isimli menteşeden veri almak için kullanılır.

### Örnek Kullanım
`DATA15`  
White | KUBU French Master | Hinge1

### DATA15 için örnek
- White|KUBU French Master|Hinge1 : Beyaz renkli, lock gear kodu KUBU French Master, menteşe tipi Hinge1

**İş dosyası örnek ----->>>** [KT8xx](./data.csv)
