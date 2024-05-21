Create a simple FastAPI web application that has an endpoint enabling inference of Llama3 8b model. Endpoint should just take any text input like for example "How to create a fast api application?" and respond back with Llama model output.

Dockerize the application, starting the docker container should bring up the fastapi server, enabling us to make HTTP requests and get a response.

Set up Github Actions that will build the latest version of the fastapi code from the repo as a docker image and push to dockerhub

Any code changes made to github should be reflected in the docker image in the dockerhub (essentially building an new image and pushing it to dockerhub)

End result: I want to be able to change the system prompt in GitHub and have a docker image that I can run to start doing Llama3 inferences.

Bonus: Make the Llama3 model as part of docker image instead of it getting pulled from huggingface every time the container starts. First docker build can be slower, but the subsequent builds after changing the system prompt in github should be quicker (< 5 minutes)
