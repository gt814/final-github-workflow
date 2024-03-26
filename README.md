# Create a docker image.
docker build -t gt814/final-github-workflow:v1.0.0 .

# Start a docker container. 
docker run gt814/final-github-workflow:v1.0.0

# Add tag for activate a go-push action.
git tag v1.0.0
git push --tags 

# Start a container from DockerHub.
docker pull --platform linux/x86_64 gt814/final-github-workflow:v1.0.0