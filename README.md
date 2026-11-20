# PDF Password Recovery Lab — NetworkWalks

## Overview

This repository documents a **hands-on cybersecurity training exercise** involving password-protected PDF files. The objective was to recover the correct passwords, unlock the challenge PDFs, and capture the completion flags.

The screenshots record password recovery using **Johnny (the graphical interface for John the Ripper)** and a **browser-based PDF hash extraction/password-testing workflow**, followed by NetworkWalks challenge-completion screens.

> **Scope:** This write-up is for authorized training and CTF/lab material only.

## Objective

- Identify the password protection on the provided PDF challenge files.
- Obtain a format suitable for password testing.
- Recover the correct passwords using password-cracking tools.
- Open the protected PDFs and capture the flags.
- Document the outcome with screenshots.

## Tools shown

| Tool | Role in the exercise |
| --- | --- |
| **Johnny / John the Ripper Jumbo** | Tested the PDF password hash and displayed a recovered password. |
| **PDF hash extraction webpage** | Extracted a John/Hashcat-compatible PDF hash from an encrypted PDF. |
| **Browser-based password tester** | Tried candidate passwords and displayed successful matches. |
| **NetworkWalks challenge PDFs** | Training material that displayed completion flags after access. |

## Walkthrough and evidence

### 1. Configure John the Ripper through Johnny

Johnny was configured to use the John the Ripper Jumbo executable. The application detected the installed executable.

![Johnny configuration showing the John the Ripper executable](screenshots/01-johnny-configuration.png)

### 2. Recover a PDF password with Johnny

The Johnny results window showed a successful PDF password recovery: `good-luck`.

![Johnny password table showing recovered password](screenshots/02-johnny-password-recovered.png)

### 3. Extract a password-testable PDF hash

Another screenshot shows an encrypted NetworkWalks PDF being processed by a PDF hash extraction webpage. The page displayed a hash in the `$pdf$...` format, described as compatible with PDF password-recovery tools.

![PDF hash extraction from a locked training PDF](screenshots/07-pdf-hash-extraction.png)

### 4. Recover passwords with a browser-based tester

The password tester screenshots show two additional successful matches: `password1` and `1qaz2wsx`.

**Recovered password: `password1`**

![Browser-based PDF password test showing password1](screenshots/06-browser-password-recovered-password1.png)

**Recovered password: `1qaz2wsx`**

![Browser-based PDF password test showing 1qaz2wsx](screenshots/08-browser-password-recovered-1qaz2wsx.png)

### 5. Capture the challenge flags

The following screenshots show three NetworkWalks congratulations/flag screens. These are the captured results of the lab exercise.

**Flag screenshot 1**

![First captured NetworkWalks flag](screenshots/03-networkwalks-flag-1.png)

**Flag screenshot 2**

![Second captured NetworkWalks flag](screenshots/04-networkwalks-flag-2.png)

**Flag screenshot 3**

![Third captured NetworkWalks flag](screenshots/05-networkwalks-flag-3.png)

## Results

| Evidence | Result |
| --- | --- |
| Johnny / John the Ripper | Recovered PDF password: `good-luck` |
| Browser password test — first result | Recovered PDF password: `password1` |
| Browser password test — second result | Recovered PDF password: `1qaz2wsx` |
| NetworkWalks | Three captured completion-flag screens |

**Outcome:** The screenshots demonstrate successful password recovery and captured challenge flags. They do not establish which recovered password corresponds to each individual flag, so no password-to-flag mapping is claimed here.

## Repository structure

```text
.
├── README.md
└── screenshots/
    ├── 01-johnny-configuration.png
    ├── 02-johnny-password-recovered.png
    ├── 03-networkwalks-flag-1.png
    ├── 04-networkwalks-flag-2.png
    ├── 05-networkwalks-flag-3.png
    ├── 06-browser-password-recovered-password1.png
    ├── 07-pdf-hash-extraction.png
    └── 08-browser-password-recovered-1qaz2wsx.png
```

## Notes

- This is a **documentation-only** repository for a completed training exercise; it does not include a password-cracking application.
- Before publishing this repository publicly, check whether the training provider permits publishing recovered passwords and challenge flags. The screenshots contain both.
- No original locked PDF file or wordlist was provided for this write-up, so those are not included.
