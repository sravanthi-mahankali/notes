---
layout: blog
title:  "Fundamental Practices"
permalink: /:title
categories: "appsec"
---

-> Same Origin Policy  
-> Input validations
-> using secure communication
-> Sensitive data need to be encrypted
   Classify data processed, stored, or transmitted by an application.
   
   Identify which data is sensitive according to privacy laws, regulatory requirements, or business needs.•Apply controls as per the classification.
   
   Don’t store sensitive data unnecessarily.Discard it as soon as possible or use PCI DSS complianttokenization or even truncation. Data that is not retained cannot be stolen.
   
   Make sure to encrypt all sensitive data at rest.•Ensure up-to-date and strong standard algorithms, protocols, and keys are in place; use proper key management.
   
   Encrypt all data in transit with secure protocols such as TLS with perfect forward secrecy (PFS) ciphers, cipher prioritization by the server, and secure parameters. Enforce encryption using directives like HTTP Strict Transport Security (HSTS).
   
   Disablecaching for responses that contain sensitive data.
   
   Store passwords using strong adaptive and salted hashing functions with a work factor

### SQl injection
   executing the sql queries using the input fields int he ui

### Command Lne execution 
    - read write files, emails, native operations
    - should sanitise the inputs

cast Objects in to proper types before interactng with the data bases .....

### CSRF

### Cross-Site-scripting (XSS)
  can use java script to reduce the reputation
  can use to steal the user cookies - which ca pertimt session hacking

### SSl vs TLS
   
 SSl is the older version and TSL is a newer version 

    hw it works ---  Hand shake 
```
    client Hello ---------------->
    <---------------------- server Hello
    key exchange <---------------- server
    client key exchage ------------->
```

