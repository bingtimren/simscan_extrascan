simscan_extrascan
=================

A patch to allow simscan for qmail to conduct extra scan defined by shell command in an environment variable

The motivation for creating this project is increase of spam / malicious emails that contain a zip attachment
which in turn contain an executable. I studied spamassassin / spamdyke / qmail-spp but none seem to allow such 
inspection to block "executable in zip". Finally, I decide to patch simscan to allow it execute certain command
passed it through an environment variable. If the command returns non-zero, simscan drops the email.


