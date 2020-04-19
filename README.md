# Wicked Gravel
New England Gravel Route Mapping Server

## How to Run
Clone:
```
git clone https://github.com/mbeneck/wicked-gravel.git
cd wickedgravel
```

To build the docker image run:
```
sudo docker build -t gravelserver [--build-arg USER=<your-basic-auth-username>] [--build-arg PASSWD=<your-basic-auth-passwd>] gravelserver
```
If you omit the username and passwd, the default will be user:wicked, passwd:gravel.

Build the docker image by running:
```
sudo docker run -dit -v ${PWD}/public/:/usr/local/apache2/htdocs -v <absolute/path/to/your/graveltiles>:/usr/local/apache2/htdocs/tiles -p 8080:80 gravelserver
```
And voila! Your website should appear at <http://localhost:8080>

