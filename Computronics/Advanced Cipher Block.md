# Component: Advanced Cipher Block

Component name: `advanced_cipher`

Callbacks:

* `createRandomKeySet([keylength:number]):userdata`  
  Creates the key generator from two random prime numbers (optionally with given key length).  
  **keylength** - Key length in bits. Range: 1 - 2048, default: 1024.  
  **Returns:** [RSAValue](#rsavalue)
* `createKeySet(num1:number, num2:number):userdata`  
  Creates the key generator from the two given prime numbers.  
  **Returns:** [RSAValue](#rsavalue)
* `encrypt(message:string, publicKey:table):string`  
  Encrypts the specified message using the specified public RSA key.
* `decrypt(message:string, privateKey:table):string`  
  Decrypts the specified message using the specified RSA key.

## RSAValue

Callbacks:

* `getKeys():table,table`  
  Returns the two generated keys, or nil if they are still being generated.
* `finished():boolean`  
  Returns whether key generation has finished.
