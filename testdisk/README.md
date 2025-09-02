**Experiment - 2**

**TestDisk: Open-Source Data Recovery Tool**

**recover a missing partition and repair a corrupted one using test
disk**

**Installation**

Linux : sudo apt-get install testdisk

macOS : brew install testdisk

Windows: Download the executable from the official website.

Link : <https://www.cgsecurity.org/wiki/TestDisk_Download>

**NOTE:-** if you using in windows please extract the .zip file first

**Procedure**

**1. Create a Log File**

-   Launch TestDisk from your terminal or command prompt using sudo
    testdisk (or testdisk_win.exe on Windows).

-   Select the \[Create\] option to generate a log file of the recovery
    session. This is helpful for future reference or troubleshooting.
    <img width="1099" height="626" alt="Image" src="https://github.com/user-attachments/assets/e26123a9-7e4e-4743-a00e-9230cb874392" />

**2. Select the Drive to Analyze**

-   TestDisk will display a list of all detected storage devices.

-   Use the Up/Down arrow keys to highlight the drive that contains your
    lost data.

-   Select \[Proceed\] to move to the next step.
-   <img width="1103" height="629" alt="Image" src="https://github.com/user-attachments/assets/c6018336-e1c6-41b9-bf26-e7d0884efe25" />

**3. Choose the Partition Table Type**

-   TestDisk will automatically suggest the most likely partition table
    type (e.g., Intel/PC, EFI GPT).

-   The default value is usually correct. Confirm the selection by
    pressing Enter.
    <img width="1083" height="633" alt="Image" src="https://github.com/user-attachments/assets/76f6d956-ab97-44f2-8a3c-c0701e73e64b" />
**4. Analyze Current Partition Structure**

-   From the main menu, choose \[Analyse\] and press Enter.

-   This will display the current partition table and check for errors
    or missing partitions.
    <img width="1103" height="631" alt="Image" src="https://github.com/user-attachments/assets/1e3a009c-ed03-4367-84a4-292dbba6a5d4" />

**5. Perform a Quick Search**

-   After the analysis, you will be prompted to perform a \[Quick
    Search\].

-   Select it and press Enter to scan the drive for lost partitions.

```{=html}
<!-- -->
```
-   Once a partition is found, you can press p to list its files.
    Deleted files and folders often appear in red.

-   Press q to return to the search results.

**6. Perform a Deeper Search**

-   If the Quick Search fails to find your lost partitions, select
    \[Deeper Search\]

-   This process can take a long time, as it scans the entire drive,
    block by block, to find remnants of partition structures.

```{=html}
<!-- -->
```
-   Again, use p to preview files and confirm if a found partition is
    the one you are looking for.

**7. Modify Partition Status**

-   After finding the correct partitions, use the Left/Right arrow keys
    to set their status.

-   Use **Left/Right arrow keys** to change status:

    -   **P**: Primary

    -   \***:** Bootable

    -   **L**: Logical

    -   **D**: Deleted

    -   **e**nsure that the partitions you want to recover are marked as
        Primary or Logical (and not deleted).

**8. Write the Partition Table**

-   Once you are confident the partition structure is correct, select
    \[Write\] from the menu.

-   Confirm the operation by pressing y (for yes). This will write the
    new partition table to your disk.

**9. Recover Files**

-   If you just need to recover a few files without fixing the partition
    table, you can do so from the file list (after pressing p).

-   Navigate to the folder containing your desired files.

-   Use the colon : key to select the files you want to recover.

-   Press the uppercase C key to copy the selected file(s).

-   Navigate to a safe destination on a different storage device and
    press uppercase C again to paste.

**10. Exit and Restart**

-   Once your task is complete, select \[Quit\] to exit the program.

-   If you wrote a new partition table to the drive, it is recommended
    to restart your computer to allow the operating system to recognize
    the changes.

**References:**

<https://www.cgsecurity.org/wiki/TestDisk_Download>

<https://www.cgsecurity.org/testdisk_doc/>
