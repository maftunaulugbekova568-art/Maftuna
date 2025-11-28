# Maftuna
loyihalar
Python 3 yordamida RPi GPIO dasturlash. Veb-kamera bilan ishlash.
Turli xil ranglar (formatlar) mavjud. OpenCV tasvirni kerakli formatga aylantirishning turli usullarini taklif etadi.
OpenCV - kompyuterni ko'rish va tasvirni qayta ishlash algoritmlari
kutubxonasi
 NumPy - bu katta ko'p o'lchovli massivlar va matritsalarni qo'llabquvvatlaydigan kutubxona bo'lib, ushbu massivlarda ishlash uchun yuqori
darajadagi (va juda tez) matematik funktsiyalarning katta kutubxonasi
Kutubxonalarni o'rnatish
"lib" bloknotini yaratamiz va OpenCV kutubxonalarini o'rnatamiz.
NumPy va Pytesseract ni ham o'rnatamiz
pip install numpy
pip install pytesseract 
bloknotni saqlaymiz.
"lib" bloknotini kompyuterga yuklab olamiz
1. Rasm yuklash:
Kod papkasida oldindan rasmlar papkasini yaratamiz va u yerga rasmni yuklaymiz
img = cv2.imread('images/OpenCV.jpg') # img o'zgaruvchisini yaratamiz 
va unga rasmni yuklaymiz
2. Rasmni ko'rsatish
cv2.imshow('Result', img) # Rasmni alohida oynada ko'rsatamiz, 
oynani 'Result' deb nomlaymiz
cv2.waitKey(0) # waitKey(10000) - oyna 10 soniya davomida 
ko'rsatiladi, waitKey(0) - cheksiz ko'rsatiladi
cv2.destroyAllWindows() # barcha oynalarni yopish
3. Tasvirni tanib olish va hajmini o'zgartirish
Terminalda tasvir o'lchamlarini ko'rsatamiz:
print (img.shape)
Terminal
(720,1200,3) # terminalda uchta element(balandlik, kenglik, qatlamlar 
soni), 3 ta qatlam-RGB dan iborat kortej ko'rsatiladi.
Kutubxonaga 
murojaat
tasvirni o’ziga 
yuklaydigan 
o'zgaruvchimiz
OpenCV kutubxonasiga 
rasmni o’qib olishi 
uchun murojaat qilamiz
Kerakli rasm manzili
Rasmning o'lchamini nomutanosib ravishda o'zgartiramiz:
img = cv2.resize(img, (300,500))
O'lchamni proportsional ravishda ikki baravar oshiramiz:
img = cv2.resize(img, (img.shape[1] // 2 ,img.shape[0] // 2)) # [0] -
balandlik, kortejdagi birinchi element, [1] – kenglik
