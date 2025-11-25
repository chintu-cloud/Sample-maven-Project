
# Sample Maven Project

This is a simple Java project built using **Apache Maven**. It demonstrates the Maven build lifecycle, unit testing, and packaging into a JAR file.

---

## 🚀 Maven Goals

1. `mvn clean`  
   Cleans previous build files and removes the `target` directory.

2. `mvn compile`  
   Compiles source code into bytecode (`.class` files).

3. `mvn test`  
   Runs unit tests to validate functionality.

4. `mvn package`  
   Packages the compiled code into a distributable format (`jar`, `war`, or `ear`).

5. `mvn install`  
   Installs the package into the local Maven repository (`~/.m2/repository`).

---

## ⚠️ Important Notes

- Before running `mvn package`, execute:
  ```bash
  mvn clean
  mvn compile
  mvn test
  ```

- Before running `mvn test`, execute:
  ```bash
  mvn clean
  mvn compile
  ```

---

## ☁️ Launching on AWS EC2

1. **Launch EC2 Instance**
   - Name: `maven-java-project`
   - Instance type: `t3.micro`
   - Networking: default
   - Security group: default
   - Keypair: not required

2. **Connect to EC2 and Setup**
   ```bash
   sudo su -
   yum install maven -y        # Installs Maven and Java automatically
   mvn --version
   yum install git -y
   git clone https://github.com/chintu-cloud/Sample-maven-Project.git
   cd Sample-maven-Project
   yum install tree -y
   tree
   ```

---

## 📂 Project Structure

```
Sample-maven-Project
├── README.md
├── pom.xml
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── mycompany
    │               └── app
    │                   └── App.java
    └── test
        └── java
            └── com
                └── mycompany
                    └── app
                        └── AppTest.java
```

---

## 🧪 Build & Test Workflow

```bash
mvn clean
mvn compile
mvn test
mvn package
```

- After `mvn package`, the JAR file will be created in the `target/` directory:
  ```
  target/my-app-1.0-SNAPSHOT.jar
  ```
  
Sample-maven-Project

   cd target/classes/com/mycompany/app/
   
                ls
                
                vi App.class 


```
 ---- App.class inside ----

Êþº¾^@^@^@7^@'
^@^B^@^C^G^@^D^L^@^E^@^F^A^@^Pjava/lang/Object^A^@^F<init>^A^@^C()V     ^@^H^@  ^G^@
^L^@^K^@^L^A^@^Pjava/lang/System^A^@^Cout^A^@^ULjava/io/PrintStream;^G^@^N^A^@^Ucom/mycompany/app/App^H^@^P^A^@^LHello World!
^@^R^@^S^G^@^T^L^@^U^@^V^A^@^Sjava/io/PrintStream^A^@^Gprintln^A^@^U(Ljava/lang/String;)V^A^@^GMESSAGE^A^@^RLjava/lang/String;^A^@^MConstantValue^A^@^DCode^A^@^OLineNumberTable^A^@^RLocalVariableTable^A^@^Dthis^A^@^WLcom/mycompany/app/App;^A^@^Dmain^A^@^V([Ljava/lang/String;)V^A^@^Dargs^A^@^S[Ljava/lang/String;^A^@
getMessage^A^@^T()Ljava/lang/String;^A^@
SourceFile^A^@^HApp.java^@!^@^M^@^B^@^@^@^A^@^Z^@^W^@^X^@^A^@^Y^@^@^@^B^@^O^@^C^@^A^@^E^@^F^@^A^@^Z^@^@^@/^@^A^@^A^@^@^@^E*·^@^A±^@^@^@^B^@^[^@^@^@^F^@^A^@^@^@
^@^\^@^@^@^L^@^A^@^@^@^E^@^]^@^^^@^@^@  ^@^_^@ ^@^A^@^Z^@^@^@7^@^B^@^A^@^@^@    ²^@^G^R^O¶^@^Q±^@^@^@^B^@^[^@^@^@
^@^B^@^@^@^M^@^H^@^N^@^\^@^@^@^L^@^A^@^@^@      ^@!^@"^@^@^@^A^@#^@$^@^A^@^Z^@^@^@-^@^A^@^A^@^@^@^C^R^O°^@^@^@^B^@^[^@^@^@^F^@^A^@^@^@^Q^@^\^@^@^@^L^@^A^@^@^@^C^@^]^@^^^@^@^@^A^@%^@^@^@^B^@&
```

              

                cd ../../../../..
                
                ls
                
                cd 
                
                mvn package                 # jar file created 
                  
                        output:
                        [INFO] BUILD SUCCESS
                        [INFO] Total time:  4.617 s
                        [INFO] Finished at: 2025-11-25T09:18:58Z


                tree
```
.
├── README.md
├── pom.xml
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── mycompany
│   │               └── app
│   │                   └── App.java
│   └── test
│       └── java
│           └── com
│               └── mycompany
│                   └── app
│                       └── AppTest.java
└── target
    ├── classes
    │   └── com
    │       └── mycompany
    │           └── app
    │               └── App.class
    ├── generated-sources
    │   └── annotations
    ├── generated-test-sources
    │   └── test-annotations
    ├── maven-archiver
    │   └── pom.properties
    ├── maven-status
    │   └── maven-compiler-plugin
    │       ├── compile
    │       │   └── default-compile
    │       │       ├── createdFiles.lst
    │       │       └── inputFiles.lst
    │       └── testCompile
    │           └── default-testCompile
    │               ├── createdFiles.lst
    │               └── inputFiles.lst
    ├── my-app-1.0-SNAPSHOT.jar
    ├── surefire-reports
    │   ├── TEST-com.mycompany.app.AppTest.xml
    │   └── com.mycompany.app.AppTest.txt
    └── test-classes
        └── com
            └── mycompany
                └── app
                    └── AppTest.class

```

---

## ✅ Example Output

- **Compile Success**
  ```
  [INFO] BUILD SUCCESS
  ```

- **Test Success**
  ```
  [INFO] BUILD SUCCESS
  ```

- **Package Success**
  ```
  [INFO] BUILD SUCCESS
  ```

---

** mvn clean command run **
 mvn clean 

                    output:
                        [INFO] BUILD SUCCESS
                        [INFO] Total time:  0.363 s
                        [INFO] Finished at: 2025-11-25T09:37:34Z

              tree 

  ```
.
├── README.md
├── pom.xml
└── src
    ├── main
    │   └── java
    │       └── com
    │           └── mycompany
    │               └── app
    │                   └── App.java
    └── test
        └── java
            └── com
                └── mycompany
                    └── app
                        └── AppTest.java

11 directories, 4 files                         # previous all files deleted    
    ```               


## 🎯 Summary

This project is a minimal Maven-based Java application that prints **Hello World!** and includes a unit test. It demonstrates the Maven lifecycle (`clean → compile → test → package → install`) and can be deployed easily on AWS EC2.

