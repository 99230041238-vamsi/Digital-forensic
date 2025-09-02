**EXPERIMENT -3**

**Wireshark**

**Network Packet Capture and Analysis Tool**

**Installation:**

**Windows:** <https://www.wireshark.org/download.html>

**Mac :** <https://www.wireshark.org/download.html>

**Linux:** preinstalled in kali else download source code from same
website

**Procedure:**

**Step 1: Start Capturing Packets**

-   First, open Wireshark. You will see a list of all available network
    interfaces (e.g., \"Wi-Fi,\" \"Ethernet\").

-   Select the interface your computer is using to connect to the
    internet (in this case, Wi-Fi).

-   Click the blue shark fin icon 🦈 in the top-left corner to start the
    capture. Wireshark will immediately begin capturing all traffic
    passing through that interface.
    <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f3c28ed3-64c1-4c04-8627-0796a7bfb27b" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/68d20206-82a6-4569-b8b9-d5f834a6e63b" />

> **Step 2: Generate Login Traffic**

-   Open a web browser and navigate
    to <http://testphp.vulnweb.com/login.php>.

-   Enter any dummy credentials. For this example, we\'ll use:

Username: testuser

Password: password123

-   Click the login button. The login will fail, but the data has
    already been sent across the network.
    <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/dc92095e-ab95-4200-8e45-cc48adf0f37d" />

**step 3: Stop Capture and Filter Traffic**

-   Return to Wireshark and click the Stop button (the red square).

-   In the display filter bar, you need to find the packet containing
    the login data. Since the form data was sent to the server, we will
    look for an HTTP POST request.

-   Apply the following filter to find the exact packet and press Enter:
-   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/c0b06bfc-ced1-4830-843e-d6f2f98a3dc1" />



**step 4: Inspect the Packet to Find Credentials**

-   In the filtered packet list, you should see a packet with
    information like \"POST /userinfo.php\". Select this packet.

-   In the Packet Details pane below the list, expand the following
    sections:

Hypertext Transfer Protocol HTML Form URL EncodedInside the \"HTML Form
URL Encoded\" section, you will see the credentials you entered in
plaintext.
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/87e87b46-5f12-457c-ae72-1852744ba531" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/4919e119-89d4-41c8-8b75-59ea49bf7e4f" />
**Result**

The experiment successfully intercepts the login credentials in a
human-readable format. The analysis of the captured POST packet reveals
the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol.
Any sensitive data sent over HTTP is transmitted openly, making it
trivial to intercept.
