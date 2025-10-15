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
List of Images with Steganography Detection Scores and File Signature Details
<img width="843" height="131" alt="image" src="https://github.com/user-attachments/assets/eea8d080-0559-4f0a-a2a8-4c5dce536353" />
<img width="1007" height="489" alt="image" src="https://github.com/user-attachments/assets/09340818-98bd-4df5-a665-dcd00b61cfef" />
<img width="721" height="189" alt="image" src="https://github.com/user-attachments/assets/aba712a7-67da-4be1-b803-6e8d0197edbc" />

<img width="1007" height="489" alt="image" src="https://github.com/user-attachments/assets/d8885a8d-e29a-4faf-b9f9-65c47f02aabd" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
