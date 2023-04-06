On Android 6 and higher, you can select your client certificate on the connection screen. 
It must be installed on your device as a "VPN and apps" certificate. 
If you use a self-signed certificate for your server, you'll also have to install your own CA certificate.

Bundle your client certificate and its private key into a PKCS 12 file with the following commands:
```bash
# Combine the certificate and the key.
cat cert.pem key.pem > pkcs12.pem
# Create a password-protected bundle.
openssl pkcs12 -in pkcs12.pem -export -out bundle.p12
```
Download the `.p12` bundle to your device and install it by opening the file from a file explorer. 
Use "VPN and apps" type. Give the certificate a human-friendly name, it can be distinguished from others.

https://user-images.githubusercontent.com/5675681/230439919-6df5af1b-8092-49c7-9763-5dc307aa1b1b.mp4

<br>
Return to the gallery, select the installed certificate and connect to your library.

https://user-images.githubusercontent.com/5675681/230440485-d1c4308a-1757-40bd-bdcf-572882032ecb.mp4

<br>

**The gallery app doesn't store or decrypt your certificates. They are managed by Android keychain.**
**You can delete the downloaded `.p12` file, but do not remove the certificate from the Android settings.**