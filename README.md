# PaginaCadastro

The project

This is a project of a web interface for Biologix - a brazilian biomed engineering startup.

Using Bitnami's WAMP stack for Windows x64 https://bitnami.com/stack/wamp

To run project:

1. Download and install the WAMP stack above;
2. Go to folder installdir (where the installation was saved) 
3. Go to installdir/apps and create a new folder "cadastro"
4. Save the files from this repository into installdir/apps/cadastro/
5. Go to installdir/apache2/conf/bitnami/bitnami-apps-prefix.conf and add at the end of the file as below

Include "installdir/apps/myapp/conf/httpd-prefix.conf"

6. Restart Apache
7. You can access the project in localhost/cadastro

(this tutorial was based on: https://docs.bitnami.com/installer/)

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
