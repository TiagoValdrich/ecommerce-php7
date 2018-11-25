#E-commerce Project

This is a project was developed in Udemy's course: [Curso de PHP 7](https://www.udemy.com/curso-completo-de-php-7/).

The template that was used is: [Almsaeed Studio](https://almsaeedstudio.com).

## Testing/see the project

If you want to test or see the project, here are some recomendations:

    * You must have version 7 of [XAMPP](https://www.apachefriends.org/pt_br/index.html);
    * You need to create a new database in your localhost with the name db_ecommerce, and import with the archive that is in the folder "database";
    * Clone this project inside htdocs;
    * Configure your hosts in C:\Windows\System32\drivers\etc  *<- If you are using Windows*, and set this:
    ```
        127.0.0.1           www.hcodecommerce.com.br
    ```
    * Configurate your httpd-vhosts.conf file:
    ```
        <VirtualHost *:80>
            ServerAdmin somerandomemail@gmail.com 
            DocumentRoot "C:/xampp7/htdocs/ecommerce" <-- Here you need to change the path 
            ServerName www.hcodecommerce.com.br <-- The host configuration that you applied in hosts
            ErrorLog "logs/dummy-host2.example.com-error.log"
            CustomLog "logs/dummy-host2.example.com-error.log" common
            <Directory "C:/xampp7/htdocs/ecommerce"> <-- Change the path here too
                Require all granted

                RewriteEngine on

                RewriteCond %{REQUEST_FILENAME} !-d
                RewriteCond %{REQUEST_FILENAME} !-f
                RewriteRule ^ index.php [QSA,L]
            </Directory>
        </VirtualHost>
    ```
    * Restart or turn on the Apache and the MySQL;
    * After this you only need to have a browser, a computer or notebook and test the project ;).