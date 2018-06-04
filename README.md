# PaginaCadastro

The project

This is a project of a web interface for Biologix - a brazilian biomed engineering startup.
https://www.biologix.com.br/

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

What my work does so far:

It has two files: index.html and index.php. The first one contains code to a simple file in which that user shall input all necessary information. It sends to index.php the information collected and index.php turns it into POST variables.

What I still need to figure out: 

1) How to make index.php communicate with server https://dev.biologix.com.br/api/v1/core/users/add
2) Once it communicates, I can start analysing data sent from html before making the request to the server. I belive this sould be done in index.php: i) find a method to evaluate if inputed cpf is valid (maybe a checksum?) ii) Same to e-mail; iii) verify is the birth date inputed is in correct format and verify the user's age if necessary; iv) Verify is password and passwordRetype are the same; 
3) I wanted to implemet 'acceptedTerm' as a checkbox (in c# would be relatively easy to do so), but it's currently as an html boolean;
4) Verify if the form in index.html is sending data in the correct order (validationOrder);
5) Finally generate a random signUpToken.

There were struggles with the testing part using the website provided (codepunker). I then changed to another website and it worked fine using post parameters. 

I'm currently watching online video courses to learn, as this one:

https://www.udemy.com/curso-completo-do-desenvolvedor-web/learn/v4/overview


