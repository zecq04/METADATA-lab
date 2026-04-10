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
| Ocean.jpg | exiftool | https://exif.tools/<br>`exiftool ocean.jpg` | <img src="Screenshot 2026-04-10 221017.png" width="300"/> | Found hidden message in metadata (comment field). Shows image can hide data without changing appearance. |
| computer.jpg | hexeditor | `hexeditor computer.jpg` | <img src="Screenshot 2026-04-10 233606.png" width="300"/> | Checked file header in hex. Can see real structure and detect if file is modified. |
| dog.jpg | binwalk | `binwalk dog.jpg`<br>`binwalk -e dog.jpg`<br>`cd _dog.jpg.extracted/` | <img src="Screenshot 2026-04-10 231258.png" width="300"/> | Found embedded file inside image. After extract, hidden content is visible. |
| rubiks.jpg | file | `file rubiks.jpg` | <img src="Screenshot 2026-04-10 231318.png" width="300"/> | File type not match extension. Actually PNG, not JPG. |
| solitaire.exe | file | `file solitaire.exe` | <img src="Screenshot 2026-04-10 234820.png" width="300"/> | Not an exe file. It is actually an image (PNG). |
