# Group programming project
## Idea
- csv medical data hosted on an ftp server
- query and download the files from a specific day
- create client side cli or gui that connects to the ftp server

## Validation
- batchID only once per file
- floats to 3dp ALWAYS
- header row could be damaged - bad header doesn't necessarily mean a bad file
- if files meet validation, they can be downloaded to the machine - hierarchical folder structure
### Technical details
- Malformed files (causing difficulties when importing into other applications, e.g., spreadsheets, databases, cloud-based machine learning etc.)
- Duplicated batch_ids (see Technical Information)
- Missing headers or misspelt/incorrect headers, e.g. "batch" rather than "batch_id"
- Missing columns on a row
- Invalid entries, e.g., reading values of 10 or greater
- Empty files (there are no "nil" returns)
- Incorrectly formatted filenames.


## Notes
- check headers against template array
- if headers are wrong, replace with template - headers must be right before passing on the files