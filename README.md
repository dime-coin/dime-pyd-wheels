# Notes About DIME-PYD-Wheels

This repo contains pyd and wheels needed for compiling Electrum-Dime binaries on Windows and Linux.



## Files
| Version & Type                                                                                                                  |OS         |Size       |SHA256 SUM                                                       | GPG    |
|:---------------------                                                                                                           |:-------   |:----------|:----------                                                      |--------|
| [pivx_quark_hash 1.2.whl](https://github.com/dime-coin/dime-pyd-wheels/raw/main/pivx_quark_hash-1.2-cp311-cp311-win_amd64.whl)  | win x64   | 58981     |9cef07256ac657287f8d3b37cb1c87e389bb5ae92ad5643057480af7c9846e94 |[SIG](https://github.com/dime-coin/dime-pyd-wheels/blob/main/pivx_quark_hash-1.2-cp311-cp311-win_amd64.whl.asc) |
| [pivx_quark_hash 1.2.whl](https://github.com/dime-coin/dime-pyd-wheels/raw/main/pivx_quark_hash-1.2-cp311-cp311-win32.whl)      | win x86   | 65733     |00ba4e675d9a4e1e6c336d9d06125067ee037731d55ede4782b837a0ededa73d |[SIG](https://github.com/dime-coin/dime-pyd-wheels/blob/main/pivx_quark_hash-1.2-cp311-cp311-win32.whl.asc) |
| [pivx_quark_hash 1.2.whl](https://github.com/dime-coin/dime-pyd-wheels/raw/main/pivx_quark_hash-1.2-cp38-cp38-linux_x86_64.whl) | lin x86_64| 215721    |4665525d44034c6fc07435d7145ccf6bee9f50d8f5ea0e2498a4878f7e5c0ab8 |[SIG](https://github.com/dime-coin/dime-pyd-wheels/raw/main/pivx_quark_hash-1.2-cp38-cp38-linux_x86_64.whl.asc) |
| [quark_hash 1.0.whl](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash-1.0-cp38-cp38-linux_x86_64.whl)           | lin x86_64| 214464    |fd5c082c7fe6f92db98dd7fe42f9f580b91dfc9b120a13e45f48597d114092ec |[SIG](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash-1.0-cp38-cp38-linux_x86_64.whl.asc) | 
| [quark_hash 1.0.whl](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash-1.0-cp311-cp311-win32.whl)                | win x86   | 64586     |17c9f70ceb8a53208056f029baf1100a5d21b65450fe376f18c56e69b8800041 |[SIG](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash-1.0-cp311-cp311-win32.whl.asc) |
| [quark_hash 1.0.pyd](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash.cp311-win_amd64.pyd)                      | win x64   | 141312    |29699a5a50b2c67b2d4c8e8819bdde68c6fd03983c6036be8f728a678bdabf9f|[SIG](https://github.com/dime-coin/dime-pyd-wheels/raw/main/quark_hash.cp311-win_amd64.pyd.asc) |


Wheels Source
--------
### pivx_quark_hash 1.2 

[GitHub](https://github.com/random-zebra/pivx_quark_hash) commit#`346602f` clone repo and build with `python setup.py bdist_wheel`. *Note: groestl.c needs some modifications for setup.py to run on Windows.*

### quark_hash 1.0

[PyPi](https://pypi.org/project/quark_hash/) sha256=eb1de478ff1acf810f50d3e227532a937252006eb124afb3da248baaa559b7d4 built with `python setup.py bdist_wheel`.

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


