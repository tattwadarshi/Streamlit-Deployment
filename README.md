# Streamlit-Deployment

**This project is an end to end implementation of a Bank Note authentication web application. We have containarized the entire application using Docker.**

Data were extracted from images that were taken from genuine and forged banknote-like specimens. For digitization, an industrial camera usually used for print inspection was used. The final images have 400x 400 pixels. Due to the object lens and distance to the investigated object gray-scale pictures with a resolution of about 660 dpi were gained. Wavelet Transform tool were used to extract features from images.

**The main idea is to predict whether a bank note is authentic.**

**Link** - https://streamlit-app-tattwa.herokuapp.com/

**The entire project includes the following steps:**
1. Building a machine learning model for detecting whether a bank note is authentic. 
2. Building A Flask App For A Bank Note Authentication. It will use the trained ML pipeline to generate predictions on new data points in real-time.
3. Deploying Machine Learning Models Using Flask And Flasgger
4. Writing, Building And Running Docker Image. Build a Docker file on your local computer. This step is basically to create a docker image and container.
5. Commit the code in GITHUB
6. Create an account in Heroku. Link the GITHUB to Heroku. 
7. Deploy the model. 
8. Web App is ready. 

**Important Note:**
**At the end of the day, docker is just a file with a few lines of instructions that are saved under your project folder with the name “Dockerfile”.**

**To deploy on Heroku you need two things:**
+ requirements.txt file
+ Procfile

**How to Get the requirements.txt file**

# Method 1: using pip
pip freeze > requirements.txt

# Method 2: using pipreqs (recommended)
+ First install pipreqs
pip install pipreqs
+ Second use pipreqs to get the requirements.txt file of any project
pipreqs yourmlapp_folder

**For the  procfile can I simply use: web: gunicorn app:app?**
+ What to Put inside the Procfile
+ web: gunicorn app:app

**should the static and templates folder remain the same for deployment as the one we prepared during Productionization?**
+ Yes,  you will have to push them too to github

**Procfile**
For Heroku you need to say which is the first file bascially you need to execute. 
web:gunicorn app: app
Which is your file of Flask you want to run first? app.py

**setup.sh**
Script program for bash that helps us to execute code with respect to requirement.txt. 
It helps us to setup environment for streamlit library. 

**Flasgger**
This will help us to create the UI part in a much feasible and easy way. It won't be that decorative but it would be a good front end web app. In Flasgger, Swagger will automatically generate the frontend UI part. 


**Advantages of Docker**
1. It standardizes the environment.
2. Build once and deploy it anywhere. 
3. Isolation - Isolate each of the environment separately.
4. Portability - You can take the docker container, put into another environment and it will be working in a similar way. 







