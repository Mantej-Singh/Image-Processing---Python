[![screenshot_1488389086.png](https://s19.postimg.org/w6hr757oz/screenshot_1488389086.png)](https://postimg.org/image/dqxa9qtkf/)
- - - -
# Image-Processing---Python



This notebook shows how using Python Imaging Library[PIL](https://pypi.python.org/pypi/Pillow/4.0.0) Library to find corrupted images in your local drive.

* Install `pip install Pillow` library.

- - - -

##Importing library to read data
```
from os import listdir
from PIL import Image
```


##Findding all *.PNG images
```
for filename in listdir('./'):
    if filename.endswith('.png'):
        print(filename, end='')
        print()
```

[![screenshot_1488389653.png](https://s19.postimg.org/3uw7a3nsj/screenshot_1488389653.png)](https://postimg.org/image/so5rar6sv/)



##Findding all *Currupt images
```
for filename in listdir('./'):
  if filename.endswith('.png'):
    try:
      img = Image.open('./'+filename) 
      img.verify()
    except (IOError, SyntaxError) as e:
      print('Bad file:', filename)
```

[![screenshot_1488389752.png](https://s19.postimg.org/4loxfvq5v/screenshot_1488389752.png)](https://postimg.org/image/vwa8nst2n/)

- - - -
- - - -


##Currupted Images :

[![screenshot_1488387919.png](https://s19.postimg.org/dn3gtho37/screenshot_1488387919.png)](https://postimg.org/image/bij3semgf/)

[![screenshot_1488388613.png](https://s19.postimg.org/w3xvkb41f/screenshot_1488388613.png)](https://postimg.org/image/gv7y6jacv/)
