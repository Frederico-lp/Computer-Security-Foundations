# Trabalho realizado na Semana #11
# LOGBOOK 11

## Indíce
- Task 1
  
- Task 2
  
- Task 3

- Task 4

- Task 5

- Task 6

pass = fred
country = PT
state name = Porto
city = Porto
organization = FEUP
unit name - LEIC 
common name - FSI
email = name@gmail.com

# Task 1

- Question 1 : What part of the certificate indicates this is a CA’s certificate?
- Question 2 : What part of the certificate indicates this is a self-signed certificate?
- Question 3 : In the RSA algorithm, we have a public exponent e, a private exponent d, a modulus n, and two secret numbers p and q, such that n = pq. Please identify the values for these elements in your certificate and key files.

- Answer 1 : The _Signatures_ part indicates that the certificate was issued by a trusted CA.
- Answer 2 : A certificate is self-signed because the subject and issuer match.
- Answer 3 : The values on our certificate are the following: 
    - e = 65537 (0x10001)
    - d = 00:8f:73:8c:9a:42:65:8e:a0:9e:26:a9:50:3c:f9: ... :98:aa:0a:f5:ca:ae:72:fd:0c:e4:4c:fc:62:cd:51
    - n = 00:cf:24:7e:8f:82:ea:44:6b:9a:49:4d:0d:ec:21: ... :70:a2:f4:8a:e7:ad:c2:54:47:d0:bb:da:76:27:7b
    - p = 00:f1:01:ef:25:e0:81:59:c9:d9:f8:d1:2c:64:b0: ... :4d:c3:ee:a5:28:eb:18:7f:57:b6:f8:ea:84:82:07
    - q = 00:dc:07:41:d8:9d:d5:e9:23:86:3e:e1:2c:2e:d7: ... :a0:78:69:bf:21:dc:dc:1a:51:19:32:b7:8a:41:ed

    - Note: The numbers on _Answer 3_ are too big to display as a whole, so we displayed the first file, followed by ellipsis and finally the second line.

# Task 2

- The alternate names we gave was: 32A, 32B.

# Task 3

- Final Output: 
    [01/14/22]seed@VM:~/.../Labsetup$ openssl x509 -in server.crt -text -noout
    Certificate:
        Data:
            Version: 3 (0x2)
            Serial Number: 4096 (0x1000)
            Signature Algorithm: sha256WithRSAEncryption
            Issuer: C = PT, ST = Porto, L = Porto, O = FEUP, OU = LEIC, CN = FSI, emailAddress = name@gmail.com
            Validity
                Not Before: Jan 14 10:06:04 2022 GMT
                Not After : Jan 12 10:06:04 2032 GMT
            Subject: C = US, O = Bank32 Inc., CN = www.bank32.com
            Subject Public Key Info:
                Public Key Algorithm: rsaEncryption
                    RSA Public-Key: (2048 bit)
                    Modulus:
                        00:c9:8b:38:7e:fd:27:b8:de:7d:69:62:33:1d:29:
                        a2:bb:f4:5a:b4:3e:f7:86:c8:16:26:83:b1:bf:b6:
                        c8:75:56:92:38:dd:26:69:48:31:30:b2:55:1e:a4:
                        75:20:3b:21:4d:9a:18:e4:b5:7a:bd:c0:d9:b4:70:
                        ed:bb:59:4b:7c:bd:a8:8e:60:74:36:83:11:57:0f:
                        37:5c:de:c3:2b:4a:c7:76:ef:10:37:cf:81:46:10:
                        e3:f5:53:b5:8b:e4:fd:79:26:f3:70:4a:8a:32:5a:
                        5c:52:7c:50:2b:a1:82:42:de:00:8f:ef:f8:75:bb:
                        fa:4b:74:30:cc:f8:56:db:5e:49:3b:42:51:96:43:
                        bf:e9:d6:67:10:be:69:08:03:a3:f7:f0:6f:a7:d6:
                        64:26:93:29:20:38:1d:2f:3b:8e:c7:4d:11:5c:73:
                        2b:1a:53:ca:1a:9f:13:bc:ff:ae:86:b0:99:2f:cb:
                        1f:52:f2:00:6a:83:46:d9:5a:8f:8b:9b:1b:d7:bf:
                        e1:7d:89:41:dc:bf:19:71:b5:69:15:a8:f1:64:8e:
                        22:a1:e4:39:72:f9:ff:79:61:8f:dd:3c:dc:8d:7f:
                        bb:78:b6:aa:67:35:6f:ef:72:6d:b6:1d:e1:fb:22:
                        c3:d7:1f:a6:74:da:8d:b8:d0:de:63:86:c9:52:92:
                        68:8d
                    Exponent: 65537 (0x10001)
            X509v3 extensions:
                X509v3 Basic Constraints: 
                    CA:FALSE
                Netscape Comment: 
                    OpenSSL Generated Certificate
                X509v3 Subject Key Identifier: 
                    40:F9:24:8A:04:02:00:3C:0B:D8:CA:C6:78:C3:56:F6:12:3F:AB:88
                X509v3 Authority Key Identifier: 
                    keyid:2C:D5:7E:45:BB:13:76:9B:17:38:4D:7A:3F:3D:6F:A7:91:B7:9D:21

        Signature Algorithm: sha256WithRSAEncryption
            7e:b7:28:7a:a7:3f:6b:9a:00:47:75:e4:30:c0:53:c7:c2:34:
            d7:d2:44:b1:93:5e:e2:7c:59:a4:23:74:da:22:ca:e3:44:74:
            b0:37:93:95:de:e0:68:1e:a8:e4:28:2e:4d:73:50:02:a0:1f:
            3e:7b:1f:bd:73:89:5f:4a:1c:61:e9:0d:df:ae:81:0f:a9:45:
            07:2d:d6:52:76:bb:fa:93:a2:79:58:e6:d1:f6:3b:61:b4:07:
            30:9d:ee:b6:36:6c:76:cc:94:a9:ea:d6:45:e3:eb:35:ae:24:
            30:55:e8:c0:c4:41:a1:ed:5e:f1:03:71:16:1c:11:9e:de:e2:
            b3:9f:c8:9f:94:8c:84:c9:e4:01:ee:9b:0b:ac:b2:02:b2:85:
            ed:40:3d:3d:8f:6b:fc:d9:08:ec:9a:d4:fe:9e:06:11:e9:98:
            36:7a:94:b0:ab:d1:3d:1c:57:c6:97:83:1a:a5:1f:36:6c:d2:
            c8:fa:8d:a7:58:27:d3:3a:bb:4f:c2:63:19:ce:48:76:96:a9:
            f9:08:54:05:93:7b:4f:e6:a4:2c:d7:4a:28:74:97:5d:68:32:
            9e:29:8e:cc:eb:9f:cc:16:6b:62:80:ff:d0:29:19:e1:a8:e7:
            72:77:9e:63:0f:7d:fc:92:12:87:4b:1d:ca:da:8e:d2:45:a6:
            3d:6d:cb:24:54:e0:38:85:55:18:c7:67:87:c9:f4:95:cb:ef:
            3e:9e:9a:43:5e:74:14:d3:27:9d:54:e1:28:d4:93:8f:1a:1d:
            d3:21:69:fb:7b:71:98:6a:45:31:13:fc:93:4c:51:72:81:91:
            c3:e3:5d:1b:ec:f1:5d:22:81:5e:0d:01:a0:43:7c:f4:e6:16:
            4a:93:03:6e:1c:bb:ec:b6:e2:98:e2:74:73:f5:f8:79:6f:1e:
            cf:38:a9:ce:4f:31:19:8b:1b:eb:b1:0a:69:d8:50:62:41:09:
            03:21:22:fb:7c:21:97:d2:d9:91:fb:f6:72:56:d6:74:a7:c8:
            3e:b2:d0:74:e8:ac:dd:1f:be:e1:e0:0c:69:ed:80:af:55:f0:
            61:9a:54:5b:f2:a4:dc:84:4e:b8:ed:89:a5:f8:5a:70:26:5d:
            74:d1:bc:f3:82:87:30:15:7e:a8:b0:8c:03:f2:bf:a8:75:e3:
            70:2b:db:5f:a6:9f:7b:40:87:79:ee:45:fc:82:b9:6b:7a:72:
            ce:be:04:a7:2c:b1:d4:02:a0:17:5e:92:0e:ee:8b:fa:a0:4d:
            1f:d9:68:a6:f8:76:5b:fc:53:55:b0:d0:9d:07:80:02:2c:4a:
            05:26:0a:d8:46:6d:9f:58:cd:64:43:32:37:2c:9d:a9:99:4c:
            5a:4a:1b:f5:d7:da:e5:8e

# Task 4
We first started by building the docker container with _docker build_ and then make it available by running _docker-compose up_.

We then created a new shell for the container where we started our Apache server with _service apache2 start_.

Our next step was to visit bank32 website, that appeared odd since the certificate wasn't yet recognized by the browser, despite already being loaded.

![warning](/outputs/log11/warning.png)

After loading our certificate (modelCA.crt), we got the following:

![bank32](/outputs/log11/bank32.png)

# Task 5

We used the previous configurations of _Task 4_ except for the _/etc/hosts_ file on the victim's machine to redirect the site we used as target (in our case, www.facebook.com) to our server. 

When we visited the site as a victim, the screen was similar to the warning we got on the previous Task, because the certificate didn't match with Facebook's URL.

# Task 6

We created a new certificate with a new DNS, and then switched certificates with the one indicated in the configuration file moved it to the directory _/certs_ and changed the file name.

We then changed the DNS on the victim's machine and changed the configuration file _ServerName_ parameter located in _/etc/apache2/sites-available_ to, in our case, Facebook (www.facebook.com).

Finally, when we write the site URL, it will redirect to our webserver since the victim's computer was configured to redirect to it.

![facebook](/outputs/log11/facebook.png)

