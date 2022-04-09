# Maven and JDK setup
Notes on how to set up maven and the openJDK on a new windows 10 system.

## Guidelines
1. Download the JDK binary.
2. Extract it to the desired installation location.
3. Create the JAVA_HOME environment variable on windows. It should point to the installation root, eg `C:\Software\openjdk-11`.
4. Add `%JAVA_HOME%\bin` to the `Path` environment variable.
5. Open up a command prompt and check the installation by typing `java -version`
6. Download and extract the maven binary to the desired location.
7. Create the MAVEN_HOME environment variable on windows. It should point to the installation root, eg `C:\Software\apache-maven-3.6.3`.
8. Add `%MAVEN_HOME%\bin` to the `Path` environment variable.

#### Sources:
##### Guide for Setting up the open JDK
https://knowledge.exlibrisgroup.com/Aleph/Knowledge_Articles/How_to_Download_and_Install_OpenJDK_11_on_Windows_10_PC_for_Aleph
##### Open JDK download source
https://jdk.java.net/java-se-ri/11

##### Maven install guide
https://maven.apache.org/install.html

# Setting up SSH for git on a new PC
## 1. Generate SSH key
Run in bash: `ssh-keygen -f $KEY_FILE_PATH -t ed25519 -C $GITHUB_EMAIL`
This generates 2 files, one having no extension (private key) and one having a `.pub` extension (public key). 
## 2. Make sure the ssh agent is running
Run in bash: ```eval `ssh-agent -s` ```
## 3. Add the private part of the generated key
Run in bash: ``` ssh-add $KEY_FILE_PATH ```


