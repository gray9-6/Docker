# Base images
FROM openjdk:11

# Working directory
WORKDIR /usr/src/myapp

# copy from source(copy all ) to destination(/usr/src/myapp)
COPY . /usr/src/myapp

# compile kiya 
RUN javac Test.java

#  run kar diya 
CMD [ "java","Test" ]