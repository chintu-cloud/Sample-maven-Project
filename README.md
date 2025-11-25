<img width="881" height="629" alt="Untitled Diagram drawio (5)" src="https://github.com/user-attachments/assets/938bc894-7619-478e-adda-e65c53726051" />

       
       
       # ╔═╗┌─┐┌┬┐┌─┐┬  ╔═╗
       # ╚═╗├─┘ │ │ ││  ║  
       # ╚═╝┴   ┴ └─┘┴─┘╚═╝

 # 🚀✨ Sample Maven Project ✨🚀
---
A complete, step-by-step Maven workflow guide


## 📌 Overview
This project demonstrates a simple Maven-based Java application with unit testing and packaging. It includes instructions for setting up an EC2 instance, running Maven goals, and verifying build outputs.

---

## 🚀 Maven Goals

1. `mvn clean`  
   Cleans previous project run files.

2. `mvn compile`  
   Converts source code into machine-understandable bytecode.

3. `mvn test`  
   Validates test cases using JUnit.

4. `mvn package`  
   Creates the final package (`.jar`, `.war`, `.ear`).

5. `mvn install`  
   Installs the final package into the local Maven repository.

---

## 🔑 Important Notes
1. **Before running `mvn package`:**
   ```bash
   run: (automatic)
                            mvn clean
                            mvn compile
                            mvn test
   then run:
                            mvn package
   ```

2. **Before running `mvn test`:**
   ```bash
    run: (automatic)
                            mvn clean
                            mvn compile
   then run:
                            mvn test
   ```

---

## 🖥️ Launch Server (AWS EC2)

- **Instance Name:** `maven-java-project`  
- **Instance Type:** `t3.micro`  
- **Networking:** Default  
- **Security Group:** Default  
- **Keypair:** Not required  

### Connect to EC2
```bash
sudo su -
yum install maven -y        # Installs Maven (Java auto-installed)
mvn --version
yum install git -y
git clone https://github.com/chintu-cloud/Sample-maven-Project.git
cd Sample-maven-Project
yum install tree -y
tree
```

---

## 📂 Project Structure

```text
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
```

---

## 🛠️ Maven Commands & Outputs

### Clean
```bash
mvn clean
```
Output:
```
                       [INFO] Scanning for projects...
                       [INFO] 
                       [INFO] -------------------------< alexa:project-java >-------------------------
                       [INFO] Building project-java 1.0-SNAPSHOT
                       [INFO] --------------------------------[ war ]---------------------------------
                       [INFO] 
                       [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ project-java ---
                       [INFO] ------------------------------------------------------------------------
                       [INFO] BUILD SUCCESS
                       [INFO] ------------------------------------------------------------------------
                       [INFO] Total time:  0.304 s
                       [INFO] Finished at: 2025-11-25T10:31:23Z
                       [INFO] ------------------------------------------------------------------------



```

---

### Compile
```bash
mvn compile
```
Creates `target/` folder with compiled `.class` files.

Output:
```
                       [INFO] Scanning for projects...
                       [INFO] 
                       [INFO] -------------------------< alexa:project-java >-------------------------
                       [INFO] Building project-java 1.0-SNAPSHOT
                       [INFO] --------------------------------[ war ]---------------------------------
                       [INFO] 
                       [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ project-java ---
                       [INFO] ------------------------------------------------------------------------
                       [INFO] BUILD SUCCESS
                       [INFO] ------------------------------------------------------------------------
                       [INFO] Total time:  0.304 s
                       [INFO] Finished at: 2025-11-25T10:31:23Z
                       [INFO] ------------------------------------------------------------------------



```

---

### Test
```bash
mvn test
```
Generates reports in `target/surefire-reports`.

Output:
```
                       [INFO] Scanning for projects...
                       [INFO] 
                       [INFO] -------------------------< alexa:project-java >-------------------------
                       [INFO] Building project-java 1.0-SNAPSHOT
                       [INFO] --------------------------------[ war ]---------------------------------
                       [INFO] 
                       [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ project-java ---
                       [INFO] ------------------------------------------------------------------------
                       [INFO] BUILD SUCCESS
                       [INFO] ------------------------------------------------------------------------
                       [INFO] Total time:  0.304 s
                       [INFO] Finished at: 2025-11-25T10:31:23Z
                       [INFO] ------------------------------------------------------------------------



```

---

### Package
```bash
mvn package
```
Creates JAR file:  
`target/my-app-1.0-SNAPSHOT.jar`

Output:
```
                       [INFO] Scanning for projects...
                       [INFO] 
                       [INFO] -------------------------< alexa:project-java >-------------------------
                       [INFO] Building project-java 1.0-SNAPSHOT
                       [INFO] --------------------------------[ war ]---------------------------------
                       [INFO] 
                       [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ project-java ---
                       [INFO] ------------------------------------------------------------------------
                       [INFO] BUILD SUCCESS
                       [INFO] ------------------------------------------------------------------------
                       [INFO] Total time:  0.304 s
                       [INFO] Finished at: 2025-11-25T10:31:23Z
                       [INFO] ------------------------------------------------------------------------



```

---

## 📊 Example Target Directory After Build

```text
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

## 🧹 Clean Again
```bash
mvn clean
```
Removes `target/` folder and resets project.

Output:
```
                       [INFO] Scanning for projects...
                       [INFO] 
                       [INFO] -------------------------< alexa:project-java >-------------------------
                       [INFO] Building project-java 1.0-SNAPSHOT
                       [INFO] --------------------------------[ war ]---------------------------------
                       [INFO] 
                       [INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ project-java ---
                       [INFO] ------------------------------------------------------------------------
                       [INFO] BUILD SUCCESS
                       [INFO] ------------------------------------------------------------------------
                       [INFO] Total time:  0.304 s
                       [INFO] Finished at: 2025-11-25T10:31:23Z
                       [INFO] ------------------------------------------------------------------------



```
```text
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


---

## ✅ Summary
```
- `mvn clean` → Cleans project  
- `mvn compile` → Compiles source code  
- `mvn test` → Runs unit tests  
- `mvn package` → Builds JAR file  
- `mvn install` → Installs JAR into local repo  
```
This README provides a step-by-step guide to setting up, building, testing, and packaging the **Sample Maven Project** on AWS EC2.

```

✨ This README.md now acts as a **complete documentation** of your Maven project workflow, including EC2 setup, Maven lifecycle, outputs, and directory structures.  

Would you like me to also add **badges** (like build status, Java version, Maven version) at the top of the README to make it visually engaging for GitHub?


