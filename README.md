### How to connect to BOX and download the data from Linux Terminal
###
#### Access your BOX account and locate the file you plan to download e.g., `myfile.fastq.gz`; click `Share` button next to the file.
#### In the pop-up window, click `Link Settings` and copy the `Direct Link`, e.g., `https://caltech.box.com/shared/static/abcdefg.gz`
#### In your terminal, type the following command to download the file 
`curl -L https://caltech.box.com/shared/static/abcdefg.gz --output myfile.fastq.gz`
###
###
###
### How to connect to BOX and upload the data from Linux Terminal (note: remember to create a unique password to use external applications in your Caltech Box account)
###
`[fgao@dator:/home/fgao]$lftp`<br/>
`lftp :~> set ftps:initial-prot ""`<br/>
`lftp :~> set ftp:ssl-force true`<br/>
`lftp :~> set ftp:ssl-protect-data true`<br/>
`lftp :~> open ftps://ftp.box.com:990`<br/>
`lftp ftp.box.com:~> user fgao@caltech.edu`<br/>
`Password:`<br/>
`lftp fgao@caltech.edu@ftp.box.com:~> mirror -R local_directory`<br/>
