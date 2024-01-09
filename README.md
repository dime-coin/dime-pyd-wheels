# Notes About DIME-PYD-Wheels

This repo contains pyd and wheels needed for compiling Electrum-Dime binaries on Windows and Linux.



## Files
| Version & Type               |OS         |Size       |SHA256 SUM                                                       | GPG    |
|:---------------------        |:-------   |:----------|:----------                                                      |--------|
| [pivx_quark_hash 1.2.whl]()  | win x64   | 58981     |2E7D2AC923ACACB6E0467123440F3099C51901476E45B92F21863B7F15941D28 |[SIG]() |
| [pivx_quark_hash 1.2.whl]()  | win x86   | 65733     |DC2DFD5FEFDF56A715B598A2C7C830F2BDFD5D12CF8CCD0F702FD5A9D2C1BC30 |[SIG]() |
| [pivx_quark_hash 1.2.whl]()  | lin x86_64| 215721    |4665525D44034C6FC07435D7145CCF6BEE9F50D8F5EA0E2498A4878F7E5C0AB8 |[SIG]() |
| [quark_hash 1.0.whl]()       | lin x86_64| 214464    |FD5C082C7FE6F92DB98DD7FE42F9F580B91DFC9B120A13E45F48597D114092EC |[SIG]() | 
| [quark_hash 1.0.whl]()       | win x86   | 64586     |17C9F70CEB8A53208056F029BAF1100A5D21B65450FE376F18C56E69B8800041 |[SIG]() |
| [quark_hash 1.0.pyd]()       | lin x86_64| 141312    |29699A5A50B2C67B2D4C8E8819BDDE68C6FD03983C6036BE8F728A678BDABF9F |[SIG]() |


Wheels Source
--------
`pivx_quark_hash 1.2` [GitHub](https://github.com/random-zebra/pivx_quark_hash) commit#`346602f` clone repo and build with python setup.py bdist_wheel. groestl.c does need some modifications for setup.py to run on Windows.

`quark_hash 1.0` [PyPi](https://pypi.org/project/quark_hash/) sha256=eb1de478ff1acf810f50d3e227532a937252006eb124afb3da248baaa559b7d4 built with python setup.py bdist_wheel

Verification
--------
To ensure the integrity and authenticity of the files you download from this repository, follow these steps to verify them using GPG (GNU Privacy Guard).

### Steps to Verify with GPG

1. **Import the Public Key**
   - Before verifying the file's signature, you need to import @Dhop14's public GPG key that was used to sign the file.
   - Retrieve the key from a public key server using the following fingerprint:
     `A3E6 459E 3707 BC46 849A C0AA 964D A787 DBC8 3054`
   - Use this command to import the key, removing spaces from the fingerprint:
     ```bash
     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "A3E6 459E 3707 BC46 849A C0AA 964D A787 DBC8 3054"
     ```

2. **Download the File and Its Signature**
   - Download both the `.whl` file and its corresponding GPG signature file (`.asc`) from the links provided in the table above.

3. **Verify the Signature**
   - To verify the signature of the downloaded file, use the following command. Replace `yourfile.whl` and `yourfile.whl.asc` with the actual names of the downloaded files:
     ```bash
     gpg --verify yourfile.whl.asc yourfile.whl
     ```
   - If the signature is authentic and valid, GPG will confirm that the signature is good.

### Troubleshooting

- **Signature Not Trusted**: If you receive a message that the signature is not trusted, it might mean that the public key is not trusted in your GPG keyring. This does not necessarily indicate a problem with the signature as long as the key is correct and belongs to the expected signer.
- **Verification Failure**: If verification fails, it could mean the file has been tampered with or corrupted during transit. Try re-downloading the file.

For more detailed instructions on using GPG, visit the [GNU Privacy Guard documentation](https://gnupg.org/documentation/).

**Note:** Always ensure that you have the correct and trusted public key for verification. The public key can be obtained from the project maintainers or from a trusted keyserver.


