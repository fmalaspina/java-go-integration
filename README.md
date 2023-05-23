# java-go-integration

Java to Golang integration example

## 1. Clone the project

## 2. We need to build the Go code as a shared library (.so on Linux or .dll on Windows). Run the following command to build the library:

```sh
cd java-golang
go build -buildmode=c-shared -o golang/bin/lib-cqm-transformer.so golang/src/cqm_transformer.go
```

## 3. Build java project

```sh
mvn clean package
java -jar target/java-go-1.0-SNAPSHOT-jar-with-dependencies.jar
Java says: about to call Go ..
Go says: adding 30 and 12
Java says: result is 42
```
