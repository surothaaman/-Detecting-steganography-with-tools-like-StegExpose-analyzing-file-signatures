# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
<img width="451" height="108" alt="image" src="https://github.com/user-attachments/assets/6d8a5abb-45bf-473b-822d-c48d1d9863d6" />

<img width="477" height="47" alt="image" src="https://github.com/user-attachments/assets/7ad7d1c0-1ac8-47b0-a66c-2a2128c244d0" />

<img width="523" height="188" alt="image" src="https://github.com/user-attachments/assets/a7233c4e-f903-4b01-9a2d-61ba17c6c248" />

<img width="927" height="73" alt="image" src="https://github.com/user-attachments/assets/f59f7e45-f39e-42df-af19-bc0267f81f32" />

<img width="927" height="112" alt="image" src="https://github.com/user-attachments/assets/bdd0deda-85e0-453a-a6a3-0c0c0136029a" />


## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
