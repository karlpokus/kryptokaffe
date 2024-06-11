# sommaravslutningen

https://kryptokaffe.se/utmaningar/sommaravslutningen/

````sh
$ openssl dgst -sha256 sommaravslutningen.zip
2A93B15DA51C6E3123C9F513EF9F0A66FFB9DAAD974F557789A94DE8465C6375
$ file latte-lurifax.wav 
latte-lurifax.wav: RIFF (little-endian) data, WAVE audio, Microsoft PCM, 16 bit, stereo 48000 Hz
$ echo -n Fika | od -A n -t x1
 46 69 6b 61
$ hexdump -C latte-lurifax.wav | grep "46 69 6b 61"
````

Nope the hex is sung. Let's try a service:

# AWS transcribe API

````sh
# eng
"But the C 66 for six to 76 the foot, the 10, the 60 from there. But the f."
# swe
"det kommer speciellt till brudar det är trevligt för såna som mig. Det finns ju en anledning till att jag kallas för kladdkskassan ovan inom sektionen. F sextionio, sextio sextioett. Femtio sextio sjuttio Fyrtiotal, fyrtiotre Sextio sextio Femtio. fyrtiosex. fyrtiofem."
````

The spoken swedish is kinda ok but the hex is way off.

````sh
$ echo 69 60 61 50 60 70 40 43 60 60 50 46 45 | xxd -r -p
i`aP`p@C``PFE
````

Listening to the damn thing, this is as close as I come:

````sh
$ echo 46 69 6b 61 5d 50 6f 73 73 6f 6f 60 69 65 5d 45 | xxd -r -p
Fika]Possoo`ie]E
````

That's good enough.
