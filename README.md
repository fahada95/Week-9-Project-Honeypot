# Week 9 Project - Honeypot
Submission for week 9 assignment.

## Which Honeypot(s) you deployed
I only deployed the Dionaea honeypot from Modern Honey Network.

## Any issues you encountered
I had minor issues setting up Google Cloud. This is because the directions assumed a bit of prior knowledge which I was not familiar with. I stumbled my way through this and was successfully able to create two VMs on Google's Compute service.

The biggest issue I had was with the install script being out of date. One of the repositories that is a dependency of the honeypot no longer existed. This would cause the install script to error out. After a bit of googling, I found that the repo had changed locations and was now under the management of a different team on GitHub. Therefore I had to replace line 70 in install_hpfeeds.sh with the new github repo link. After doing this, I was able to run through the installation process without issue. 

I also found that after accidentally deleting the sensor from the admin console in MHN, I was not able to see the attacks from the sensor page, however I was still able to see the attacks from the Attacks page. This was a minor issue. 

## A summary of the data collected: number of attacks, number of malware samples, etc.

After deploying the honeypot, I was able to get some attacks. In only a short amount of time, the admin console about 37 attacks. The total number of attacks I was able to get, which was about a 10 minute duration, was 40. All attacks were to the Dionaea honeypot. Both the source and destination ports varied. The protocol for every attack was PCAP which is a packet capture which was attempting to identify open ports on our honeypot instance.

## Any unresolved questions raised by the data collected

In my attacks I only saw pcaps. What do other attacks look like?
