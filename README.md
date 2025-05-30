# steganography
steganography
**steganography – Easy-to-Use Image Hiding Tool**  

Stego is a smart tool that lets you **hide secret files inside images** without anyone noticing. It uses **strong encryption** and clever tricks to keep your data safe and undetectable.  

### **Key Features**  
✔ **Strong Protection** – Your hidden file is locked with **military-grade encryption (AES-256 + RSA)**. Only someone with the right private key can unlock it.  
✔ **Compression** – Shrinks your file before hiding it, making it harder to detect.  
✔ **Smart Hiding Technique** – Scatters hidden data randomly in the image (using **LSB steganography**) so it doesn’t look suspicious.  
✔ **Keeps Filenames** – When you extract the file, it remembers the original name.  
✔ **Works Everywhere** – Runs on Windows, Mac, and Linux (just needs Python).  

---  

### **How to Install**  
1. **Download Stego**:  
   ```sh
   pip install -r requirements.txt
   ```  
2. **Generate Encryption Keys** (like a password pair):  
   - Run:  
     ```sh
     python generate_keys.py
     ```  
   - Enter a **strong passphrase** (this protects your private key).  
   - Two files will be created:  
     - `myprivatekey.pem` (keep this **secret!**)  
     - `mypublickey.pem` (share this to let others hide files for you).  

---  

### **How to Use**  

#### **1. Hide a File Inside an Image**  
```sh
python secret_pixel.py hide host.png secret.txt mypublickey.pem output.png
```  
- `host.png` = The image you hide the file in.  
- `secret.txt` = The file you want to hide.  
- `mypublickey.pem` = Your public key (for encryption).  
- `output.png` = The new image with the hidden file.  

#### **2. Extract a Hidden File**  
```sh
python secret_pixel.py extract output.png myprivatekey.pem [extracted.txt]
```  
- `output.png` = The image with the hidden file.  
- `myprivatekey.pem` = Your private key (to unlock the file).  
- `[extracted.txt]` = (Optional) Name for the extracted file. If left blank, it uses the original filename.  

---  

### **Why Stego is Safe & Hard to Detect**  
- **Encryption**: Uses **AES-256 + RSA** (like banks and governments).  
- **Random Hiding**: Data is scattered in the image using a secret pattern (seed).  
- **Works Best with PNG/BMP/TIFF** (lossless formats).  
- **Avoids Suspicion**: Hides data in a way that steganalysis tools (like `zsteg`) can’t easily find.  

---  

### **Want to Help Improve Stego?**  
You can:  
- Report bugs or suggest features.  
- Help with code improvements (send a **Pull Request**).  
- Fix/improve documentation.  

---  

### **Final Thoughts**  
Stego is a **powerful yet simple** way to hide files inside images securely. Whether for privacy, security, or fun, it keeps your data **hidden and safe** from prying eyes.  

🚀 **Get started now and hide your secrets like a pro!**
