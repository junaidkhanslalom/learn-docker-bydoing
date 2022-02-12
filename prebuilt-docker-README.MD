. Working With Prebuilt Docker
    1. Get and View httpd
        In the Docker Instance, verify that docker is installed:
        ### docker ps
    2. Using docker, pull the httpd:2.4 image:
        ### docker pull httpd:2.4
    3. Run the image:
        ### docker run --name httpd -p 8080:80 -d httpd:2.4
    4. Check the status of the container:
        ### docker ps
    5. In a web browser, test connectivity to the container:
        ### <PUBLIC_IP_ADDRESS>:8080
    6. Run a Copy of the Website in httpd
    Clone the Widget Factory Inc repository:
    ### git clone https://github.com/linuxacademy/content-widget-factory-inc
    7. Change to the content-widget-factory-inc directory:
        ### cd content-widget-factory-inc
    8. Check the files:
        ### ll
    9. Move to the web directory:
        ### cd web
    10. Check the files:
        ### ll
    11. Stop the httpd container:
        ### docker stop httpd
    12. Remove the httpd container:
        ### docker rm httpd
    13. Verify that the container has been removed:
        ### docker ps -a
    14. Run the container with the website data:
        ### docker run --name httpd -p 8080:80 -v $(pwd):/usr/local/apache2/htdocs:ro -d httpd:2.4
    15. Check the status of the container:
        ### docker ps
    16. In a web browser, check connectivity to the container:
        ### <PUBLIC_IP_ADDRESS>:8080
    17. Get and View Nginx
        Using docker, pull the latest version of nginx:
        ### docker pull nginx
    18. Verify that the image was pulled successfully:
        ### docker images
Run the container using the nginx image:
### docker run --name nginx -p 8081:80 -d nginx 
Check the status of the container:
### docker ps
Verify connectivity to the nginx container:

### <PUBLIC_IP_ADDRESS>:8081
Run a Copy of the Website in Nginx
Stop the nginx container:
### docker stop nginx
Remove the nginx container:
### docker rm nginx
Verify that the container has been removed:
### docker ps -a
Run the nginx container, and mount the website data:
### docker run --name nginx -v $(pwd):/usr/share/nginx/html:ro -p 8081:80 -d nginx
Check the status of the container:
### docker ps
In a web browser, verify connectivity to the container:
### <PUBLIC_IP_ADDRESS>:8081
Stop the nginx container:
### docker stop nginx
Remove the nginx container:
### docker rm nginx
Verify that the container has been removed:
#### docker ps -a
