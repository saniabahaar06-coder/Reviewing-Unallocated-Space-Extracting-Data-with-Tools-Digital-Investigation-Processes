# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="1542" height="862" alt="Screenshot 2026-09-07 230404" src="https://github.com/user-attachments/assets/516fb517-5c2b-4988-870d-04e9e9c5b6db" />


<img width="1542" height="862" alt="Screenshot 2026-09-07 230423" src="https://github.com/user-attachments/assets/a9c8beea-cb6e-4ebc-afd9-5355c2ef6e89" />
<img width="1542" height="862" alt="Screenshot 2026-09-07 230441" src="https://github.com/user-attachments/assets/4c2cfa11-3221-4ff9-aff2-f86a7456b938" />

<img width="1541" height="862" alt="Screenshot 2026-09-07 230505" src="https://github.com/user-attachments/assets/813b4610-8b33-4e4c-ba33-c5dfea6ff326" />
<img width="1545" height="822" alt="Screenshot 2026-09-07 230525" src="https://github.com/user-attachments/assets/0542b082-885a-49b4-af6c-c2d3c0c87113" />

<img width="1777" height="807" alt="Screenshot 2026-09-07 230542" src="https://github.com/user-attachments/assets/6157f921-7ae2-497b-aa19-fee9c5add6da" />
<img width="1872" height="807" alt="Screenshot 2026-09-07 230606" src="https://github.com/user-attachments/assets/9188ad96-50da-4ad3-9d55-422da0b672b9" />



## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

