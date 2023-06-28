# OSCP Exam Report generator

Generate OSCP report with just one command.
Based on https://github.com/noraj/OSCP-Exam-Report-Template-Markdown

## Installation

https://github.com/noraj/OSCP-Exam-Report-Template-Markdown#requirements

Install packages on Ubuntu

```sh
sudo apt install texlive-latex-recommended texlive-fonts-extra texlive-latex-extra pandoc p7zip-full -y
```

Add the Eisvogel Latex Template found here https://github.com/Wandmalfarbe/pandoc-latex-template#installation

```sh
mkdir -p $HOME/.local/share/pandoc/templates/ && \
wget -O $HOME/.local/share/pandoc/templates/eisvogel.tex https://raw.githubusercontent.com/Wandmalfarbe/pandoc-latex-template/master/eisvogel.tex
```

# Usage

Make a copy of the OSCP-Exam-Report-Template.md file and edit it accordingly, then run the following command

```
$ ./generate_report OSCP-Exam-Report.md

Enter your OSID: OS-12345678
Enter your email: platy@email.com

Scanning the drive:
1 file, 244921 bytes (240 KiB)

Creating archive: OSCP-OS-12345678-Exam-Report.7z

Items to compress: 1

Files read from disk: 1
Archive size: 242782 bytes (238 KiB)
Everything is Ok

$ ls
OSCP-Exam-Report-Template.md        OSCP-OS-12345678-Exam-Report.pdf
OSCP-Exam-Report.md                 README.md
OSCP-OS-12345678-Exam-Report.7z     generate_report
```
