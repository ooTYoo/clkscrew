## parse_mdt_certs
This script is used to parse the certificate structs stored within the .mdt file. The structs are encoded in the proprietary [HAB](http://vm1.duckdns.org/Public/Qualcomm-Secure-Boot/Qualcomm-Secure-Boot.htm) format.

### To run
```
$ python parse_mdt_certs.py widevine/widevine.mdt 
[+] Found 2 HAB cert structs
[-] Parsing struct at offset 4618
[-]   - cert_name: 	O=Motorola Inc, OU=Motorola PKI, CN=HAB CA 637
[-]   - issuer_name: 	O=Motorola Inc, OU=Motorola PKI, CN=CSF CA 637-1; SN=6323
[-]   - exp_len: 	3
[-]   - exponent: 	010001
[-]   - mod_len: 	256
[-]   - modulus: 	c61364d71c0273f47d68f2fc9ae047085bbb3d0fa3c7c155d5b37a7d59112b8bfaae8402d1615758d481b09c89e7eb6e99da5fb736538a1ab72f33e0637ad8db228eccaa7f2a45c7da548f475b0ed6e01f9fa83664f7daca3f9bf565e8447f5b56180e3f37a4a9ec988208dee45abe6694844681b1e4cdda0417ec1e2c8e4727d2aa0d1ba7fb6851176df16510eeeee54fca4d6eb0773e4866665b4974ac5defd8f6a106d8c07372b1971c3e050b50d555b7fc4dca4dc1e1e2cbf378c87fc0ee5ec895ea14d599ed8d830fd721c870ebad3fa3c7d8f4f3b02c2c7af3e056d20afc62fda614f5ed10aa1b6d705a2785a71a3dc8e7f28defe463e5a817efb6890f
[-]   - cert_sig_len: 	256
[-]   - cert_sig: 	0def2f024a9853147ddcdefa321e0d5752aed22b2d90f3474142159584d5f33f9efdee7fbe8bb9ca81d859a79aa0136f006b7c2fa52567a7530e7874023f4a14a046b36b794087bb858619512a7bc04d81d3e9a0e495365b540adcb76005c305f65f634d9295892dda96ce7d36261d9cf74dab808c8e481d75831e4e7234993a3c91617792ea9cdf22c65eaf41caa7f3c55f7ba77f028831ac244868b469e51b00bc237038ccee8b5067a367cb0c65162b4353f698f71871b7d5a0aa50ac49ba94299921c7e2a66e597b334a48af597e39c72458107127af81a015cfd4422ecd3f9663b70f678086fb93ad2785af93d16b7e85c494f39a797d0f2bd103ea413b
[-] Parsing struct at offset 5262
[-]   - cert_name: 	O=Motorola Inc, OU=Motorola PKI, CN=CSF CA 637-1
[-]   - issuer_name: 	O=Motorola Inc, OU=Motorola PKI, CN=APP 637-1-2; SN=6325
[-]   - exp_len: 	3
[-]   - exponent: 	010001
[-]   - mod_len: 	256
[-]   - modulus: 	c44dc735f6682a261a0b8545a62dd13df4c646a5ede482cef858925baa1811fa0284766b3d1d2b4d6893df4d9c045efe3e84d8c5d03631b25420f1231d8211e2322eb7eb524da6c1e8fb4c3ae4a8f5ca13d1e0591f5c64e8e711b3726215cec59ed0ebc6bb042b917d44528887915fdf764df691d183e16f31ba1ed94c84b476e74b488463e85551022021763af35a64ddf105c1530ef3fcf7e54233e5d3a4747bbb17328a63e6e3384ac25ee80054bd566855e2eb59a2fd168d3643e44851acf0d118fb03c73ebc099b4add59c39367d6c91f498d8d607af2e57cc73e3b5718435a81123f080267726a2a9c1cc94b9c6bb6817427b85d8c670f9a53a777511b
[-]   - cert_sig_len: 	256
[-]   - cert_sig: 	3cc1961f0d833a6197bd5537ee3f7d784dcf5dfb83b03bdf40d08d9da4564680ed54e0a4a30d9909795aebb3fa152fc20606f1e8b0b1abab88f812e06d45363a442ae1439840a2c7fbea32786fa99e886025151599e96962379511ffbf0c22790498c41907b220e32af0ff6d2f856dba656155f6ae1155562df6e07ffcb4ed5690e9484b307e8b5b8296fe3cb3a39d50879e891f1f1b33bb5c1c5e6fc4ef3fdab03f66ad2f1c90e11d8ff59b2425fd71950346a6e961e9a7e5368520f4d40a4f0c413b46d85dfd06e11299f875818e4fb47018c30c4cf28c6aaa05647b8b8f56c577a2fd6b2a7b902ff8374fc5977ecd35da309fa10b8832559d77ae856abc13
[+]
[+] Decrypting signatures of certs:
[-]   - cert[1].sig: 	3cc1961f0d833a6197bd5537ee3f7d784dcf5dfb83b03bdf40d08d9da4564680ed54e0a4a30d9909795aebb3fa152fc20606f1e8b0b1abab88f812e06d45363a442ae1439840a2c7fbea32786fa99e886025151599e96962379511ffbf0c22790498c41907b220e32af0ff6d2f856dba656155f6ae1155562df6e07ffcb4ed5690e9484b307e8b5b8296fe3cb3a39d50879e891f1f1b33bb5c1c5e6fc4ef3fdab03f66ad2f1c90e11d8ff59b2425fd71950346a6e961e9a7e5368520f4d40a4f0c413b46d85dfd06e11299f875818e4fb47018c30c4cf28c6aaa05647b8b8f56c577a2fd6b2a7b902ff8374fc5977ecd35da309fa10b8832559d77ae856abc13
[-]     - hash: 	33a9dc70b31f36138820348552bd6bde8268002aeadb3289d571092c9564c5fd
[-]     - offset: 	5262 - 5649
[-]   - .sig: 	5f66b195a7fd15c72d9a85fbbfc84e73a3ffda3257a87bdb2d1dd974914f5d4276c4e2c13218d8d50687e086c874a91bcb33590f08f3044b0dfba4561dd416055823b8b5164816c12c79a780828e4be18e8771206783c37b7008bf538249ad7580ef4ce84a6de5485b281f5ce9ad2350bcc483696221d0c5970daf75ca1d8050fdafc3f4915c1f8a88fa6baaf48ce1e099e3941659af032a5ee37fe9893057870810a5d41695108baf62fc55ba645935a1109ef418600add83d3e6dad88330f72ee652bbcab225fe31ee8e2aa1496b4930468304d7fb1b3a2fe1181d23e9cbe0084af377a53b71163a8a670ea64962b272c88cb1038f1d4c9634ef448049c1d0
[-]     - hash: 	d919f6c1ed13b5012f4acb01fe0ffb22b672b2536c3dfa451bc89dbff21cdf41
[-]     - offset: 	4276 - 4362

[+] Signature of .mdt file: offset 5907 - 6163
[-]   - RSA-PKCS1-v1.5 Signature
[-]   - Decrypted message digest: (len=51)
[-]   -   hashAlgo: SHA-256
[-]   -   raw: 	3031300d0609608648016503040201050004205f5ca2d7133f925dd289b9275a558de5d44a4f654883fd5e251a94ceb1cff243
[-]   -   hsh: 	5f5ca2d7133f925dd289b9275a558de5d44a4f654883fd5e251a94ceb1cff243
[+] Searching for region of file being used for hash
[-]   - offsets: 180 - 4276
```

## pycrypto
This script is used to first factorize the corrupted modulus collected from the characterization experiments, and then generate the self-signed `widevine` update blob.

This requires [SageMath](http://doc.sagemath.org/html/en/installation/) to be installed, together with its python bindings.

### To run
```
$ ~/SageMath/local/bin/python pycrypto.py
  nprime:   c44dc735f6682a261a0b8545a62dd13df4c646a5ede482cef858925baa1811fa0284766b3d1d2b4d6893df4d9c045efe3e84d8c5d03631b25420f1231d8211e2322eb7eb524da6c1e8fb4c3ae4a8f5ca13d1e0591f5c64e8e711b3726215cec59ed0ebc6bb042b917d44528887915fdf764df691d183e16f31ba1ed94c84b476e74b488463e85551022021763a3a3a64ddf105c1530ef3fcf7e54233e5d3a4747bbb17328a63e6e3384ac25ee80054bd566855e2eb59a2fd168d3643e44851acf0d118fb03c73ebc099b4add59c39367d6c91f498d8d607af2e57cc73e3b5718435a81123f080267726a2a9c1cc94b9c6bb6817427b85d8c670f9a53a777511b
  dprime:   04160eecc648a3da19abdc42af4cfb41a798e5eb8b1b49c2c29a9ed29eb10e5f73ded6ce0ca5d00344ead384c03dcf17950252a97f19da0c13621e10a6bfcde45e124dafe3b215be2866e083f12f08f25d31155279b33a265a8431cc60da7ddc843d8cb6b505f9252f96ca2aa9f0b79c01495f20a54d848bdf947cf1ef7e79653921beb9d7cbf70b9b2b0df44efb4a94a3772c2f74df5f29911aca1f56066b4dfc34ec5afedb460950eb346e99492405beadecd9131ba3b9504ae7ef739b63efbf308e608ee5e31e13cd100c191de5ab5c2dd28dee93094eef7df3f74ac84f7c08059732a50ec5b5739c5f7c31f3b886dc66fb5eedb7bc47a56d6462efa9ffa1
  new_mdt:  9e500b0f07fb300150e68216ec330151228949a90730e03895513f429e5297bf34a69c1a8fb2649adb5d564524e71aae28e2754654649990def871bfadf361aedaae2caa30a273e4c987cb77627b8617e86f61a77a21b3d9b817431c1e775ae594be78d40b41707189eb45634adc6b1491a4e436f26b031aaeb57f21f7a8a5445ec764f18699c7daccf6927a4a74f512e48040913844dc398cae6a743e2b862d6cb3d2ca306823df9a926ada9f11ac843a9ca366833ff575ef2d7e67d5fe6f442ab39215d2b62cb583b50c9dda6282473fcf6ef3d7fe0c9a12c24c0a60163776d025bfcf20e3b5aa0b02e872224515922c8bf0248f8726052cfbab74d47a0854
  new_cert: 7f4cc741805678568801e7434bb8b52a32dae347918555d8010e6bdf0b07488371332e07dacaa0aeeadc0b7dac6124355306a23031734ae74d20b74df922c9f983d5e441d4b0171c921515e325f7ec8c0fecbc9f6ca1168105deb3818c1cae473d38a6963cabbdce1e6111b48f545c012142bc5f2565afd0cca5cf9cff4cbc83a3d3638992d4687c853815bcb27c654f821ee33dd3f6350e4c48ccdf2809808133cc3673e1ea434d82ef33bac3a06dd5549d45a89e7f7a39042e01c256d071cae28e332101b5554d901d92943d730b978bdc4f34c8fd556856d6251dfcb8aba52d392c4265396808dc008737e445d8e3acc9e02b43ffde74dc4a98bf485e41c6
```