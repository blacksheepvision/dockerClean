# Mass Docker container remover

I had 50+ docker containers on my pc that I wanted to clean, don't know 
if there is a simple solution. I didn't want to delete all just keep 5 of them.

To generate container list:

```bash
sudo docker ps -a | awk '{print $1}' > containers.txt
```

And to remove unwanted containers:

```bash
cat containers.txt | sudo ./rmContainers.sh
```
