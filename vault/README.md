# Information regarding Vault/Secret management and their primary usage
Here I'll store some basic knowledge regarding Vault/Secrets management for reuse in for example talks/show and tell. 

## Information gathered from Vault (Hashicorp) presentations:
See https://developer.hashicorp.com/vault/tutorials/getting-started/getting-started-intro for more information. 

Nya infon, med flera infallsvinklar: https://developer.hashicorp.com/vault/tutorials/get-started/why-use-vault 

```
What are secrets: 
 - AuthN AuthT
 - Username/pwd
 - DB creds
 - API tokens
 - TLS certs 
 - ....

 ```
 These are sprawled out, and often handled bad inside:
 ```
 - Source 
 - Config
 - VCS
 - Filesystems
```
So, to handle secrets, introducing Vault/Secrets managers as it is:
```
Centralized
Encrypted at rest/in transition
ACL controlled  
Audit logged. 
Encryption key 
~~~~~ 
Dynamic secret
 Vault ->:
    * APP
        - ephermal 
        - unique
        - revoke


-----------------------
Encryption as a service!
 - Named  key  CC,SSN, 
 - High Level API
    - Encrypt, Sign, Verify
 - HMAC (CC , << MESSAGE>>)
 - Key lifecycle

```

