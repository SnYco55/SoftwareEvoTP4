# SoftwareEvoTP4
## 1.2.4 Questions
1. its almost impossible, which make SHA-256 a reliable cryptographic hash function for now.
2. "aac" and "ada" are two different strings that give the same checksum so its a collision.
3. It is not recommended because tools like TAR or Gzip include variable metadata (timestamps, file order,...), which changes the resulting hash even if the file content remains identical.

## 2.2.1 Questions

1. size :
    | text | data | bss | dec | hex | filename |
    |------|------|-----|-----|-----|----------|
    | 1065 | 532  | 4   | 1601| 641 | hello-world |
   
   permissions : -rwxr-xr-x
   yes the build generate the executable

3. its different because it depend of the time when it was build
4. No because its not build time reproducible, the build depend of the time when its built
5. yes because its run time reproducible. Once its built the time is fixed during and the output when running multiples times is the same
6. the output can be different because of the different architecture
7. Not a good idea because of 5.

## 2.3.1 Questions

1. The output are the same, and its because rand() use a seed that are the same for every of us
2. yes it always gives the same output, because of the same seed, its randomness reproducible

## 2.4.1 Questions

1. yes because its build time reproducible shasum give the same value for 2 different compilation
2. no because this time, the randomness generator use the time wich changes, its not run time reproducible
3. yes time make the output different

## 2.6.1 Questions

2. When the number of iterations n increases, the estimate of pi generally gets closer to the real value (≈ 3.1416). However, the execution time increases proportionally with n, which is expected for a Monte Carlo algorithm.

3. No its not reproducible at build time because shasum -a 512 montecarlo-pi of two different executable of the same source code are not the same, to correct that we need to remove all the part that use macros (__DATE__ and __TIME__)

4. No its not reproducible at run time because different executions of the same compiled source
code do not produce exactly the same output result. To make it reproducible at run time we need to remove all the code that rely on time and the print of time execution

5. the file montecarlo-pi-runRepro.c is already reproducible at run time and build time

## 3.3.1 Questions

1. we need 2 parameters as the same as before, it shows us that Docker do not change that




