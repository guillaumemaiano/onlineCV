FROM httpd:2.4        
# CORS blocks Swagger-UI from reading HTTPDed JSON from other containers
#run: echo '
        #             \nSetEnvIf Referer "^https://localhost\/.*$" request-swagger
        #           \nHeader set Access-Control-Allow-Origin "localhost" env=request-swagger
        #           \nRewriteCond "%{HTTP_HOST}" "^localhost"
        #           \nRewriteCond "%{REQUEST_METHOD}" =OPTIONS
        #           \nRewriteRule "^.*$" - [R=200]'  >>
# quick but terrible security-wise: 
RUN echo "Header set Access-Control-Allow-Origin '*'" >> /usr/local/apache2/conf/httpd.conf && apachectl restart 
