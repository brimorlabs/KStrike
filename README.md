![KStrike](https://github.com/brimorlabs/KStrike/blob/master/logo.png?raw=true)


# KStrike
Stand-alone parser for User Access Logging from Server 2012 and newer systems

# [BriMor Labs](https://www.brimorlabs.com)

## KStrike

This script will parse data from the User Access Logging files contained on Windows Server 2012 and newer systems, found under the path "\Windows\System32\Logfiles\SUM" (please visit the KPMG blog post at https://advisory.kpmg.us/blog/2021/digital-forensics-incident-response.html for more details). For documentation on these files, please visit the official documentation page at https://docs.microsoft.com/en-us/windows-server/administration/user-access-logging/manage-user-access-logging



### Usage 
Run the script from the command line, afer you have extracted the database files from the SUM folder. This script will work with Python 2 or Python 3. It has also been tested on the most recent SIFT workstation release

```
This script will parse on-disk User Access Logging found on Windows Server 2012
and later systems under the path "\Windows\System32\LogFiles\SUM"
The output is double pipe || delimited when re-directed to a file.

The output is a single pipe | delimited with the CSV option.
The output type is based on the file extension with invalid extensions writing to a csv file.

Example Usage:
KStrike.py Current.mdb > SYSNAME_Current.txt
KStrike.py C\Windows\System32\LogFiles\SUM\Current.mdb SYSNAME_Current.csv
KStrike.py C\Windows\System32\LogFiles\SUM\Current.mdb SYSNAME_Current.json
KStrike.py C\Windows\System32\LogFiles\SUM\Current.mdb SYSNAME_Current.xlsx
KStrike.py C\Windows\System32\LogFiles\SUM\Current.mdb SYSNAME_Current.txt
```

This script has been tested on the following systems:
- Windows
- macOS
- \*nix

REQUIREMENTS:

- libesedb (pyesedb) (https://github.com/libyal/libesedb)
- Pandas
