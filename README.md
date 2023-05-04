Download Link: https://assignmentchef.com/product/solved-cs642-hw1-password-cracking
<br>
<h1>Part A: Password Cracking</h1>

<ol>

 <li>Recover the password used to generate the challenge hash above. Hint: The password is an ASCII string consisting only of numeric digits.</li>

 <li>Give a pseudocode description of your algorithm and the worst-case running time for it.</li>

 <li>Discuss the merits of your colleague’s proposal and suggest how your attack might be made intractable (harder).</li>

 <li>Put your solutions in the file txt .</li>

</ol>

<h1>Part B: Encryption</h1>

python3 baddecrypt.py testkeyfile $CT

Your job is to assess the security of this encryption scheme. Your solution will be a Python program attack.py that takes as input a ciphertext and modifies the ciphertext so that the decrypted message has a different (and more lucrative to the recipient) AMOUNT field and still passes the verification in baddecrypt.py . The file attack.py must do this without access to the key file or knowledge of the key. You can assume the ciphertext contains the sample message hardcoded in badencrypt.py .

We will test your solution with original versions of badencrypt.py and baddecrypt.py and with different encryption keys than the test key provided. To ensure that attack.py produces the correct formatted output, you can run from the command line:

CT=$(python3 badencrypt.py testkeyfile)   MODCT=$(python3 attack.py $CT)   python3 baddecrypt.py testkeyfile $MODCT

<ol>

 <li>Complete the attack program py (feel free to make modifications to the pre-filled content. The skeleton is provided just to help you out)</li>

 <li>In txt , describe what is wrong with your colleague’s scheme and how it should be fixed so that it will be more secure.</li>

</ol>

(Your attack script will not have direct access to the key file and should not attempt to gain access to the process memory of baddecrypt or any other files to steal the key directly.)

Extra credit: More password cracking

Yet another colleague, to make the password cracking hard, uses hash iteration: SHA256 is iterated 256 times. Something like the following code:

The password is representative of real-world passwords: something complex enough that the person that selected this password would consider using it for a website login, but easy enough to be memorable.

Find the password used to produce the challenge hash. Give a pseudocode description of your algorithm and the correct password in solutions.txt .

<h2>Hints</h2>

The website has a password policy that requires that the password must have at least 6 characters and atleast three of the four character classes: uppercase letters ( A-Z ), lower case letters ( a-z ), symbols

( ~`<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="3c1d7c">[email protected]</a>#$%^&amp;*()+=_-{}[]|:;”’?/&lt;&gt;,. ), and digits ( 0-9 ).

<a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">You can look at </a><strong><u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">CrackStation’s password crackin</a></u></strong><strong><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">g</a><u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm"> dictionaries</a></u></strong> <strong><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">(</a><u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">https://crackstation.net/crackstationwordlist-password-crackin</a></u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">g</a><u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">-dictionar</a></u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">y</a><u><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm">.htm) </a></u></strong><a href="https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm"> for some help.</a>

It is wise to estimate the running time of your solution before starting it.