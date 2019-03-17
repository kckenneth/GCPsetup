### Step 1 — Installing Docker Compose
Although we can install Docker Compose from the official Ubuntu repositories, it is several minor version behind the latest release, so we'll install Docker Compose from the Docker's GitHub repository. The command below is slightly different than the one you'll find on the Releases page. By using the -o flag to specify the output file first rather than redirecting the output, this syntax avoids running into a permission denied error caused when using sudo.

We'll check the current release and if necessary, update it in the command below:
```
sudo curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
```
Next we'll set the permissions:
```
sudo chmod +x /usr/local/bin/docker-compose
```
Then we'll verify that the installation was successful by checking the version:
```
docker-compose --version
```
This will print out the version we installed:
```
Output
docker-compose version 1.18.0, build 8dd22a9
```
Now that we have Docker Compose installed, we're ready to run a "Hello World" example.
