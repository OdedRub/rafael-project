# get jar file


FROM anapsix/alpine-java
RUN adduser -D kepler-alien
USER kepler-alien
ARG VER
ADD /target/myapp-$VER.jar /home/myjar.jar
CMD ["java","-jar","/home/myjar.jar"]
