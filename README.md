# Goldman-Sachs-Engineering-Virtual-Program
<!--PROJECT -->
<h3 align="center">Goldman Sachs Engineering Virtual Program</h3>
 <p align="center">
    This repo contains my attempt file for the Goldman Sachs Engineering Virtual Program and a certificate of completion.
    <br />
    <a href="https://github.com/BishalBudhathoki/Goldman-Sachs-Engineering-Virtual-Program/blob/main/Goldman%20Sachs_completion_certificate.pdf"><strong>Check the certificate »</strong></a>
    <br />
    <br />
    <a href="https://github.com/BishalBudhathoki/Goldman-Sachs-Engineering-Virtual-Program/blob/main/Goldman-Sachs.docx">View the submitted file</a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#cracked-password">Cracked Passwords</a></li>
      </ul>
    </li>
    <li>
      <b>Questions: </b>
      <ul>
        <li><a href="#Q1">What type of hashing algorithm was used to protect passwords?</a></li>
        <li><a href="#Q2">What type of hashing algorithm was used to protect passwords?</a></li>
        <li><a href="#Q3">What controls could be implemented to make cracking much harder for the hacker in the event of a password database leaking again?</a></li>
        <li><a href="#Q4">What can you tell about the organization’s password policy (e.g. password length, key space, etc.)?</a></li>
       <li><a href="#Q4">What would you change in the password policy to make breaking the passwords harder?</a></li>
      </ul>
    </li>
    <li><a href="#email">Email/Memo explaining your findings in relation to controls used by the organization and your proposed uplifts.</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This project/program is about Crack leaked password database where we need to crack the password from the given <a href="https://github.com/BishalBudhathoki/Goldman-Sachs-Engineering-Virtual-Program/blob/main/passwd_dump.txt">  password dump file </a> that contains the username and there hashed password, finding out the hashing algorithm used for authentication, level of protection the current hashing algorithm provides, preventive measures, what the password dump file tells about it and preventive measures that the organization can take to minimize the password database attack and make authentication strong along with an email/memo for the organization and references used.

### Cracked-password

From the given <a href="https://github.com/BishalBudhathoki/Goldman-Sachs-Engineering-Virtual-Program/blob/main/passwd_dump.txt">password dump file</a> these are the passwords that has been cracked using online tools like
* https://crackstation.net/
* https://www.dcode.fr/md5-hash

a.	experthead:e10adc3949ba59abbe56e057f20f883e -           <b>123456</b> <br />
b.	interestec:25f9e794323b453885f5181f1b624d0b -	   <b>123456789</b> <br />
c.	ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 -	   <b>qwerty</b> <br />
d.	reallychel:5f4dcc3b5aa765d61d8327deb882cf99 - 	  <b> password</b> <br />
e.	simmson56:96e79218965eb72c92a549dd5a330112 -	   <b>111111</b> <br />
f.	bookma:25d55ad283aa400af464c76d713c07ad -	  <b> 12345678</b> <br />
g.	popularkiya7:e99a18c428cb38d5f260853678922e03 - <b>	   abc123</b> <br />
h.	eatingcake1994:fcea920f7412b5da7be0cf42b8c93759 -  <b> 1234567</b> <br />
i.	heroanhart:7c6a180b36896a0a8c02787eeafb0e4c -	   <b>password1</b> <br />
j.	edi_tesla89:6c569aabbf7775ef8fc570e228c16b98 -	   <b>password!</b> <br />
k.	liveltekah:3f230640b78d7e71ac5514e57935eb69 -	   <b>qazxsw</b> <br />
l.	blikimore:917eb5e9d6d6bca820922a0c6f7cc28b -	   <b>Pa$$word1</b> <br />
m.	johnwick007:f6a0cb102c62879d397b12b62c092c06 -	   <b>bluered</b> <br />
n.	flamesbria2001:9b3b269ad0a208090309f091b3aba9db -  <b>Flamesbria2001</b> <br />
o.	oranolio:16ced47d3fc931483e24933665cded6d -	   <b>Oranolio1994</b> <br />
p.	spuffyffet:1f5c5683982d7c3814d4d9e6d749b21e -	   <b>Spuffyffet12</b> <br />
q.	moodie:8d763385e0476ae208f21bc63956f748 -		   <b>moodie00</b> <br />
r.	nabox:defebde7b6ab6f24d5824682a16c3ae4 - 		   <b>nAbox!1</b> <br />
s.	bandalls:bdda5f03128bcbdfa78d8934529048cf - 	   <b>Bandalls </b> <br />

<!-- Q1 -->
## Q1
1.	Hashing algorithm used: MD5.

<!-- Q2 -->
## Q2
2.	Level of protections offered to the passwords:
After going through the provided password dump file and decrypting them, it has been found that all those hash values are the result of using MD5 algorithm to decrypt the password and following is what I found on my own research about MD5.

MD5 creates 512-bit blocks that contains 16 words of 32-bit each resulting in 128-bit message. Protection is provided in different stages. <br />
a.	Message digest value is initialized using hexadecimal numerical values.<br />
b.	In every individual stage, four message digest is passed through those changes the current data block along with the values passed from the previous block.<br />
c.	The value obtained from the final block is then MD5 digest for current block.<br />
d.	No two-password ca have same hash value.<br />
So, this must be practically not decryptable. But this is not always the case like in Flame malware in 2012. If anyone got the hash value from any password database leakage, then it can be decrypted in few seconds or a minute.<br />

<!-- Q3 -->
## Q3
3.	To make cracking much harder for the hacker in the event of a password database leaking again we can do:<br />
a.	We can use hashing with salt to slow down the password cracking from the obtained rainbow table. No methods to prevent password cracking is safe but this is a lot of work.<br />
b.	We are using MD5 algorithm. We can do better. We can use algorithms like bcrypt – specify complexity that affects the speed at which hashing and guessing occurs, scrypt – prevents parallel cracking.<br />
c.	Above two takes lot of resources to authenticate one user and for that we can use Server-relief that uses browser or user’s system for the required resources.<br />
d.	Required length of the password can be set to least 16 that increases the cracking time.<br />
e.	No username and password similarity and not even similarity with the brand.<br />
f.	Advising users not to use dictionary word instead use letters characters, numbers all jumbled.<br />
g.	Promote use of password generator tool that generates and saves the password.<br />

<!-- Q4 -->
## Q4
4.	Upon inspecting and cracking password from the given dump file this is what I have:<br />
a.	The least password length is 6 and maximum is 14.<br />
b.	All the passwords are mostly letter and numbers and only 3 got characters.<br />
c.	Only passwords are hashed using MD5 algorithm. <br />
d.	No password is hashed + salted.<br />
e.	Company accepts any type of password like all number, all letter, all character that are easily crack able.<br />

<!-- Q5 -->
## Q5
5.	There are some preventive measures that the organization can use to make password cracking harder.<br />
a.	Using more secure hashing algorithm like SHA, bcrypt, scrypt instead of MD5.<br />
b.	Length of password be at least 16.<br />
c.	No dictionary password acceptable.<br />
d.	Password should contain capital letter, number, symbols, and non-dictionary.<br />
e.	All the password encryption to be done using salt and hash.<br />
f.	Even suggest passwords with own password generator tool.<br />

<!-- EMAIL -->
## Email
Dear Ma’am/Sir,
After obtaining the leaked hashes I tried to crack the password, which was not even hard, I have found some vulnerabilities in the password policy of the organization. The purpose of this email is to present you my findings on the organization’s current password policy and my recommendation to prevent cracking of the password and increase the time involved in cracking it.<br />
All the passwords cracked shows that the organization is using the MD5 algorithm for the security of user data authentication. This is an outdated and easily compromise able hashing algorithm. <br />
There are even online tools that can crack the obtained hashed file like https://crackstation.net/ and https://www.dcode.fr/md5-hash . We can enter the hash from the obtained passwd_dump.txt file into the provided text field and upon selecting decrypt button, respective passwords are generated in fraction of second. <br />
From the cracked password, <br />
•	minimum length of the password is found to be 6.<br />
•	no password requirements, hence, any kind of password is accepted.<br />
•	All passwords are hashed with MD5 algorithm.<br />
•	No password is salted along with hash.<br />
From above findings, here are some of my recommendations to strengthen the authentication and prevent the password cracking for the better password policy:<br />
•	Not accepting dictionary password, no username, date of birth, organization name in the password.<br />
•	Length of the password to be at least 16 that contains minimum 1 capital letter, small letter, number, and symbols.<br />
•	Providing strong password generator for the users with the option to set their own password.<br />
•	Suggesting user to use password generator/manager tools.<br />
•	Using better algorithm for encrypting password like bcrypt, scrypt, SHA (Secured Hashed Algorithm).<br />
•	Using Salt along with the hash.<br />
These are my findings and recommendations. Hope this helps the organization to strengthen the authentication of user and prevent password cracking in the future.<br />
Thank you,<br />
Regards,<br />
Bishal Budhathoki,<br />
Master of Information Technology<br />

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
https://crackstation.net/ <br />
https://en.wikipedia.org/wiki/Hash_function_security_summary  <br />
https://searchsecurity.techtarget.com/definition/digital-signature  <br />
https://searchsecurity.techtarget.com/definition/MD5  <br />
https://www.dcode.fr/md5-hash  <br />
https://onlinetoolweb.com/md5-salt-decrypt-online-tool/  <br />
https://www.wordfence.com/learn/how-passwords-work-and-cracking-passwords/  <br />
