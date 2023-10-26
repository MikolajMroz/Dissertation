# Dissertation
Developing File Extraction Methods for Open-Source Forensics Software in C#

## Acknowledgements
Firstly, a huge thank you to the Abertay course organisers, module leaders, and my supervisors Dr. Ethan Bayne and Ian Ferguson for equipping me with the knowledge I needed to tackle my learning and giving me opportunities and experience I could only dream of in preparation for making my way up in the world.  
I would like to sincerely thank my amazing friends, my ever-supporting family, and my beautiful girlfriend Himali for helping me through all the rough times over the course of my studies, keeping my spirits high.

## Abstract
### Context

OpenForensics is an open-source file carving tool originally made to demonstrate the benefits of using advanced GPU pattern-matching techniques to perform file carving in a digital forensics investigation. Its primary aim was to showcase a quantifiable improvement in processing times for reading in and analysing digital forensic data when compared to other CPU-restricted tools commonly used today. 

It successfully achieved this aim, albeit with a simplistic approach to file carving; the files it ‘carves out’ from disk images are done so using a basic ‘file header-footer’ carving algorithm, only taking into account one unique identifier at the beginning (the header) and one at the end (the footer). This implementation causes a number of problems with certain file structures such as .ZIPs, which use multiple nested headers and footers to contain their data, and as a result, are misidentified by the program and output as several broken files instead.

### Aim
This paper aimed to demonstrate the methodology behind refactoring OpenForensics’ file detection and validation algorithms to improve the program’s reliability in processing realistic forensic datasets and accurately reproducing a vast variety of different filetypes from a given disk image. These improvements were implemented into locally stored source code and its accuracy was compared to the original pre-refactor release of OpenForensics, as well as a group of currently available file-carving tools to determine a measurable impact on speed and accuracy, just as was originally done in the initial of the program.

### Results
Results showed that the introduction of a semantic file-detection algorithm, a success rate of 100% was achieved in the extraction of ZIP files during testing. Processing times for file searching and carving were also improved, taking up to 20% less time for the program to finish its file analysis phase. The paper concludes by saying that semantic file detection algorithms can greatly improve the detection rate of forensic evidence from a given target and urges further development in the field of digital forensics, particularly with regards to standardisation.
