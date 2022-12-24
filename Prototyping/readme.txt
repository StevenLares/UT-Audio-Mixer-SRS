When you compile using Clickable (using 'clickable desktop', 'clickable', etc), it will automatically download the image file from the relevant repo if it does not exist. If it does exist, but the dockerhub repo has a newer version, Clickable will download the new version while keeping the old one. This produces bloat.

Tips to reduce this bloat:

Run this command to list docker images and their IDs
docker image ls

Run the following command when you are switching between compilation type (for example switching from compiling for desktop to compiling for a connected phone)
docker rmi <image ID>


On the other hand, if it's been at least a day since you've last compiled your project (and you wish the compile it the same way as last time), then run
clickable update-images



Use the above tips to store at most one clickable docker image at a time. This will help with storage issues.
