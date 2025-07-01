Git Basics:
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
--Create a github repo--
git remote add origin https://repo.git
git remote -v
git push origin main/master
git pull origin master
git branch test_branch
git checkout test_branch
--makes changes in the .py file and commit--
git checkout master/main
git merge test_branch

Docker Basics:
docker --version
sudo docker images
sudo docker pull hello-world
sudo docker run hello-world
sudo docker run -p 80:80 -d nginx
sudo docker ps
sudo docker stop container_id

Flas app with docker:
nano app.py
"from flask import Flask, render_template, request
app=Flask(name)
@app.route("/")
def home_page(name=None):
return render_template("index.html",name=name)
if name == 'main':
app.run(host='0.0.0.0',port=5000)
" sudo apt install python3-pip

nano Dockerfile
"FROM python3-alpine3.15
WORKDIR /app
COPY ./app
RUN pip install flask
CMD ["python3","app.py"]

sudo docker build -t myimg:1 .
sudo docker run -p 8000:5000 myimg:1
--docker hub--
sudo docker login -u username
sudo docker tag myimg:1 username/dockerimage
sudo docker push username/dockerimage
docker logout

Jenkins sudo systemctl start jenkins
sudo systemctl status jenkins --check https://localhost:8080-- sudo more ... copy and paste the password -create new item->add github repo link->build a trigger "H/5 ****"->build steps->consol output
