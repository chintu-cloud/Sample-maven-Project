Here’s a clean and professional **README.md** you can use for your `Sample-maven-Project`. It documents the Maven lifecycle, project structure, and EC2 setup exactly as you’ve demonstrated:

```markdown
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

## 🎯 Summary

This project is a minimal Maven-based Java application that prints **Hello World!** and includes a unit test. It demonstrates the Maven lifecycle (`clean → compile → test → package → install`) and can be deployed easily on AWS EC2.
```

---

Would you like me to also add **badges** (like build status, Java version, Maven version) at the top of the README to make it visually engaging for GitHub?

