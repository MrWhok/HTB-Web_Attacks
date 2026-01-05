# HTB-Web_Attacks

## Table of Contents
1. [HTTP Verb Tampering](#http-verb-tampering)
    1. [Bypassing Basic Authentication](#bypassing-basic-authentication)
    2. [Bypassing Security Filters](#bypassing-security-filters)

## Tools/Useful Links

## HTTP Verb Tampering
### Bypassing Basic Authentication
#### Challenges
1. Try to use what you learned in this section to access the 'reset.php' page and delete all files. Once all files are deleted, you should get the flag.

    We can solve this by changing the request header from **GET** to **PUT**. The answer is `HTB{4lw4y5_c0v3r_4ll_v3rb5}`.

### Bypassing Security Filters
#### Challenges
1. To get the flag, try to bypass the command injection filter through HTTP Verb Tampering, while using the following filename: file; cp /flag.txt ./

    To solve this, we need to change the endpoint to `/index.php` and use **POST** as the HTTP Verb. We can click **change request method** to **POST**. Here the request looks like:

    ![alt text](<Assets/Bypassing Security Filters - 1.png>)

    The answer is `HTB{b3_v3rb_c0n51573n7}`.