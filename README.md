# Git Basics:
sudo apt install git  
git --version  
mkdir project  
cd project  
nano example.py  
python3 example.py  
git init  
git status  
git add .  
git commit -m "Message"  
git log  

--Create a GitHub repo--  
git remote add origin https://repo.git  
git remote -v  
git push origin main/master  
git pull origin master  
git branch test_branch  
git checkout test_branch  

--make changes in the .py file and commit--  
git checkout master/main  
git merge test_branch  
markdown
Copy
Edit
# Docker Basics:
docker --version  
sudo docker images  
sudo docker pull hello-world  
sudo docker run hello-world  
sudo docker run -p 80:80 -d nginx  
sudo docker ps  
sudo docker stop container_id  
markdown
Copy
Edit
# Flask App with Docker:
nano app.py  
<pre><code>from flask import Flask, render_template, request app = Flask(__name__) @app.route("/") def home_page(name=None): return render_template("index.html", name=name) if __name__ == '__main__': app.run(host='0.0.0.0', port=5000) </code></pre>
bash
Copy
Edit
sudo apt install python3-pip  
nano Dockerfile  
<pre><code>FROM python:3-alpine3.15 WORKDIR /app COPY ./app /app RUN pip install flask CMD ["python3", "app.py"] </code></pre>
bash
Copy
Edit
sudo docker build -t myimg:1 .  
sudo docker run -p 8000:5000 myimg:1  

--Docker Hub--  
sudo docker login -u username  
sudo docker tag myimg:1 username/dockerimage  
sudo docker push username/dockerimage  
docker logout  
markdown
Copy
Edit
# Jenkins:
sudo systemctl start jenkins  
sudo systemctl status jenkins  
Go to: https://localhost:8080

bash
Copy
Edit
sudo more /var/lib/jenkins/secrets/initialAdminPassword
Jenkins Setup Steps:

Create new item

Add GitHub repo link

Add a build trigger: "H/5 * * * *"

Add build steps

Check console output

yaml
Copy
Edit

---

This version will show up **exactly line by line** in your README. Let me know if you want it 
