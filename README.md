### How to connect to BOX and download the data in Terminal
###
#### Access your BOX account and locate the file you plan to download e.g., `myfile.fastq.gz`; click `Share` button next to the file.
#### In the pop-up window, click `Link Settings` and copy the `Direct Link`, e.g., `https://caltech.box.com/shared/static/abcdefg.gz`
#### In your terminal, type the following command to download the file 
`curl -L https://caltech.box.com/shared/static/abcdefg.gz --output myfile.fastq.gz`
