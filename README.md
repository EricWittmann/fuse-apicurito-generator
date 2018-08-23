# Fuse Apicurito Generator

This project implements Fuse specific project generators that the
[Apicurito](https://github.com/Apicurio/apicurito) project can be
configured to use.


# Building

    mvn clean install

# Running

    java -jar target/fuse-apicurito-generator-*-SNAPSHOT.jar

# Testing with Curl

Assuming you create an open OpenAPI file called `api.json` and you want
to generate file called `example.zip`, then you would run the following:

     curl -s -X POST -H "Content-Type: application/json" \
          -d @api.json http://localhost:8080/api/v1/generate/camel-project.zip \
          -o example.zip

If you want to just test against the Swagger Petstore API, you run:

     curl -s http://localhost:8080/api/v1/generate/camel-project.zip \
          -o example.zip

See the `README.md` in zip file for more details about the generate project.