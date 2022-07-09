JAVAC    = javac
JAR      = jar
SRC_PATH = com/interpreter/jlox/

SRCS=$(wildcard $(SRC_PATH)*.java)

all: build

build: $(SRCS)
	$(JAVAC) $(SRC_PATH)*.java 
	$(JAR) cmvf META-INF/MANIFEST.MF jlox.jar $(SRC_PATH)*.class

run:
	java -jar jlox.jar

clean:
	rm -f com/interpreter/jlox/*.class
	rm -f jlox.jar
