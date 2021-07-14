## Create a secure NodeJS web app using lets encrypt with nginx inside docker with docker compose

### Motivation
---
I create this repository so everyone can setup their own https Node JS web app easily by just following the instruction. I found it is quite hard to learn how to setup a Node JS https website using nginx inside docker. So I hope you can setup a Node JS https website by following this short tutorial. The result of the Node JS https website will have grade A SSL.

<br/>

---
### Notes
---
Special Thanks to the author of the website https://pentacent.medium.com/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71

1. I follow this tutorial for the lets encrypt with nginx setup. And highly recommend you to read it to know the setup explanation.
2. `init-letsencrypt.sh` file is also downloaded from https://github.com/wmnnd/nginx-certbot

<br/>

---
### Prerequisite
---
1. Docker installed in machine(VPS).
2. Docker Compose installed in machine(VPS).
3. Domain(Free or Paid).

<br/>

---
### Docker
---
In here, I use 3 docker images:
1. node js -> expose port 5000
2. nginx
3. certbot

Then, I use docker compose to run those containers.

<br/>

---
### Configuration
---
##### nginx/default.conf
Change all `test.com` to your domain.

##### init-letsencrypt.sh
1. Change all `test.com` to your domain.
2. Change `email` to your email address.

<br/>

---
### How to Run
---
1. Clone this repository.
2. Do the configuration.
3. Run `chmod +x init-letsencrypt.sh` in the clone root dir.
4. Run `sudo ./init-letsencrypt.sh` in the clone root dir.
5. Run `docker-compose up --build -d` in the clone root dir to rebuild the container.
6. Go to your domain.com, and you will see `Hello from finic two three` sentence if the configuration is success.
