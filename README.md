
### Disclaimer

This docker image is far from being truly persistent and docker-way. It is more like a beginning to start an evolved container but it is a good way to improve it.

### Special thanks
I started this images following the Official Nginx image and antoher one Composer project as well
I have to say thank you to: [Nginx official image](https://hub.docker.com/_/nginx/) | [Composer](https://hub.docker.com/r/graze/composer/)

### Supported tags and respective Dockerfile links
I've worked to automate this image using this [Dockerfile](https://github.com/starase/composer)


### Details
Image: Alpine 3.5
Process control system: supervisord

*Image size: ~130Mb*

### Software
* supervisor
* nginx
* php-fpm7
* composer


### Customizations
There are some customizations for my personal purposes and by default the root directory for nginx is /app 
If you need to use composer you have to link it because the work home directory is different as well
This image is almost ready for production environment but if you want do follow the best practice you need a SSL certificate. There are some ways to implement it but is not the scope of this opera


### Try it
You can pull the image and it will be up&running simply doing:

``` docker pull starase/composer ```

You can start it:

```docker run -d -i -t -v /host/directory:/app starase/composer```

Of course you can customize it. 
My reccomendation is to run it with persistent volume to preserve the data
Another thing you can do is puting name or hostname, simply adding ```--name name``` and ```--h hostname``` before the image's name




### Issues & Contributing
Before you start to code, we recommend discussing your plans through a GitHub issue, especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing. Otherwise you feel free to drop me a line at paolo [at] starase.com


> Have fun, happy dockerizing
