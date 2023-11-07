Ciopa Cristian-Mihai 341C2




1
code-ul script-ului:

#!/usr/bin/env python3
# Giff me za flag!

import os
import base64
from Crypto.Cipher import AES
from Crypto.Util import number

BLOCK_SIZE = 32

if __name__ == "__main__":

    #task1

    # print(base64.encodebytes(c).decode("ASCII"))
    # shared = 33575766774760666026995348518731262982152328583169238317898593012848377955850
    # key = shared.to_bytes((shared.bit_length() + 7) // 8, byteorder='big')[0:BLOCK_SIZE]
    # cipher = AES.new(key, AES.MODE_ECB)
    # print(cipher.decrypt(base64.b64decode("sbUaUT/rfOjcCzj4ZED6BfIYjVvYWelMbIAPzTBqGTKtqZGriWlIIQSl/NjPuMO3Iz/cay9hFyMUmqgL0jRfIA==")))

    


folosesc o ecuatie pe hartie si vad o asemnare:

my_pub = pow(g, my_priv, p)
shared= pow(2, my_priv, p)

sbUaUT/rfOjcCzj4ZED6BfIYjVvYWelMbIAPzTBqGTKtqZGriWlIIQSl/NjPuMO3Iz/cay9hFyMU
mqgL0jRfIA==

\xb1\xb5\x1aQ?\xeb|\xe8\xdc\x0b8\xf8d@\xfa\x05\xf2\x18\x8d[\xd8Y\xe9Ll\x80\x0f\xcd0j\x192\xad\xa9\x91\xab\x89iH!\x04\xa5\xfc\xd8\xcf\xb8\xc3\xb7#?\xdck/a\x17#\x14\x9a\xa8\x0b\xd24_ 

R: SpeishFlag{vmBRBkJnXppT7nTK3gIQndX268gQb5bn}

2

m am plimbat prin foldere pana am dat de usr local bin pentru ca asa zicea in hint uri
am gasit binarul robot sudo care poate fi rulat ca alt user
dau strings.robotsudo
gasesc path de configurare path/usr/share/vim/talent/robosudo.conf
dau cat
allow roombax usr/src ...
allow janitor /usr/local
imi dau seama de aici ca se poate aduga un sufix (cum este mentionat si in hint)
trebuie sai zic practic prima linie de sintaxa
creez vacuum-controla si in el imi deschid un nou bash in care sunt userul roombax
ii dau chmod +x dupa dau robot-sudo usr/local/bin/vacuum-controla/
aacum sunt rombax si folosesc ltrace ca sa vad ca este un strcmp in spate cu o cheie si cand dau match pe ea primesc obraznicul acesta
---->

R: SpeishFlag{r0hjV5WZiBBYmhuhhTey8eFtg8rpHkcF}

3
