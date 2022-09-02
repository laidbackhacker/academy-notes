# Plasma Random Number Generation project - notes
## TODO
- Find Python hashing library
- Hash pixel sum
- Seed into mersenne twister

- View Base64 as binary
- Hash and seed

- Mix with default entropy source (system time)

- Investigate other RNG algs in python

- setup github repo

## Report
- picture of setup
- data flowchart
- how it works
- code snippets of different implementations
- sample data from both implementations - showing raw numbers and hashes
- results of randomness - scatter graphs comparing the outcomes
- known compromises made/how to improve
- what I've learned
- what went well
- references

Python Random module (Mersenne Twister) is not secure, uses linear recursion

Need a csprng with seeding

# Snippets
## Take image, sum pixel values
```python
import picamera
import picamera.array
import numpy
from PIL import Image

with picamera.PiCamera() as camera:
    with picamera.array.PiRGBArray(camera) as output:
        camera.resolution = (1600, 1600)
        camera.capture(output, 'rgb')
        pixelTotal = numpy.sum(output.array)
        print(pixelTotal)
```
## Mix pixel sum and time, hash, RNG
```python
import hashlib
import time
import numpy
from randomgen import ChaCha
pixelTotal=92239410
pixelTotal=int(str(pixelTotal)[1:])
mixedEntropy = str(bin(pixelTotal)[2:]) + str(bin(time.time_ns())[2:])
hashHex = hashlib.sha256(mixedEntropy.encode('ASCII')).hexdigest()
hashInt = int(hashHex, 16)
randomNum = numpy.random.Generator(ChaCha(seed=hashInt))
randomValue=randomNum.standard_normal()
print(randomValue)
```
## Mix image binary and time, hash, RNG
```python
import hashlib
import numpy
import cv2
import sys
import time
import PIL.Image as Image
from io import BytesIO
from randomgen import ChaCha

img=cv2.imread('capture.jpeg')
pil_im = Image.fromarray(img)
output = BytesIO()
pil_im.save(output, format="jpeg")
hex_data=output.getvalue()

mixedEntropy = str(bin(int.from_bytes(hex_data,byteorder=sys.byteorder))[2:]) + str(bin(time.time_ns())[2:])
hashHex = hashlib.sha256(str(mixedEntropy).encode('ASCII')).hexdigest()

hashInt = int(hashHex, 16)

randomNum = numpy.random.Generator(ChaCha(seed=hashInt))
randomValue=randomNum.standard_normal()
print(randomValue)
```
## Capture raw hex
```python
import picamera
import picamera.array
import numpy
from PIL import Image

with picamera.PiCamera() as camera:
    with picamera.array.PiRGBArray(camera) as output:
        camera.resolution = (1600, 1600)
        camera.capture(output, 'rgb')
        pil_im = Image.fromarray(output, mode="RGB")
		hexStream = BytesIO()
		pil_im.save(hexStream, format="jpeg")
		hex_data=hexStream.getvalue()
		print(hex_data)
        
```