# Detailed Writeup: 


## Challenge 1: Path treversal
### Approach:
- Went to the gallery page in network tab and found the command /getFile?file=Path_of_file
- Used it redirect to `/home/kaptaan/PClub-DVWA/routes.txt` where the flag was present.

### Screenshots:

<img src="./Screenshots/Screenshot from 2024-05-23 22-58-36.png" alt="Alt Text">
<img src="./Screenshots/Screenshot from 2024-05-23 22-58-53.png" alt="Alt Text" >

### Flag:
pclub{path_trav3rsa1_1s_fun}

## Challenge 2: Command Injection
### Approach:
- Used the /ipDetails to go to the page and found the command injection vulnerability as the hint suggested.
- Used the command `1|ifconfig eth0` to find the mac-address of the host.
### Screenshots:

<img src="./Screenshots/Screenshot from 2024-05-23 23-01-41.png" alt="Alt Text">
<img src="./Screenshots/Screenshot from 2024-05-23 23-02-59.png" alt="Alt Text" >

### Flag:
pclub{60:45:bd:af:3f:e5}

## Challenge 3: SQL Injection
### Approach:
- Was unable to find the flag but the approach was to use the SQL injection to bypass the login page and get the flag.
- Found out that the blogs in `/getBlogDetail?blog='&part=link` was vulnerable to SQL injection, tested it using `blog='` and it gave an error.
- Found out there were 4 columns in the table using `blog=' order by 4#`.

### Screenshots:

<img src="./Screenshots/Screenshot from 2024-05-23 23-05-33.png" alt="Alt Text">
<img src="./Screenshots/Screenshot from 2024-05-23 23-10-06.png" alt="Alt Text" >
