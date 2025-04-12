---
layout: post
title: Secure Messages
date: 2025-04-12 05:00:10
last_updated: 2025-04-12 05:00:10
description: Secure Messages
tags: security messages
categories: security
featured: false
---

## Secure Messages

Use encryption - openssl encryption (openssl enc)

### Encrypt message

```
echo "my message" | openssl enc -aes-256-cbc -a -salt -pass pass:mysecretpassword
echo "my message" | openssl enc -e -aes-256-cbc -pbkdf2 -a -salt -pass pass:mysecretpassword

```

### Decrypt message

```
echo "U2FsdGVkX1+0x5v3Z4Q6g7Q==" | openssl enc -d -aes-256-cbc -a -pass pass:mysecretpassword
echo "U2FsdGVkX1+0x5v3Z4Q6g7Q==" | openssl enc -d -aes-256-cbc -pbkdf2 -a -pass pass:mysecretpassword
```

### Secret and Secure Messages (on Youtube)

[Secure and Secret Messages YT] https://www.youtube.com/watch?v=ADpJUY19-eQ "https://www.youtube.com/watch?v=ADpJUY19-eQ"
[Secure and Secret Messages YT] Secret and Secure Messages (on Youtube)
