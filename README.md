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
   and yes the build generate the executable

2. its different because it depend of the time when it was build

3. No because its not build time reproducible, the build depend of the time when its built

4. yes because its run time reproducible. Once its built the time is fixed during and the output when running multiples times is the same

5. the output can be different because of the different architecture

6. Not a good idea because of 5.

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

2. The image from Listing 7 is bigger because it contains the compiler and the build tools.  
The image from Listing 8 is smaller because the build tools are not in the final image.

3. The container image is much bigger than the binary.  
This is because the image also contains the Alpine system and some libraries.

4. The instruction copies the compiled binary from the build stage to the runtime stage.  
It is a good idea because the final image stays small and does not contain the build tools.

5. It is difficult to obtain the exact same image ID.  
Some things like timestamps, metadata or different base image versions can change the result.

6. Yes, we get the same output because the container runs with the same environment.  
we use the same parameters so the result is the same.

7. podman save transfers the full container image with all layers and metadata.  
So the other student can run exactly the same image.

## 4.1.6 Questions

1. Yes, the resulting binary should be the same because Nix builds are deterministic.

2. Yes, the path is the same because it is generated from a hash of the inputs in the Nix store.

3. Yes, if we build multiple times we get the same result because the build is reproducible.

4. nix shell nixpkgs#hello opens a temporary shell where the hello program is available.  
nix profile add installs the program permanently in the user profile.

5. The Nix store contains all packages (including Nix itself) and their dependencies.  
It is immutable so packages cannot be modified and reproducibility is ensured.

6. nix flake lock creates or updates the flake.lock file with the exact versions of dependencies.  
This helps keeping builds reproducible.

7. The build would fail because Nix builds are sandboxed.  
The program cannot access the network or system files that are not declared.

8. Nix uses hashes and the flake.lock file to fix dependency versions.  
So even if upstream changes, the project still uses the same inputs.

9. A minimal flake.nix would define a devShell with gcc and jdk packages.  
Yes, the flake.lock file should also be shared to ensure reproducibility.

## 4.2 General questions

1. Nix is better for reproducible builds because all dependencies are defined and isolated.  
Containers mostly reproduce the runtime environment.

2. No, it is not totally safe. Containers isolate processes but they still use the host kernel.

3. No, AI outputs are not always reproducible. 
Parameters like temperature or randomness can change the result.

4. The program could be shared as a compiled binary, a container image or the source code with build instructions.

5. Yes thanks ! and thanks again for the stickers !!

6. Le TP était très intéressant, mais je l’ai trouvé assez dense. Il est presque impossible de suivre les explications tout en répondant aux questions en même temps.
   On se retrouve donc à devoir choisir entre écouter les explications et prendre du retard sur les questions, ou prendre le temps de répondre aux questions mais alors perdre le fil des explications.
   C’est un peu dommage car le sujet est vraiment intéressant et, je pense, très important.
   De plus, ce dilemme est difficile à gérer pendant 4 heures, et il est presque inévitable de décrocher à un moment.


