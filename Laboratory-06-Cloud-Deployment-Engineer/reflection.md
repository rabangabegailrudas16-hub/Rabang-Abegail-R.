
# Mission Reflection

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because it allows the configuration of multiple containers to be written in one file. Instead of manually typing many Docker commands, the engineer can use one command to deploy the complete application. This also makes the deployment more consistent and easier to repeat.

An indentation error in a YAML file can prevent Docker Compose from reading the configuration correctly. YAML depends on proper indentation, so using a Tab instead of spaces or placing an item at the wrong level can result in an error. This shows why careful formatting is important when working with Infrastructure as Code.

We used environment variables such as `MYSQL_PASSWORD` to provide configuration values to the containers. These variables allow the application and database to use the required settings without placing configuration directly into application commands. Environment variables also make configurations easier to modify when needed.

It was interesting to deploy a private cloud storage system such as Nextcloud in only a few minutes. Before this activity, deploying multiple services seemed more complicated because each component had to be configured separately. Docker Compose made the process easier because the database and application could be defined and deployed together.

Since Mission 1, my understanding of Cloud Computing has improved significantly. I learned that cloud computing is not only about using online services but also about deploying, managing, and documenting infrastructure. I now have a better understanding of containers, cloud infrastructure, Docker, storage, networking, and Infrastructure as Code. This mission helped me understand how the different concepts I learned from previous activities can work together to create a complete cloud application.
