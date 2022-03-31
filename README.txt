                           hashlib
                          20060408a
           Python secure hash and message digest module
           MD5, SHA1, SHA224, SHA256, SHA384 and SHA512
        (backported from Python 2.5 for use on 2.3 and 2.4)

BUILDING

  python setup.py build [options]

  Valid options:
    --openssl-prefix=path, --openssl-incdir=path, --openssl-libdir=path

  If OpenSSL 0.9.7 or later is found it will be used.  Version
  0.9.8 is preferred as it provides many more optimized algorithms.
  OpenSSL is not required.

INSTALLING

  python setup.py install

USAGE

  Use the following hash object constructors:

    md5, sha1, sha224, sha256, sha384, and sha512

  Hash objects have update, copy, digest, and hexdigest methods.

    >>> x = hashlib.sha224('spam')
    >>> x.hexdigest()
    'e047c44d875407fdb49d53d8b2326fc3e20e27f08434fef1275a3981'
    >>> y = x.copy()
    >>> y.update(' and eggs')
    >>> y.hexdigest()
    '1c54f569f9b5c7cec6a34465de51df10b0048f3d48f7051ac6eb2e54'
