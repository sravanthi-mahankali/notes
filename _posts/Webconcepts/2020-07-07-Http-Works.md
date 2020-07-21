---
layout: blog
title: "Http Works" 
permalink: /:title
categories: WebConcepts
---
```
          Browser                                  Https://youtube.com
                         give me youtube.com
            |     -------------------------------->       |
            |                                             |
            |  sends a list of SSL/TLS versions and       |
            | encryption algorithms that I can  work with |
            |    ---------------------------------->      |
            |                                             |
            |     chooses the best SSL/TLS version and    |
            |    encryption algorithm among the ones      |
            |    sent, and based on my preferences.       |
   oh I     |     reply with my certificate,              |
 Know and   |     which includes my public key,           |
  I trust   |     so they can verify who I am.            |
            |    <----------------------------------      |
            |                                             |
            |   I generate a 'pre-master key' so we can   | I use my private 
            |           both use it later when we         | key to decrypt
            |             generate a unique key.          | the pre-master key.
            |      I encrypt that pre-master key with     |  
            | server's public key and then send it to him.|      
            |                                             |
            | ------------------------------------------> |

      So far all the communication between them has been in the open.
                  They haven't secured any messages.
            |                                             |
            |                                             |
  generate  |                                             | generate 
  symmetric |                                             | Symmertic
  key with  |                                             | key with
  pre-master|                                             | pre-master
  key       |                                             | key
            |                                             |
            |      sends a test msg with encryption       |
            |      ------------------------------->       |
            |      reply saying look good can you verify  |
            |      the encrypted msg that i have send .   |

      -----------------Secure  connection established-------------------

    from now on we will communicate with msg encrypted with the symmetric key 

```

### How browser will verify the authorised CA
