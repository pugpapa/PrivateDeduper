# PrivateDeduper
When files go awry and your tech-savvy partner is not allowed to see file names or content … what is a therapist to do? 


Apparently there are some weird things happening with OneDrive sync.  At some point, the syncing "broke".  What happened was that folder names changed from "FOLDER_NAME" to "FOLDER_NAME [2|3|4|etc]".

The goal here will be to create a script to be run at a top directory level and perform the following:
1. Identify all files recursively underneath
1. Files will be duped if:
  * The file name matches another existing file name, can have at most 1 characte difference
  * The file path matches the same directory structure (save for 1 character on the trailing folder)
  * File size must match
  * File modify time must match

