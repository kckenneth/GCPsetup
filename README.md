# GCPsetup

This is a brief introduction to how to setup GCP (Google Cloud Platform). 

1. Create a VM (8CPUs, 30GB RAM, 200GB SSD, Ubuntu 16.04) 
- allow HTTP, HTTPs while creating a VM (for Jupyter access)
2. <a href=https://github.com/kckenneth/GCPsetup/blob/master/ssh_setup.md>Set up SSH to Google instance</a> [<a href=https://cloud.google.com/compute/docs/instances/adding-removing-ssh-keys#project-wide>Source</a>]
3. <a href=https://github.com/kckenneth/GCPsetup/blob/master/docker.md>Install Docker</a> [<a href=https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04>Source</a>] 
4. <a href=https://github.com/kckenneth/GCPsetup/blob/master/docker-compose.md>Install Docker Compose</a> [<a href=https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-16-04>Source</a>] 
5. <a href=https://medium.com/@kn.maragatham09/installing-jupyter-notebook-on-google-cloud-11979e40cd10>Open port for Jupyter notebook</a> 
- make the external IP as static 
> VPC network --> external IP addresses --> change Type from Ephemeral to Static  
- 8889 for jupyter notebook in Firewall setup 
> Create firewall rule 
> name: kchenjp  
> Targets = all instances in the network  
> Source filter = IP ranges  
> Source IP ranges = `0.0.0.0/0` manually typed in  
> Second source filter = None  
> Protocols and ports = specified protocols and ports = check tcp and type `8889`  
- 4040 for spark job visualization 

Transferring files from GCP to local machine 
```
$ scp -i ~/.ssh/w261 kchen@xx.xx.xx.xx:/home/kchen/main_work_for_homework/Assignments/FinalProject/notebook_Chen.ipynb
```
