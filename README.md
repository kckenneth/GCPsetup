# GCPsetup

This is a brief introduction to how to setup GCP (Google Cloud Platform). 

1. Create a VM (8CPUs, 30GB RAM, 200GB SSD, Ubuntu 16.04) allow HTTP, HTTPs while creating a VM 
2. <a href=https://github.com/kckenneth/GCPsetup/blob/master/ssh_setup.md>Set up SSH to Google instance</a> [<a href=https://cloud.google.com/compute/docs/instances/adding-removing-ssh-keys#project-wide>Source</a>]
3. <a href=https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04>Install Docker</a> 
4. <a href=https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-16-04>Install Docker Compose</a> 
5. <a href=https://medium.com/@kn.maragatham09/installing-jupyter-notebook-on-google-cloud-11979e40cd10>Open port for Jupyter notebook</a> 
- make the external IP as static 
- 8889 for jupyter notebook in Firewall setup 
- 4040 for spark job visualization 


