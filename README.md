     
# ***** Sample-maven-Project *****

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

## ⚠️ Important Notes

- Before running `mvn package`, execute:
  ```bash
  mvn clean
  mvn compile
  mvn test
  mvn package
  ```

- Before running `mvn test`, execute:
  ```bash
  mvn clean
  mvn compile
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
[INFO] BUILD SUCCESS
```

---

### Compile
```bash
mvn compile
```
Creates `target/` folder with compiled `.class` files.

Output:
```
[INFO] BUILD SUCCESS
```

---

### Test
```bash
mvn test
```
Generates reports in `target/surefire-reports`.

Output:
```
[INFO] BUILD SUCCESS
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
[INFO] BUILD SUCCESS
```

---

## 📊 Example Target Directory After Build

```text
target
├── classes
│   └── com/mycompany/app/App.class
├── generated-sources/annotations
├── generated-test-sources/test-annotations
├── maven-archiver/pom.properties
├── maven-status/maven-compiler-plugin
│   ├── compile/default-compile
│   └── testCompile/default-testCompile
├── my-app-1.0-SNAPSHOT.jar
├── surefire-reports
│   ├── TEST-com.mycompany.app.AppTest.xml
│   └── com.mycompany.app.AppTest.txt
└── test-classes/com/mycompany/app/AppTest.class
```

---

## 🧹 Clean Again
```bash
mvn clean
```
Removes `target/` folder and resets project.

Output:
```
[INFO] BUILD SUCCESS
```

---

## ✅ Summary
- `mvn clean` → Cleans project  
- `mvn compile` → Compiles source code  
- `mvn test` → Runs unit tests  
- `mvn package` → Builds JAR file  
- `mvn install` → Installs JAR into local repo  

This README provides a step-by-step guide to setting up, building, testing, and packaging the **Sample Maven Project** on AWS EC2.

```

✨ This README.md now acts as a **complete documentation** of your Maven project workflow, including EC2 setup, Maven lifecycle, outputs, and directory structures.  

Would you like me to also add **badges** (like build status, Java version, Maven version) at the top of the README to make it visually engaging for GitHub?


