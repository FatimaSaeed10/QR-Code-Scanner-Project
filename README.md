# QR-Code-Scanner-Project
This Python project allows users to scan and decode QR codes using the computer's webcam or an image file.

# Must Have to install these two packages

!pip install qrcode
!pip install image

import qrcode
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)
Data = "Done(U+1F603	)"
qr.add_data(Data)
qr.make(fit=True)

img = qr.make_image(fill_color="black", back_color="white")
img.save("qrcode.png")


Output

![image](https://user-images.githubusercontent.com/126961974/224959437-2e45c571-e60b-4c98-bbdd-2be0844ff860.png)

