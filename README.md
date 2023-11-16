# AWS

**LOAD BALANCER** The growth in the number of active users inevitably leads to an increase in the load on the servers. To ensure good UX it is necessary to properly balance the load. This is why the use of load balancer is important – it distributes network or application traffic between multiple servers in a server pool. Each load balancer resides between client devices and back-end servers, receiving and distributing incoming requests to any available server capable of fulfilling them.

![Alt text](screenshots/Capture.PNG)
 ## Load Balancer Types
- [Classic load balancer](#classic)
- [Application load balancer](#application)
- [Network load balancer](#network)
- [Gateway load balancer](#gateway)

## 1. Classic load balancer <a name="classic"></a>
- Create atleast 3-4 instances with bootstrap script in the the 3 different availability zones.
![Alt text](<screenshots/Screenshot (45).png>)

- Check whether all the instances are running by copying their public IP-address on the browser. 

Instance1
![Alt text](<screenshots/Screenshot (41).png>)
Instance2
![Alt text](<screenshots/Screenshot (46).png>)
Instance3
![Alt text](<screenshots/Screenshot (44).png>)

- Create Classic Load Balancer and add all the 3 target instances.
![Alt text](<screenshots/Screenshot (48).png>)

- Select the classic load balancer, go to details and copy the DNS name for example-http://classiclb-1652469063.ap-south-1.elb.amazonaws.com/.

- Paste the DNS name on the browser, reload the page again and again to check whether load balancer is working or not.
![Alt text](screenshots/lb.PNG)

- Remove the access of instances that are directly accessed from their IP addresses. By removing the HTTP security group from each instances.
 ![Alt text](<screenshots/Screenshot (49).png>)
Now, again copy the ip address of instances are running or not. If they are not respnse back it means you are on a right path and the target-instances of load balancer will show Out of Service.
![Alt text](<screenshots/Screenshot (52).png>)

- Now, again edit all the instances security group
and add the Type-HTTP & source-add the security group of load balancer which shows in the below ss.
![Alt text](<screenshots/Screenshot (53).png>)
Here we can see that the one instance which is attached to load balancer security group comes In-service.
![Alt text](<screenshots/Screenshot (54).png>)
Do the same with all the remaining servers.

- After doing the above task, now if we check the load balancer target instances it will show In-service.
![Alt text](<screenshots/Screenshot (55).png>)
after this the load balancer will again start working.