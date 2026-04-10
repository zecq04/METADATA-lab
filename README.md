# Week 4: METADATA

## Tools learned:

1. `file`
2. `exiftool`
3. `hexeditor`
4. `binwalk`

---

## Task

| Picture | Tools | Link / Command | POC | Analysis |
|--------|------|----------------|-----|----------|
| Ocean.jpg | exiftool | https://exif.tools/<br>`exiftool ocean.jpg` | <img src="Screenshot 2026-04-10 221017.png" width="300"/> | Metadata analysis using exiftool reveals hidden information embedded within the image file. The "Comment" field contains a hidden message indicating the presence of a flag. This demonstrates that metadata can be used to hide sensitive or secret data without changing the visible content of the image. |
| solitaire.exe | file | `file solitaire.exe` | <img src="Screenshot 2026-04-10 233606.png" width="300"/> | The file command is used to identify the real file type. The result shows that "solitaire.exe" is actually a PNG image file instead of an executable. This proves that file extensions can be misleading and should always be verified using appropriate tools. |
| rubiks.jpg | file | `file rubiks.jpg` | <img src="Screenshot 2026-04-10 234820.png" width="300"/> | The analysis shows that the JPG file is actually stored as a PNG format. This indicates that the file extension has been modified to disguise its real type, which is a common technique in file obfuscation. |
| computer.jpg | hexeditor | `hexeditor computer.jpg` | <img src="Screenshot 2026-04-10 231318.png" width="300"/> | Hexeditor is used to analyse the raw binary content of the image file. By examining the file header and hexadecimal structure, we can identify the actual file format and detect any hidden or manipulated data. This method helps in verifying file integrity and uncovering hidden information. |
| dog.jpg | binwalk | `binwalk dog.jpg`<br>`binwalk -e dog.jpg`<br>`cd _dog.jpg.extracted/` | <img src="Screenshot 2026-04-10 231258.png" width="300"/> | Binwalk is used to scan and extract hidden data from the image file. The output reveals embedded files within the image, and extraction confirms the presence of hidden content. This demonstrates how steganography techniques can be used to conceal files inside images. |
