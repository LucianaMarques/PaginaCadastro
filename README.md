# PaginaCadastro

The project

This is a project of a web interface for Biologix - a brazilian biomed engineering startup.

Using Bitnami's WAMP stack for Windows x64 https://bitnami.com/stack/wamp

Project's requirements:

The application should communicate using HTTP with the URL: https://dev.biologix.com.br/api/v1/core/users/add
In order to do so, it should send a POST messege and in return get a response in JSON format.

The request should contain the following:

- Name (string) - mandatory
- E-mail (string) - mandatory
- cpf (string) - mandatory
- birth date (date) - mandatory
- password (string) - mandatory
- passwordRetype (string) - optional 
- gender (char) - mandatory
- acceptedterm (checkbox) - optional
- validationOrder - optional
- signUpToken (string) - mandatory
