# Gray-Algorithm-Python

```
from PIL import Image

image = Image.open("example.png")
width, height = image.size
pixel = image.load()

for x in range(width):
   for y in range(height):

        PIXEL_COLOR = pixel[x, y]

        TOTAL_COLOR = int(
            (PIXEL_COLOR[0] + PIXEL_COLOR[1] + PIXEL_COLOR[2]) / 3
        )

        image.putpixel(
            (x, y),
            (TOTAL_COLOR, TOTAL_COLOR, TOTAL_COLOR)
        )
```

- Image.Open ile resmimizi açtık ve image değişkenine atadık. 
- image.size ile resmimizin yüksekliğini ve genişliğini aldık.
- image.load() ise resmimizin pixel değerlerini tutar. Bunun sayesinde pixellere ulaşarak renk değerlerini alacağız.

```
for x in range(width):
   for y in range(height):
```
Burada resimdeki bütün pixelleri geziyoruz. Bunları x, y adında değişkenlerde tutuyoruz.

```
PIXEL_COLOR = pixel[x, y]
```
PIXEL_COLOR değişkeni bizim o anda bulunduğumuz pixelin renk değerini tutuyor.

```
        TOTAL_COLOR = int(
            (PIXEL_COLOR[0] + PIXEL_COLOR[1] + PIXEL_COLOR[2]) / 3
        )
```
Burası algoritmanın önemli olan kısmı. Burada RED, GREEN, BLUE değerlerini toplayıp 3'e bölüyoruz. Bilindiği gibi RGB renkleri (RED, GREEN, BLUE) bu şeklinden oluşuyor. Bizde bulunduğumuz pixeldeki rengi alarak bu algoritmaya yerleştiriyoruz. 
- Algoritmanın aslı şu şekilde:
```
Gray = (Red + Green + Blue) / 3
```

![Ekran Resmi 2021-12-08 00 56 56](https://user-images.githubusercontent.com/25556230/145112400-11e0c347-5689-4da0-b74c-513597fd6e02.png)
![Ekran Resmi 2021-12-08 00 57 14](https://user-images.githubusercontent.com/25556230/145112424-ebfb9ff1-269a-4aa6-a0a0-0c96ad85fdd1.png)


### KAYNAKLAR
1- https://tannerhelland.com/2011/10/01/grayscale-image-algorithm-vb6.html
