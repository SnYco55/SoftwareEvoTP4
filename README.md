# SoftwareEvoTP4
## 2.2.1 Questions

1.
2.
3. No because its not build time reproducible
4. yes becuase its run time reproducible
5. the output can be different because of the different archite
6. Not a good idea because of 5.

## 2.3.1 Questions

1.
2. yes it always gives the same output, because its randomness reproducible


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



