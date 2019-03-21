checksum
========

Validates MD5/SHA1/SHA256/SHA512 CheckSums on the command line. 

```

checksum - File CheckSum Validator - https://github.com/ferventcoder/checksum
                    forked version - https://github.com/jftuga/checksum
License: Apache v2

checksum checks a file and returns a check sum for md5, sha1, sha256 and sha512.

To use checksum you would simply provide a file path and it will return the sum for the file.
  Example: checksum -f="a\relative\path"
  Example: checksum -f="a\relative\path"
  Example: checksum "a\relative\path" -t=sha256

You can also check against an existing signature.
To validate against an existing signature (hash) you would simply provide
 the file and the expected signature. When checking a signature, if the 
 signature is valid it exits with 0, otherwise it exits with a non-zero exit code.
  Example: checksum -f="c:\\path\to\somefile.exe" -c="thehash"
  Example: checksum "c:\\path\to\somefile.exe" -c="thehash" -t=sha256

 == Synopsis == 
  checksum [-t=sha1|sha256|sha512|md5] [-c=signature] [-f=]filepath

== Options ==
  -?, --help, -h             Prints out the options.
  -f, --file=VALUE           REQUIRED: file - The is the name of the file. 
                               The file should exist. You do not need to 
                               specify -f or -file in front of this argument.
  -t, --type, --hashtype=VALUE
                             Optional: hashtype - 'md5', 'sha1', 'sha256' or 
                               'sha512'. Defaults to 'sha256' or is determined 
                               by length of passed check value.
  -c, --check=VALUE          Optional: check - the signature you want to 
                               check. Not case sensitive.
```
