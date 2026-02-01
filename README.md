```python
# QR-code-generator-using-python
import qrcode

#data i want to store in qr code
data = "https://www.snapchat.com/add/aniketsingh_782?share_id=GPEcP3HPxOA&locale=en-GB"

#create Qr code object
qr = qrcode.QRCode(
    version = 1, #control the size of qr code
    error_correction = qrcode.constants.ERROR_CORRECT_H,
    box_size = 10,
    border = 4,
)

#add data
qr.add_data(data)
qr.make(fit = True)

#create an image
img = qr.make_image(fill_color = "black", back_color = "white")

#save the image
img.save("qrcode.png")

print("QR Code generated successfully")
```
