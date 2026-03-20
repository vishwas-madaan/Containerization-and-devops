## Class 2 - Dockerfile Basics

This class demonstrates a simple Java application containerization using Docker.

---

### 📄 Files Included

- `hello.java` → Java program  
- `Dockerfile` → Instructions to build Docker image  

---

### 💻 Java Program

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello Docker");
    }
}


### Dockerfile

FROM openjdk:11
COPY hello.java /app/
WORKDIR /app
RUN javac hello.java
CMD ["java", "Hello"]


##  Steps to Run
```bash
Build Docker image:

docker build -t java-app .

Run container:

docker run java-app
```
## Output
```bash
Hello Docker
```
## conclusion
```bash
This experiment demonstrates how to containerize a basic Java application using Docker.
```