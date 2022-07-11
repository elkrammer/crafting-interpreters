JAR         = jar
JAVAC       = javac
SRCS        = $(wildcard $(SRC_PATH)*.java)
SRC_PATH    = com/interpreter/jlox
TOOLS_PATH  = com/interpreter/tools

all: build

build: $(SRCS)
	$(JAVAC) $(SRC_PATH)/*.java 
	$(JAR) cmvf META-INF/MANIFEST.MF bin/jlox.jar $(SRC_PATH)/*.class

tools:
	$(JAVAC) $(TOOLS_PATH)/*.java
	$(JAR) cmvf META-INF/TOOLS-MANIFEST.MF bin/generate_ast.jar $(TOOLS_PATH)/*.class
	
run:
	java -jar bin/jlox.jar

clean:
	rm -f com/interpreter/jlox/*.class
	rm -f com/interpreter/tools/*.class
	rm -f bin/{jlox.jar,generate_ast.jar}
