# Docker Web Server

CodeAlpha DevOps Internship — Task 4  
Created by Kayalvili Balendran

## About
A simple website running with Nginx inside a Docker container.
An automatic health check checks whether the website is responding.

## Tools Used
- Docker Desktop
- Nginx
- HTML

## Build and Run
Make sure Docker Desktop is running.
Open PowerShell in the project folder and run:

```powershell
docker build -t codealpha-web:v2 .
docker run -d --name codealpha-project -p 127.0.0.1:8080:80 codealpha-web:v2
```

Open http://localhost:8080 in your browser.

## Check the Container
```powershell
docker ps
docker logs codealpha-project
```

The status should show `healthy` after about 15 seconds.

## Stop and Start
```powershell
docker stop codealpha-project
docker start codealpha-project
```