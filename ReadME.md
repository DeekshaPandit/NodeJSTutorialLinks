* NodeJS project Architecture: 
  https://dev.to/santypk4/bulletproof-node-js-project-architecture-4epf
  
* Twelve Factor App: 
  https://12factor.net/
  
* https://dev.to/embiem/auto-generate-sitemapxml-in-nextjs-2nh1
* Closure:
  https://www.quora.com/What-exactly-is-a-closure-in-JavaScript
  
* Regular and Arrow functions difference:
  https://www.geeksforgeeks.org/difference-between-regular-functions-and-arrow-functions/
  
* Uncaught Exception:
  https://shapeshed.com/uncaught-exceptions-in-node/

* You really dont know Node
https://github.com/azat-co/you-dont-know-node

* clustering in nodejs (use of cores)
https://medium.com/tech-tajawal/clustering-in-nodejs-utilizing-multiple-processor-cores-75d78aeb0f4f

* How to speed up node app:
https://www.sitepoint.com/how-to-create-a-node-js-cluster-for-speeding-up-your-apps/

* frquently asked questions in nodejs:
https://medium.com/@vigowebs/frequently-asked-node-js-interview-questions-and-answers-b74fa1f20678

* nodejs stream:
https://flaviocopes.com/nodejs-streams/

* nodejs child processes:
https://www.freecodecamp.org/news/node-js-child-processes-everything-you-need-to-know-e69498fe970a/

* Nodejs Practical crypto:
 Protect Password:
  1) Rainbow tables make easy to find the password hashed by SHA256/MD5/.....
  2) Use Salt for making hashed password strong (Salt= any random value)
  3) latest 
  
     PBKDF2 (Password-Based Key Derivation Function 2) - saves use from brute force attack.
     ARGON2
     SCRYPT
     BCRYPT
aes-256-cbc(advance encryption standard, 256 bits, cypher block chaining)

 Protect Data in REST:
   By Applying Symmetric Encryption/Decryption mechanism
    
   e.g. secure SSN.
   
   const crypto =  require("crypto");
   const algorithm = "aes-256-cbc';
   let ssn="222-222-4444";
   let password = "PassW0rd!" // should be a good key
   const salt = crypto.randomBytes(32);
   const key = crypto.scryptSync(password, salt,32);
   const iv = crypto.randomBytes(16);
   const cipher = crypto.createCipheriv(algorithm, key,iv);
   let encrypted = cipher.update(ssn, 'utf8', 'hex');
   encrypted += cipher.final('hex');
   console.log(encrypted);
   const decipher = crypto.createDecipheriv(algorithm,key, iv);
   let decrypted = decipher.update(encrypted, 'hex','utf8');
   
    for securing the keys:
    use Azure KeyVault or AWS Key Management system.
  
   Protect Data in Transit:
   
   
   
   
   Two Factor Authentication:
   
   
   
   
   
   
   
   
   
 
 
 
