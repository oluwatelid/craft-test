FROM bellsoft/liberica-runtime-container:jdk-17-stream-musl as builder
WORKDIR /voting
COPY . .
RUN ./mvnw -Dmaven.test.skip=true clean package


FROM bellsoft/liberica-runtime-container:jre-17-musl
WORKDIR /voting
COPY --from=builder /voting/target/*.jar voting.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "voting.jar"]
