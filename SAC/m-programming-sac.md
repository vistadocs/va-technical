![](media/image1.png)

# M Programming Standards and Conventions

***SAC***

The Department of Veterans Affairs M Programming Standards and
Conventions.

This document takes effect 11/1/2021. At that time all previous versions
are rescinded.

Table of Contents

[Revision History [3](#_Toc10635704)](#_Toc10635704)

[General Programming Standards and Conventions
[6](#_Toc10635705)](#_Toc10635705)

[**Definitions applicable to this document**
[6](#_Toc10635705)](#_Toc10635705)

[**Files** [7](#_Toc10635707)](#_Toc10635707)

[M Language Programming Standards and Conventions
[8](#_Toc10635708)](#_Toc10635708)

[**Routines (Routine structure and format)**
[8](#_Toc10635709)](#_Toc10635709)

[**Variables** [10](#_Toc10635710)](#_Toc10635710)

[**Commands** [16](#_Toc10635711)](#_Toc10635711)

[**Functions** [17](#_Toc10635712)](#_Toc10635712)

[**Name Requirements** [18](#_Toc10635713)](#_Toc10635713)

[**Options (Option file entries)** [18](#_Toc10635714)](#_Toc10635714)

[**Device Handling** [19](#_Toc10635715)](#_Toc10635715)

[**Miscellaneous** [19](#_Toc10635716)](#_Toc10635716)

[**Conventions** [19](#_Toc10635717)](#_Toc10635717)

[Interface Programming Standards and Conventions
[20](#_Toc10635718)](#_Toc10635718)

[**User Interface Standards for Scroll Mode and Screen Mode**
[20](#_Toc10635719)](#_Toc10635719)

[**User Interface Conventions for Scroll Mode and Screen Mode**
[21](#_Toc10635720)](#_Toc10635720)

[**User Interface Conventions for GUI Mode**
[22](#_Toc10635721)](#_Toc10635721)

**Revision History**[]{#_Toc10635704 .anchor}

+----------+---------------------------------+------------------------+
| **Date** | **Description**                 | **Author**             |
+----------+---------------------------------+------------------------+
| 9/1/2021 | Updated footer to include       | SACWG Members:         |
|          | SharePoint SACWG site.          |                        |
|          |                                 | Nien-Chin Ackerman     |
|          | Updated format to DOCX          |                        |
|          |                                 | Sid Dane               |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Debbie Trost           |
+----------+---------------------------------+------------------------+
| 4/1/2021 | Added 2.2.1.3 Site and          | SACWG Members:         |
|          | Programmer must be in Upper     |                        |
|          | Case.                           | Nien-Chin Ackerman     |
|          |                                 |                        |
|          | Updated 2.2.2.2 to limit number | Sid Dane               |
|          | of patches in 2^nd^ line, and   |                        |
|          | to maintain line length         | Ron DiMiceli           |
|          | requirements.                   |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 3/3/2021 | Added DILOCKTM to 2.3.1.3.2     | SACWG Members:         |
|          |                                 |                        |
|          |                                 | Nien-Chin Ackerman     |
|          |                                 |                        |
|          |                                 | Sid Dane               |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 1        | Added 2.3.5 Restricting access  | SACWG Members:         |
| 1/4/2020 | to Non-VistA globals            |                        |
|          |                                 | Bill Ackerman          |
|          | Added 2.2.16 Restricting the    |                        |
|          | inclusion of I.P. Addresses in  | Sid Dane               |
|          | routines                        |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 9/3/2020 | Added 2.5.1.5 Allowing 2^nd^    | SACWG Members:         |
|          | parameter for \$Query           |                        |
|          |                                 | Bill Ackerman          |
|          |                                 |                        |
|          |                                 | Sid Dane               |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 1        | Updated 2.1.1                   | SACWG Members:         |
| /23/2020 |                                 |                        |
|          | Updated 2.2.14                  | Bill Ackerman          |
|          |                                 |                        |
|          | Updated 2. Introductory         | Sid Dane               |
|          | Paragraph                       |                        |
|          |                                 | Ron DiMiceli           |
|          | Re-ordered Revision History     |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 9/4/2019 | Updated 2.2.1                   | SACWG Members:         |
|          |                                 |                        |
|          | Updated 2.3.1.6                 | Bill Ackerman          |
|          |                                 |                        |
|          | Updated and expanded 2.10.3     | Sid Dane               |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 6/5/2019 | Updated 2.2.14                  | SACWG Members:         |
|          |                                 |                        |
|          | Updated 2.2.15                  | Bill Ackerman          |
|          |                                 |                        |
|          |                                 | Sid Dane               |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | William Easter         |
|          |                                 |                        |
|          |                                 | Paul Harrod            |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 |                        |
|          |                                 | Non-Voting Members:    |
|          |                                 |                        |
|          |                                 | Mike Montali           |
+----------+---------------------------------+------------------------+
| 4/3/2018 | Update header and footer.       | Bill Ackerman          |
|          |                                 |                        |
|          | Updated SACC to SACWG           | Sid Dane               |
|          |                                 |                        |
|          | Updated Standards and           | Ron DiMiceli           |
|          | Conventions Committee to        |                        |
|          | Standards and Conventions Work  | Randy Morton           |
|          | Group.                          |                        |
|          |                                 | Rob Whelan             |
|          | Reviewed for 508 compliance.    |                        |
|          |                                 | Gregory Woodhouse      |
+----------+---------------------------------+------------------------+
| 1        | Updated 2.2.1                   | Bill Ackerman          |
| 1/9/2017 |                                 |                        |
|          | Clarification of first line     | Sid Dane               |
|          | format                          |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 |                        |
|          |                                 | Rob Whelan             |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
+----------+---------------------------------+------------------------+
| 5/5/2016 | Updated 2.2.1                   | Bill Ackerman          |
|          |                                 |                        |
|          | Clarification of first line     | Sid Dane               |
|          | format                          |                        |
|          |                                 | Ron DiMiceli           |
|          | Added 2.9.5                     |                        |
|          |                                 | Randy Morton           |
|          | Added Multidivisional           |                        |
|          | requirement.                    | Rob Whelan             |
|          |                                 |                        |
|          | It is required that             | Gregory Woodhouse      |
|          | applications function properly  |                        |
|          | in a multidivisional            |                        |
|          | environment. The SAC does not   |                        |
|          | specify what this means or how  |                        |
|          | multidivisional environment     |                        |
|          | beyond the high level           |                        |
|          | requirement that applications   |                        |
|          | must function correctly in an   |                        |
|          | environment supporting multiple |                        |
|          | divisions.                      |                        |
|          |                                 |                        |
|          | Updated 2.3.1.1                 |                        |
|          |                                 |                        |
|          | Local variable names may not    |                        |
|          | exceed sixteen characters.      |                        |
|          | Namespaced variables must be    |                        |
|          | all uppercase characters. All   |                        |
|          | other local variables can be    |                        |
|          | mixed case.                     |                        |
|          |                                 |                        |
|          | Updated 2.2.4                   |                        |
|          |                                 |                        |
|          | Routine names and Labels are    |                        |
|          | limited to sixteen (16)         |                        |
|          | characters (not including the   |                        |
|          | formal list for parameter       |                        |
|          | passing) and may not contain    |                        |
|          | lower case characters.          |                        |
+----------+---------------------------------+------------------------+
| 8        | Updated 2.3.3.2 to include      | Andrew Bakke           |
| /30/2012 | \$ROLES                         |                        |
|          |                                 | Albert Consentino      |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 | (Co-Chair)             |
|          |                                 |                        |
|          |                                 | Jerry Rutherford       |
|          |                                 |                        |
|          |                                 | Tammy Salewsky         |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Jesse Staab            |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 6/6/2012 | Added 2.5.1.4                   | Andrew Bakke           |
|          |                                 |                        |
|          |                                 | Albert Consentino      |
|          |                                 |                        |
|          |                                 | Ron DiMiceli           |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 | (Co-Chair)             |
|          |                                 |                        |
|          |                                 | Jerry Rutherford       |
|          |                                 |                        |
|          |                                 | Tammy Salewsky         |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Jesse Staab            |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 8        | Updated 2.2.4                   | Andrew Bakke           |
| /24/2011 |                                 |                        |
|          | Clarified the relationship      | Albert Consentino      |
|          | between routine names and       |                        |
|          | labels. Routine names, as well  | Ron DiMiceli           |
|          | as labels within routines, may  |                        |
|          | only be 8 characters.           | Randy Morton           |
|          |                                 | (Co-Chair)             |
|          |                                 |                        |
|          |                                 | Jerry Rutherford       |
|          |                                 |                        |
|          |                                 | Tammy Salewsky         |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Jesse Staab            |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 7/6/2011 | Updated 2.2.2                   | Andrew Bakke           |
|          |                                 |                        |
|          | Removed the spaces before       | Albert Consentino      |
|          | Package Name, the patch         |                        |
|          | listing, and the Version Date   | Ron DiMiceli           |
|          | to make the requirement and the |                        |
|          | example consistent.             | Randy Morton           |
|          |                                 | (Co-Chair)             |
|          |                                 |                        |
|          |                                 | Jerry Rutherford       |
|          |                                 |                        |
|          |                                 | Tammy Salewsky         |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Jesse Staab            |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 2/9/2011 | Updated 2.2.3                   | Andrew Bakke           |
|          |                                 |                        |
|          | Changed the reference to the    | Albert Consentino      |
|          | directive                       |                        |
|          |                                 | Ron DiMiceli           |
|          | Updated 2.2.5 and 2.3.1.1       |                        |
|          |                                 | Randy Morton           |
|          | Modified casing requirements    | (Co-Chair)             |
|          | for local variables.            |                        |
|          |                                 | Jerry Rutherford       |
|          |                                 |                        |
|          |                                 | Tammy Salewsky         |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Jesse Staab            |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 5/1/2008 | Added 2.2.6.3                   | Added 2.2.6.3          |
|          |                                 |                        |
|          | Added "and must be in patch     | Added "and must be in  |
|          | release order" to 2.2.2.2       | patch release order"   |
|          |                                 | to 2.2.2.2             |
|          | Corrected font in the           |                        |
|          | description for Actual List     | Corrected font in the  |
|          |                                 | description for Actual |
|          | Added number sequence to Files  | List                   |
|          | section                         |                        |
|          |                                 | Added number sequence  |
|          |                                 | to Files section       |
+----------+---------------------------------+------------------------+
| 1        | Approved                        | David Alexander        |
| 2/5/2007 |                                 |                        |
|          |                                 | Wally Fort             |
|          |                                 |                        |
|          |                                 | Debbi Lawson (CACI)    |
|          |                                 |                        |
|          |                                 | Randy Morton           |
|          |                                 | (Co-Chair)             |
|          |                                 |                        |
|          |                                 | Jean Sheppard          |
|          |                                 |                        |
|          |                                 | Gregory Woodhouse      |
|          |                                 | (Chair)                |
+----------+---------------------------------+------------------------+
| 7        | Revised                         | SACC Committee         |
| /13/1999 |                                 |                        |
+----------+---------------------------------+------------------------+
| 1        | Adopted                         | SACC Committee         |
| /22/1996 |                                 |                        |
+----------+---------------------------------+------------------------+

1\. General Programming Standards and Conventions

The definitions, standards, and conventions within this section apply to
all programming and user environments in use in the Veterans Health
Information Systems and Technology Architecture (VistA). This includes
all applications that use commercial software products as an integral
part of VistA (but not to the commercial application itself unless the
commercial application is installed in the VistA environment) and to all
development environments including, but not limited to programming
languages such as M or Pascal and graphical user interface (GUI)
environments such as Delphi.

**Definitions Applicable to this Document**[]{#_Toc10635705 .anchor}

+------------------------+---------------------------------------------+
| > Term                 | > Definition                                |
+========================+=============================================+
| > Actual List          | > These are the actual values that are      |
|                        | > passed into an API or Supported Reference |
|                        | > by a caller. For example: when the        |
|                        | > variable DA is equal to 200, the 200 is   |
|                        | > the actual parameter used when \^DIE is   |
|                        | > called. A group of these values are the   |
|                        | > Actual List.                              |
+------------------------+---------------------------------------------+
| > CONVENTIONS          | > Programming guidelines which are designed |
|                        | > to promote consistency and safety across  |
|                        | > VistA applications. Exemptions from       |
|                        | > conventions are not required, but         |
|                        | > developers are strongly encouraged to     |
|                        | > follow them. It is also strongly          |
|                        | > recommended that the developer document   |
|                        | > any deviation from these conventions.     |
+------------------------+---------------------------------------------+
| > DBA                  | > Database Administrator                    |
+------------------------+---------------------------------------------+
| > DBIA                 | > DataBase Integration Agreement. See ICR.  |
+------------------------+---------------------------------------------+
| > EXEMPTION            | > Authority granted by the SACC to a        |
|                        | > specific version of a VistA application   |
|                        | > which allows that application to not      |
|                        | > comply with a particular section of the   |
|                        | > SAC for a specified timeframe.            |
+------------------------+---------------------------------------------+
| > EXTENSIONS           | > An addition, deletion, or modification to |
|                        | > the current Standards and Conventions     |
|                        | > document. Each extension will contain an  |
|                        | > appropriate effective date, and may       |
|                        | > optionally contain an expiration date or  |
|                        | > event. (The Programming SACC will update  |
|                        | > the SAC quarterly via extensions, which   |
|                        | > have the full weight of the original SAC. |
|                        | > Every effort will be made to keep all     |
|                        | > VistA development standards and           |
|                        | > conventions in one location.)             |
+------------------------+---------------------------------------------+
| > Formal List          | > These are the formal values that are      |
|                        | > passed into an API or Supported Reference |
|                        | > by a caller. For example: when the        |
|                        | > variable DA is equal to 200, DA is the    |
|                        | > formal parameter used when \^DIE is       |
|                        | > called. A group of these values are the   |
|                        | > Formal List.                              |
+------------------------+---------------------------------------------+
| > IA                   | > Integration Agreement. IAs can be         |
|                        | > accessed via the DBA menu on FORUM.       |
+------------------------+---------------------------------------------+
| > IAC                  | > Integration Agreement Committee           |
+------------------------+---------------------------------------------+
| > ICR                  | > Integration Control Registrations         |
|                        | > (Formerly Database Integration            |
|                        | > Agreements)                               |
+------------------------+---------------------------------------------+
| > Incremental Lock     | > Allows multiple locks on the same         |
|                        | > resource.                                 |
+------------------------+---------------------------------------------+
| > KERNEL               | > The Kernel is a set of software utilities |
|                        | > that form the foundation of VistA and     |
|                        | > include elements that start with the      |
|                        | > namespaces XG\*, XLF\*, XOB\*,            |
|                        | > XPD\*,XQ\*, XT\*, XU\*, XV\*, ZI\*, ZO\*, |
|                        | > ZT\*, ZU\*.                               |
+------------------------+---------------------------------------------+
| > Ls                   | > Refers to one or more spaces, or a single |
|                        | > tab character, at the beginning of the    |
|                        | > line or between the label and body of the |
|                        | > line.                                     |
+------------------------+---------------------------------------------+
| > MAILMAN              | > Mailman is a set of software utilities    |
|                        | > that form the foundation of VistA \'s     |
|                        | > electronic mail and communications and    |
|                        | > include elements that start with the      |
|                        | > namespace XM\*.                           |
+------------------------+---------------------------------------------+
| > NAMESPACE            | > A unique prefix of between 2 and 4 alpha  |
|                        | > characters assigned by the DBA.           |
+------------------------+---------------------------------------------+
| > NEW                  | > A way to create a new version of a        |
|                        | > variable either by explicit declaration   |
|                        | > or implicitly through parameter passing.  |
+------------------------+---------------------------------------------+
| > Non-Comment source   | > An executable line of code, or a line of  |
| > line                 | > text or data referenced by an executable  |
|                        | > line of code.                             |
+------------------------+---------------------------------------------+
| > PACKAGE              | > A set of routines, files, options,        |
|                        | > templates, security keys, screens,        |
|                        | > bulletins, functions, help frames, forms, |
|                        | > blocks, objects, protocols, dialogues,    |
|                        | > list templates, windows, etc. namespaced  |
|                        | > according to DBA requirements that        |
|                        | > function as a unit.                       |
+------------------------+---------------------------------------------+
| > SACWG                | > [Standards and Conventions Work           |
|                        | > Group](https://vaww.oed.portal.v          |
|                        | a.gov/communities/app_dev/sac/default.aspx) |
+------------------------+---------------------------------------------+
| > STANDARD             | > A rule which all VistA software must      |
|                        | > follow.                                   |
+------------------------+---------------------------------------------+
| > SUPPORTED REFERENCE  | > Documentation regarding routines, labels, |
|                        | > extrinsic functions, files, or global     |
|                        | > nodes that are accepted and documented by |
|                        | > the IAC for use by all packages.          |
|                        | > Supported references are listed on the    |
|                        | > DBA menu on FORUM.                        |
+------------------------+---------------------------------------------+
| > VA FileMan           | > The Database Management System for VistA, |
|                        | > with namespaces DD\*, DI\* and DM\*.      |
+------------------------+---------------------------------------------+
| > VistA                | > Veterans Health Information Systems and   |
|                        | > Technology Architecture                   |
+------------------------+---------------------------------------------+

**Files**[]{#_Toc10635707 .anchor}

Naming requirements for files used by VistA packages.

-   All VA FileMan files in the M Language environment must be number
    spaced in the number space assigned to the package by the DBA.

-   All Windows, DOS, VMS, or other host files created or exported as
    part of a VistA application shall be namespaced in the namespace
    assigned by the DBA.

-   Packages exporting script files should provide script files for all
    the terminal emulation packages commonly in use in the VA.

-   Packages exporting spreadsheet templates should apply protection to
    embedded formulas to prevent accidental deletion by a user.
    Spreadsheet templates should contain documentation describing the
    purpose of the template, complex functions, and user help.

2.  M Language Programming Standards and Conventions[]{#_Toc10635708
    .anchor}

All M-based VistA software will meet the following standards, and must
comply with the spirit of the conventions. When releasing a routine in a
defect repair or enhancement patch, all modules within the routine must
be compliant with current VA Standards and Conventions. This includes
lines of code not modified as part of the current effort. Tools such as
XINDEX should be run prior to, and frequently during, development and
maintenance activities.

1.  The 1995 ANSI/MDC X11.1 Sections 1 and 2 will be adhered to unless
    explicitly modified by this document.

2.  **Routines (Routine structure and format)**[]{#_Toc10635709 .anchor}

    1.  The first line of a routine must be in the following format:
        routine name\<ls\>;\[optional
        space\]site/programmer\<space\>-\<space\>brief description
        \[optional space\];\<space\>date of creation/edit

> Example: ZZAA12 ;DALOI/XXX -- Example Routine; May 01, 2017@13:36
>
> Updating the date of creation/edit is optional when updating an
> existing routine. If updated, inclusion of time is optional. The
> format of the date of last edit must be able to be interpreted by
> existing FileMan utilities. The use of existing Kernel date utilities
> to create the date of last edit is highly recommended. For example: S
> Y=\$\$FMTE\^XLFDT(\$\$NOW\^XLFDT) The local variable Y will be
> returned with the formatted date.

1.  The first line of a routine cannot contain the formal list for
    parameter passing.

2.  Routines generated by VA FileMan or Kernel and other compiled
    routines used in exporting a package, need not comply with this
    standard (i.e., 2.2.1).

3.  Site and Programmer must be in upper case

```{=html}
<!-- -->
```
2.  The second line of a routine must be in the following format:
    \[LABEL-optional\]\<ls\>;;version number;package
    name;\*\*p~m~,\...p~n~\*\*;version date;Build n where:

> ;;1.0;PACKAGE;\*\*p~m~,...p~n~\*\*;Feb 1, 2007;Build 1

1.  The version number must be the same on all of the package-namespaced
    routines.

2.  p~m~,\...p~n~ are the applied patch numbers, in order of patch
    release, separated by commas and must be in patch release order.
    This \";\" piece is null if there are no patches.

-   If the addition of a new patch number forces the line to exceed the
    number of characters allowed in paragraph 2.2.5, the oldest patches
    should be removed to make room for the newer patch number and
    replaced with ellipses (See example). Do not remove more patch
    numbers than are necessary to adhere to the line length limit. Do
    not create an additional line to add patch numbers.

> Example:\
> ;;1.0;Package;\*\*...139,149,182,326,513,425,574,642,658,773,864,921,993,1001\*\*;Aug
> 13, 2020;Build 92

1.  The version date must be the same on all of the package namespaced
    routines.

    1.  Kernel utilities should be used to update the version date.

2.  Build n \[optional\] will be automatically added to the routines by
    KIDS transport. The build number may not be manually edited.

3.  Routines compiled from templates, cross-references, etc., by VA
    FileMan during or after package installation are exempt from the
    second line requirement.

```{=html}
<!-- -->
```
1.  If local modifications to a routine are restricted or prohibited by
    policy or directive, the third line should contain an appropriate
    notice. (e.g., \"Per VHA Directive 2004-038, this routine should not
    be modified\".) VHA Directives can be found at
    <http://vaww1.va.gov/vhapublications/publications.cfm?Pub=1>.

2.  Routine names and Labels are limited to sixteen (16) characters (not
    including the formal list for parameter passing) and may not contain
    lower case characters.

    1.  LABEL+OFFSET references will not be used except for \$TEXT
        references.

    2.  Lines referenced by \$TEXT for use other than to check for the
        existence of a routine or a line label in that routine must be
        in the following format: \[LABEL-optional\]\<ls\>;;text or M
        code.

3.  The line body must contain at least 1 printable character, must not
    exceed 245 characters in length, and must contain only the ASCII
    characters values 32-126. Line labels, global variable names, system
    variables, SSVNs, etc. must be uppercase.

4.  Package routine names of the following forms will not be used:

    1.  NAMESPACE_I\* (with the exceptions of Kernel, VA FileMan, and
        routines created to support the INIT process).

    2.  NAMESPACE_NTE\* (with the exception of the package integrity
        routines).

    3.  NAMESPACE_Z\*

5.  The maximum routine size, as determined by executing
    \^%ZOSF(\"SIZE\"), is 20,000 characters. 15,000 of the allowed
    20,000 characters may be non-comment source lines (including ";;"
    comment lines). 5,000 characters are reserved for non-";;" comments.

6.  Vendor specific subroutines may not be called directly except by
    Kernel, Mailman, and VA FileMan.

7.  All applications will use documented TaskMan utilities to interface
    with TaskMan.

8.  Naked references must either be appropriately preceded by the full
    reference defining it or be documented.

    1.  An appropriate preceding full reference is one that is on the
        same physical routine line as the naked reference and has no
        code between it and the naked reference that branches in any
        manner to other lines of code or executables.

    2.  Naked references requiring documentation must be documented
        within the routine in the immediate vicinity of the naked
        reference. Naked references that are preceded by a full
        reference which is outside of the routine where the naked
        reference is used must have documentation in both the routine
        containing the full reference and the routine containing the
        naked reference. This documentation must be in the immediate
        vicinity of the appropriate reference.

    3.  Uses of naked references in called utilities are exempt, e.g., S
        DIC=200,DIC(0)=\"AEQ\",DIC(\"S\")=\"I
        \$L(\$P(\$G(\^(1)),\"\^\",9))\" D \^DIC is a legitimate use of
        the naked reference.

9.  \% Routines

    1.  No application will distribute % routines. (Exemptions: Kernel,
        and VA FileMan)

    2.  No % routines shall execute variables which could be set by a
        programmer prior to executing the code.

    3.  No routine may use VIEW commands using variables as arguments
        which could be set by a programmer prior to executing the code.
        (Exemption: Kernel)

10. Z Routines

    1.  No application will export routines whose names start with the
        letter \"Z\". (Exemption: Kernel)

11. Routines may not be invoked using the extended reference syntax,
    i.e., D \^\|VAH\|TAG\^ROUTINE is illegal.

12. References to components (routines, files, etc.) in another
    application's namespace must be approved and documented in the
    Integration Control Registration listing of Forum. Integration
    Control Registration entries used by the routine must be documented
    after the 2nd line, and any other mandated entries. Each Integration
    Control Registration is defined as Private, Controlled Subscription,
    or Supported. Documentation of references that are defined as
    "Supported" is optional. The format for these entries
    is:\<ls\>;\<space\>Reference\<space\>to\<space\>\[Routine/File
    referenced\]\<space\>in\<space\>ICR\<space\>#\[ID from ICR
    registration\]

> example: ; Reference to LINE1\^ROU in ICR #99999
>
> ; Reference to LINE2\^ROU in ICR #99999
>
> or alternately, multiple reference to the same ICR may be combined on
> a single line.
>
> example: ; Reference to LINE1\^ROU,LINE2\^ROU in ICR #99999

13. Exemptions to the SAC used by the routine must be documented after
    the 2nd line, and any other mandated entries. The format for these
    entries is:

> \<ls\>;SAC EXEMPTION \[ID from Exemption
> Spreadsheet\]\<space\>:\<space\>\[short description of exemption\]
>
> example: ; SAC EXEMPTION 19901031-01 : Package-wide variable use

14. The inclusion of an IP address in a routine is prohibited. The use
    of IP addresses is discouraged in favor of the Fully Qualified
    Domain Name. In the event an IP Address must be used, an entry in
    the Parameters file (#8989.5), or an entry in a file in the
    custodial package namespace, must be used to hold a numeric IP
    address.

```{=html}
<!-- -->
```
1.  **Variables**[]{#_Toc10635710 .anchor}

    1.  Local Variables

        1.  Local variable names may not exceed sixteen characters.
            Namespaced variables must be all uppercase characters.  All
            other local variables can be mixed case. Any variable
            containing lowercase characters must be NEWed at the
            beginning of the routine, subroutine or DoDot.

        2.  The full evaluated length of a local variable name including
            subscripts must not exceed 200 characters. The evaluated
            length is calculated as follows.

            -   Example subscripted variable: NAME(sub1,sub2,\...,subn)

            -   (e.g. (\$L(NAME)+3) + (\$L(sub1) + \$L(sub2) + \...
                > +\$L(subn) ) + (2 \* number of subscripts) +15)

            -   VAR(\"XXX\",123,1,2,0) would evaluate to a string length
                > of 42, (6+11+10+15)=42.

        3.  System-Wide Variables

            1.  The following are system-wide variables. Any application
                > setting system wide variables must conform to the
                > following definitions.

                -   AGE - Patient age in years from date of birth to DT
                    > expressed as an integer, or, if deceased, the date
                    > of death.

                -   DFN - Internal number of an entry in the PATIENT
                    > File (#2).

                -   DOB - Patient date of birth expressed in internal VA
                    > FileMan format.

                -   SEX - Patient sex; either \"F\" or \"M\".

                -   SSN - Social Security Number with 9 contiguous
                    > digits, or 9 digits and a \"P\".

                -   VA(\"BID\") - Brief patient identifier up to 7
                    > characters.

                -   VA(\"PID\") - Patient identifier; up to 15
                    > characters.

            2.  The following variables, referenced elsewhere in this
                > document, are set by Kernel during sign-on, or by VA
                > FileMan, and can be assumed to exist by all VistA
                > applications.

                -   DILOCKTM -- VA FileMan Lock Time-out value.

                -   DT - Current date, without time, in internal VA
                    > FileMan format.

                -   DTIME - Time-out parameter for a read command in
                    > seconds.

                -   DUZ array - Contains user-specific information.

                -   DUZ(0) is this user\'s VA FileMan access code.

                -   DUZ(2) is the internal entry of the institution
                    > file.

                -   DUZ(\"AG\") is the agency code (from the Kernel site
                    > param file).

                -   DUZ("AUTO") is used by Menu Manager to control
                    > whether all items on a menu are presented
                    > automatically.

                -   U - Caret (i.e., \"\^\").

                -   IO - The hardware name of the last selected
                    > in/output device.

                -   IO(0) - The assigned principal device (primary
                    > device).

                -   ION - The logical name of the IO device.

                -   IOST - The last selected input/output device\'s
                    > subtype from the Terminal Type file.

                -   IOST(0) - The internal entry number in the Terminal
                    > Type file of the last selected IO device\'s
                    > terminal type.

                -   IOM - The width of the IO device.

                -   IOSL - The length of the IO device.

                -   IOF - The code to start output at the top of a page
                    > (e.g., W \@IOF).

                -   IOBS - The backspace of the IO device.

        4.  VistA packages are not allowed to KILL, NEW, SET, MERGE,
            READ (into) or otherwise modify the variable DUZ or any DUZ
            array element. (Exemptions: Kernel, and VA FileMan)

        5.  The variables DT, DTIME, and U have no array elements and
            shall be initially defined by Kernel or VA FileMan.

            1.  The variable U will not be KILLed or NEWed or changed
                > from the value defined by Kernel or VA FileMan. (It is
                > legal to SET U=\"\^\".)

            2.  The variable DT will not be KILLed or NEWed. If changed
                > it must be set using the supported reference S
                > DT=\$\$DT\^XLFDT.

            3.  The variable DTIME may be changed, but must be restored
                > to its original value before exiting the option.

                1.  The Kernel supported reference \$\$DTIME\^XUP will
                    > reset DTIME to its original value, e.g., S
                    > DTIME=\$\$DTIME\^XUP(DUZ).

        6.  VistA packages are not allowed to KILL, NEW, SET, MERGE,
            READ (into) or otherwise modify variables beginning with
            "IO" and any of their array elements except those documented
            as modifiable in the Kernel System and Developer documents
            in the VA Software Document Library. (Exemptions: Kernel,
            Mailman, and VA FileMan)

        7.  VistA packages are not allowed to KILL, NEW, SET, MERGE,
            READ (into) or otherwise modify variables beginning with
            "%". Exceptions to this are the single character variable
            \"%\" and the variables set for and/or returned by Kernel,
            and VA FileMan supported references. (Exemptions: Kernel, VA
            FileMan and MailMan)

        8.  A VistA package may declare local variables in its namespace
            as package-wide. A VistA package may not kill or change
            another VistA package\'s package-wide variables.

            1.  The variables and all of their array elements must be
                > described in the package\'s technical manual.

            2.  Documentation on how to create and kill package-wide
                > variables created by an option that is removed from
                > its exported menu path must be included in the
                > technical manual.

        9.  All supported references must leave the lock tables and
            local symbol tables unchanged upon exit with the exception
            of the following:

            -   Documented input and output variables (including
                > globals).

            -   Documented side effects, such as lock table changes, and
                > changes to files.

            -   Variables within the namespace of the supported
                > reference being called may be changed or killed during
                > execution of the supported reference. (For example,
                > the VA FileMan \^DIC call kills the variable DIE (DIE
                > is within the DI namespace of the \^DIC supported
                > reference), which may exist in the symbol table prior
                > to the call.)

            -   Variables composed of a single alpha character followed
                > optionally by one numeric.

            -   The variable %.

> These supported references must be documented in the package technical
> manual and on FORUM with a descriptive list of ALL input and resulting
> output variables.

10. Naming requirements for variables passed between packages.

    1.  Input variables in an Actual List passed by reference between
        > packages must be package namespaced.

        -   Legal: D BLD\^DIALOG(3500010,,.IBDATA,\"IBX\")

        -   Illegal: D BLD\^DIALOG(3500010,,.Y,\"IBX\")

    2.  Variables containing values which will be updated must be
        > namespaced.

        -   Legal: S DA=10,DR=\".01;.104\",DIC=\"\^DPT(\",DIQ=\"IBX\" D
            > EN\^DIQ1

        -   Illegal: S DA=10,DR=\".01;.104\",DIC=\"\^DPT(\",DIQ=\"Y\" D
            > EN\^DIQ1

```{=html}
<!-- -->
```
2.  Global Variables

    1.  Lowercase characters in global names and global subscripts are
        prohibited. (Exemption: Cross-references created using field
        values containing lowercase characters and subscripts used in
        the \^TMP and \^XTMP globals.)

    2.  The full evaluated length of a global reference must not exceed
        200 characters. The evaluated length is calculated as follows.

        -   Example subscripted variable:

> \^NAME(sub1,sub2,\...,subn)
>
> (e.g (\$L(NAME)+3) +(\$L(sub1) + \$L(sub2) + \... +\$L(subn)) + (2 \*
> number of subscripts ) +15)
>
> \^TMP(\"XXX\",123,1,2,0) would evaluate to a string length of 42
> (6+11+10+15)=42.

3.  The KILLing of unsubscripted globals is prohibited and should be
    protected. (Special instruction to the site will be required to
    enable the killing of a unsubscripted global. Application developers
    must document when calls to EN\^DIU2 are made to delete files stored
    in unsubscripted globals).

4.  READing, KILLing, SETting or MERGing \^% globals is prohibited.
    (Exemption: Kernel)

5.  All globals must be VA FileMan compatible. \^TMP, \^XTMP and
    \^UTILITY have a standing exemption from this requirement.

    1.  The global \^TMP will be used as a scratch global within a
        > session. The first subscript shall be \$J, or the first two
        > subscripts shall be a package namespaced subscript followed by
        > \$J. This global subscript should be killed before and after
        > use.

    2.  The global \^XTMP will be translated, with one copy for the
        > entire VistA production system at each site. The structure of
        > each top node shall follow the format \^XTMP(namespaced-
        > subscript,0)=purge date\^create date\^optional descriptive
        > information, and both dates will be in VA FileMan internal
        > date format.

6.  Fields in VA FileMan files which contain executable code must be
    write protected in the DD with \"@\" (e.g.,
    \^DD(file,field,9)=\"@\"), or be defined as VA FileMan data type of
    M language.

7.  References to the DD Global require a formal Database Integration
    Agreement (DBIA) with the VA FileMan Development team and must be
    registered with the Database Administrator.

8.  All global variables executed by % routines must be in
    write-protected globals.

9.  Extended reference syntax may not be used to reference global
    variables, i.e., S X=\^\|VAH\|GLOBAL(1,1) is illegal.

```{=html}
<!-- -->
```
3.  Intrinsic (system) Variables

    1.  The use of lowercase intrinsic variables is prohibited.

    2.  No VistA package may use the following intrinsic (system)
        variables unless they are accessed using Kernel or VA FileMan
        supported references: \$D\[EVICE\], \$I\[O\], \$K\[EY\],
        \$P\[RINCIPAL\], \$ROLES, \$ST\[ACK\], \$SY\[STEM\], \$Z\*.
        (Exemptions: Kernel, and VA FileMan)

        1.  \$D\[EVICE\] may check for a binary status, ie 0 or 1.

        2.  \$K\[EY\] May not rely on vendor specific values.

4.  Structured System Variables (SSVNs)

    1.  The following Structured System Variables may be used only by
        Kernel, or VA FileMan or through their supported references:
        \^\$CHARACTER, \^\$DEVICE, \^\$DISPLAY, \^\$EVENT, \^\$GLOBAL,
        \^\$JOB, \^\$LOCK, \^\$ROUTINE, \^\$SYSTEM, \^\$Z\*, and
        \^\$WINDOW.

5.  Non-VistA Globals

    1.  Read, Write, and Delete access are not allowed for system
        globals not in a VistA maintained namespace. Read and Write
        access are still allowed for \^TMP, \^UTILITY, and \^XTMP.
        (Exemptions: Kernel, and VA FileMan). The system globals
        include, but are not limited to:

        1.  \^%MV\*, \^% GLOBALS IN LOWER CASE NAMESPACES, \^%gCache\*,
            \^Cache\*, \^odd\*, \^r\*, \^ROUTINE,\^%SYS, \^%RS

```{=html}
<!-- -->
```
2.  **Commands**[]{#_Toc10635711 .anchor}

    1.  BREAK Command

        1.  Direct use of the BREAK command is prohibited. Use
            \^%ZOSF(\"BRK\") and \^%ZOSF(\"NBRK\"). (Exemptions: Kernel
            and VA FileMan)[]{#Close .anchor}

    2.  CLOSE Command

        1.  Direct use of the CLOSE command is prohibited. Use the
            supported \^%ZIS\* namespaced routines. (Exemptions: Kernel,
            Mailman and VA FileMan)

    3.  HALT Command

        1.  Direct use of the HALT command is prohibited. Use the
            supported reference H\^XUS. (Exemptions: Kernel, and VA
            FileMan)

    4.  JOB Command

        1.  Direct use of the JOB command is prohibited. Use the Kernel
            Task Manager\'s supported calls to create jobs. (Exemptions:
            Kernel, and MailMan)

    5.  KILL Command

        1.  The argumentless form of the KILL command is prohibited.
            (Exemption: Kernel)

        2.  The exclusive form of the KILL command is prohibited.
            (Exemptions: Kernel, and VA FileMan)

    6.  LOCK Command

        1.  All LOCKs shall be of the incremental form. (Exemption:
            Kernel)

            -   All incremental LOCKS must have a timeout, the timeout
                > must not be less than the value of the Kernel variable
                > "DILOCKTM".

    7.  NEW Command

        1.  The argumentless form of the NEW command is prohibited.

        2.  The exclusive form of the NEW command is prohibited.
            []{#Open .anchor}

    8.  OPEN Command

        1.  The use of the OPEN command is prohibited. (Exemptions:
            Kernel, Mailman and VA FileMan)

    9.  READ Command

        1.  All READ commands shall read into local variables, \^TMP or
            \^XTMP.

        2.  All user input READs must have a timeout. If the duration of
            the timeout is not specified by the variable DTIME and the
            duration exceeds 300 seconds, documentation in the package
            technical manual is required.

        3.  All user input READ commands shall be terminated by a
            carriage return. (Exemptions: Kernel, and VA FileMan)
            (Developers desiring to implement escape processing
            \[function keys, arrow keys, etc.\] must use Kernel supplied
            supported references \[XGF\].)

    10. Transaction Processing Commands

        1.  VistA packages may use transaction-processing commands as
            long as the operations have no irreversible side effects.

    11. USE Command

        1.  The use of the USE command with parameters is prohibited.
            (Exemptions: Kernel, and VA FileMan)

    12. VIEW Command

        1.  The use of the VIEW command is prohibited. (Exemptions:
            Kernel, and VA FileMan)

    13. MWAPI Commands

        1.  No VistA package may use the MWAPI commands: ESTART, ESTOP,
            ETRIGGER. (Exemption: Kernel)

    14. Commands

        1.  The use of Z\* commands is prohibited. (Exemptions: Kernel,
            and VA FileMan)

3.  **Functions**[]{#_Toc10635712 .anchor}

    1.  Intrinsic Functions

        1.  Use of the \$NEXT function is prohibited.

        2.  The use of the \$VIEW function is prohibited. (Exemptions:
            Kernel, and VA FileMan)

        3.  The use of \$Z\* functions are prohibited. (Exemptions:
            Kernel, and VA FileMan)

        4.  The use of the (non-standard) \$INCREMENT function is
            prohibited. (Exemption: Kernel)

        5.  The use of two parameter \$Query (non-standard) is allowed.
            \$Query(Reference,Direction) The optional direction
            parameter can be 1 for forward or -1 for reverse. Example:
            \$Query(\^ABC(1,2,3),-1)

    2.  Extrinsic Functions

        1.  Supported references that use parameters will document the
            elements of the formal list internally within the routine
            and in the package technical or programmer manual.
            Documentation will specify which elements of the formal list
            are required and which are optional, if any, and those
            elements which must be passed by reference.

        2.  Supported extrinsic special variables - extrinsic functions
            with an empty formal list - will be documented within the
            routine and in the technical or programmer manual.

4.  **Name Requirements**[]{#_Toc10635713 .anchor}

    1.  Unless otherwise approved by the IAC, routine, global, security
        key, option, template, bulletin, function, screen, help frame,
        protocol, form, block, list templates, objects, dialogues,
        remote procedures, and Kernel parameters, etc,. names must be
        consistent with the assigned namespace.

    2.  The following do not have to be namespaced: Mail Groups, File
        Names, Menu Text,

5.  **Options (Option file entries)**[]{#_Toc10635714 .anchor}

    1.  Option selection must be made through Menu Manager. Hardcoded
        menu management systems are not allowed.

    2.  All options in a package must be path independent once the steps
        described in the technical manual for creating and killing
        package-wide variables have been taken.

    3.  The following must not exist after exiting an option:

        -   Any documented output variables created by a called
            supported reference.

        -   Any documented locks created by a called supported
            reference.

        -   Any documented temporary scratch global nodes (e.g., \^TMP
            and \^UTILITY) created by a called supported reference, with
            the exception of \^XTMP global data.

        -   Any local variables, locks, and scratch global nodes (except
            \^XTMP, or other scratch globals designed to be passed
            between parts of a package) created by the application.

6.  **Device Handling**[]{#_Toc10635715 .anchor}

    1.  All device manipulation will be made through the use of the
        Kernel supported references. See Sections
        [[2.4.2]{.underline}](#Close) and [[2.4.8]{.underline}](#Open)
        for specific information about the [CLOSE]{.underline} and
        [[OPEN]{.underline}](#Open) commands. (Exemptions: Kernel and VA
        FileMan)

    2.  Any output to a hard copy device (e.g., printer) must allow for
        queuing.

    3.  Output directed to a hard copy device (e.g., printer) will not
        start with a form feed or line feeds with the purpose of
        creating a form feed, and will leave the device at top-of-form
        when the output is finished.

7.  **Miscellaneous**[]{#_Toc10635716 .anchor}

    1.  Application software must use documented Kernel supported
        references to perform all platform specific functions.
        (Exemptions: Kernel and VA FileMan)

    2.  No data element which may be interpreted as a number may contain
        more than 15 significant digits.

    3.  Packages may phase out supported references (as callable from
        outside the application and documented by IAC) by providing a
        minimum 18-month notice to the PROGRAMMER, CHIEF PROJECT
        MANAGER, and SITEMANAGERS NATIONAL mail groups on FORUM.

    4.  Globals and routines will use only the M character set profile.

    5.  It is required that applications function properly in a
        multidivisional environment. The SAC does not specify what this
        means or how multidivisional environment beyond the high level
        requirement that applications must function correctly in an
        environment supporting multiple divisions.

8.  **Conventions**[]{#_Toc10635717 .anchor}

    1.  Only Kernel and VA FileMan and existing Supported References may
        use \^UTILITY.

    2.  Tasks should be deleted from Task Manager\'s list by SETting the
        variable ZTREQ equal to \"@\" just prior to the application
        QUITing.

    3.  Adding, editing, deleting, and formatting data

        1.  VA FileMan developer tools should be used for adding,
            editing, and deleting data.

        2.  Date and time formatting should be done through Kernel or
            FileMan utilities.

        3.  Killing entries in a global within another VISTA
            application's namespace and number range must be done
            through \^DIK and requires an approved ICR with the other
            application.

        4.  The use of //// (four slash input) with FileMan may only be
            done when updating fields in files within the Application's
            assigned namespace and number range. The use of four slashes
            should only be used when data has previously been validated
            to pass the input transform of the field.

        5.  Direct global sets or kills may only be used on globals
            within the application's approved namespace and number
            range. The set should only be executed when data has
            previously been validated to pass the input transform of the
            field. (Exemption: \^TMP and \^XTMP)

    4.  Routine documentation

        1.  Routine line tags referenced from outside the routine should
            include a comment describing the code's function after the
            line tag.

        2.  Any supported references or routines invoked initially from
            an option or protocol should contain comments explaining the
            functionality and all input and output variables.

    5.  The Data Dictionary may only be edited with FileMan.

    6.  READ commands should not be used in the data dictionary.

    7.  WRITE commands should not be used in data dictionaries (except
        for VA FileMan generated ID nodes). The call EN\^DDIOL should be
        used instead.

    8.  The proper method of determining if a device is a CRT is to
        check that the variable IOST starts with the string \"C-\".
        (e.g., I \$E(IOST,1,2)=\"C-\")

    9.  Descriptive information should be included on the third piece of
        the 0 node of the XTMP global, such as task description and
        creator DUZ.

    10. The line body of a routine must contain at least 1 character.
        Generally a single semicolon is used to demarcate a blank line.

    11. Error trapping - To use the new error trapping in a routine, NEW
        \$ESTACK,\$ETRAP S \$ETRAP=\"D tag\^routine\"

    12. Access to components in another package's namespace must have an
        approved Integration Control Registration. This includes
        Routines, Files, and all other package components.

```{=html}
<!-- -->
```
2.  Interface Programming Standards and Conventions[]{#_Toc10635718
    .anchor}

It is the intention of this section of the Standards and Conventions to
provide a consistent path for users as applications migrate from
scrolling mode to a screen mode (either ScreenMan, List Manager, or
screen oriented editors) to a GUI environment.

1.  **User Interface Standards for Scroll Mode and Screen
    Mode**[]{#_Toc10635719 .anchor}**.**

    1.  Deletion of a data value, if permissible, must be initiated by
        the user entering the at-sign \"@\".

    2.  All user-input READs which are in any way evaluated by the
        application must be escapable by entering a caret \"\^\", which
        takes an action other than a reread.

    3.  All prompts requesting user input must provide additional help
        when the user enters a question mark (\"?\"). Any unrecognized
        or inappropriate response must be handled properly; i.e., at a
        minimum in a manner similar to the way VA FileMan handles
        responses. Refer to the VA FileMan User\'s Manual for more
        information. Responses to READs that are in no way evaluated by
        the application are excluded from this requirement.

    4.  In scrolling mode, defaults must be so indicated with a double
        slash (\"//\") or \"replace\" indicating that \"replace/with\"
        editing is allowed. The null response (i.e., typing only the
        RETURN key) shall select the default.

    5.  The program must return to the Menu Manager with no more than
        one intervening read when a user input READ command times out if
        the argument of the read is in any way evaluated by the
        application. A timeout at the menu level must halt through
        H\^XUS

2.  **User Interface Conventions for Scroll Mode and Screen
    Mode**[]{#_Toc10635720 .anchor}**.**

    1.  Developers are encouraged to use the following terminology.
        []{#Exit .anchor}

        1.  Exit - Exit ends a function or application and removes from
            the screen all windows and pop-ups associated with that
            function or application. If information has been changed,
            the application may automatically save the information, or
            prompt the user to save or discard the information.

        2.  Quit - Like Exit, Quit ends a function or application and
            removes from the screen all windows and pop-ups associated
            with that function or application. If information has been
            changed, the application may automatically discard the
            information, or prompt the user to save or discard the
            information.

        3.  Close (or Cancel) allows users to back out of a function or
            application, one pop-up at a time, until they reach the
            highest level window. At that point, another Close request
            has the same effect as an Exit action.

        4.  When users Close a pop-up, the application can decide
            whether to discard or retain the information in that pop-up,
            depending on how the application wants to establish the
            default values the next time the pop-up is displayed. If the
            information is discarded and the pop-up is later
            redisplayed, the pop-up contains the default values set by
            the application. If the information is retained and the
            pop-up is later re-displayed, the pop-up contains the same
            values as it did when the user Closed the pop-up.

    2.  Developers are encouraged to use the following key assignments:

        1.  PF1 key (or the equivalent key that produces the \<ESC\>OP
            sequence) - May result in different actions based on the
            next key selected.

        2.  PF2 key (or the equivalent key that produces the \<ESC\>OQ
            sequence) - Context-Sensitive Help. Provides context
            sensitive help about a specific item, field, or window.

        3.  PF3 key (or the equivalent key that produces the \<ESC\>OR
            sequence) - Exit. Exit is defined in
            [[3.2.1.1]{.underline}](#Exit) above.

        4.  PF4 key (or the equivalent key that produces the \<ESC\>OS
            sequence) - Backtab. Moves the cursor to the previous entry
            field. The cursor moves from right to left, bottom to top.

        5.  F10 key - Menu Bar. Moves the cursor to the menu bar, if one
            is available, at the top of the window or pop-up currently
            in focus.

        6.  F12 key - Cancel. Cancel is defined in
            [[3.2.1.3]{.underline}](#Close) above.

        7.  Tab key - Tab. Moves the cursor to the next entry field. The
            cursor moves from left-to-right, top-to-bottom.

        8.  PF1,H key sequence - Application Help. Provides information
            about the particular segment of the application being used.

    3.  If a user is waiting for a lock which times out, then
        appropriate notification should be given to the user.

3.  **User Interface Conventions for GUI Mode**[]{#_Toc10635721
    .anchor}**.**

    1.  User Interface Conventions for GUI Mode are detailed in a
        separate document.
