
lox: build
	java -cp bin/lox com.craftinginterpreters.lox.Lox

build: bin generate-ast
	javac -d bin/lox src/com/craftinginterpreters/lox/*.java

generate-ast: build-tool
	java -cp bin/lox com.craftinginterpreters.tool.GenerateAst src/com/craftinginterpreters/lox

build-tool: bin
	javac -d bin/lox src/com/craftinginterpreters/tool/*.java

clean:
	rm -rf bin

bin:
	mkdir -p bin/lox
