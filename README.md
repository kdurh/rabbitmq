# rabbitmq
# Set environment variable
set CP=./lib;amqp-client-5.16.0.jar;slf4j-api-1.7.36.jar;slf4j-simple-1.7.36.jar
set CP=./lib/amqp-client-5.16.0.jar;./lib/slf4j-api-1.7.36.jar;./lib/slf4j-simple-1.7.36.jar

# Compile
javac -cp "./lib/amqp-client-5.16.0.jar;./lib/slf4j-api-1.7.36.jar;./lib/slf4j-simple-1.7.36.jar" NewTask.java Worker.java

java -cp %CP% Send

# Execute
java -cp ".;lib/*" NewTask