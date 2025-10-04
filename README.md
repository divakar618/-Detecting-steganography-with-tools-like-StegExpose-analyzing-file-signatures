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

<img width="907" height="450" alt="Screenshot 2025-10-04 112155" src="https://github.com/user-attachments/assets/3c095f1e-8db7-4eb9-9636-f215d459a3a2" /><img width="808" height="131" alt="Screenshot 2025-10-04 130642" src="https://github.com/user-attachments/assets/5026f8e5-50cd-46c7-b64c-7ed465fe37f4" /><img width="820" height="39" alt="Screenshot 2025-10-04 131000" src="https://github.com/user-attachments/assets/9d93d9a1-df23-450d-bb02-22a3627f2776" /><img width="1275" height="522" alt="Screenshot 2025-10-04 130119" src="https://github.com/user-attachments/assets/948e713e-a336-4759-8a61-ccc1805659af" />







## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
