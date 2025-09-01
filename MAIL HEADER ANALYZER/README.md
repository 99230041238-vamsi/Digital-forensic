**EXPERIMENT -- 4**

**MHA**

**Mail Header Analyzer**

**Link:-** <https://mxtoolbox.com/EmailHeaders.aspx>

**Procedure**

**Step 1: Get the Email Header**

-   First, you need to copy the full, raw header from the email.

-   Gmail: Open the email, click the three dots (⋮), and select Show
    original.

-   Select all the text in the header and copy it.
-   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/6215b733-964a-488f-9dd1-b779e79040ca" />


**Step 2: Use a Mail Header Analyzer**

-   The easiest way to analyze the header is with an online tool.

-   Navigate to a site which analyze Email Header

-   Paste the entire header you copied into the analysis box.

-   Click the \"Analyze\" button to get a parsed, easy-to-read report.
-   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/4712cf18-7c3c-4769-ac51-e93c72c35b74" />
-   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/826e5ba0-e7a9-4b62-9fd4-0df584fcb163" />

> **Step 3: Analyze The Report**

-   This is the most critical step. In the analyzer\'s report, look for
    the SPF, DKIM, and DMARC results.
    <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3a3a3b8d-437e-4c06-9edd-197935f18607" />
    <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/974332d3-9eb8-499b-9bc9-b4e68fc54c65" />
    <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0f8e2d0b-69ad-4ef7-a8ec-bad0da071aca" />
-   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/84c15520-34a3-4f2a-9be1-16afcb50de09" />


**Review the Overall Delivery Summary**

-   First, look at the high-level summary to get an immediate sense of
    the email\'s status.

-   Check DMARC Compliance: The report shows the email is DMARC
    Compliant. This is the most important overall result.

-   Check SPF Status: Both SPF Authenticated and SPF Alignment passed.
    This means the sending server was authorized.

-   Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated
    failed (❌). This is a critical finding and indicates a problem with
    the email\'s digital signature.

**Investigate the SPF Record and Email Path**

-   Next, verify why the SPF check passed.

-   Examine the SPF Record: The SPF record for the domain is v=spf1
    include:mailgun.org \~all. This record explicitly authorizes servers
    from Mailgun to send emails on its behalf.

-   Trace the Relay Information: The delivery path shows the email was
    sent from m241-136.mailgun.net.

-   Conclusion: Since the email came from a Mailgun server, which is
    authorized in the SPF record, the SPF check passed.

**Analyze the DKIM Failure**

**References**
