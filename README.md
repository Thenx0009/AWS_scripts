# AWS

**LOAD BALANCER** The growth in the number of active users inevitably leads to an increase in the load on the servers. To ensure good UX it is necessary to properly balance the load. This is why the use of load balancer is important – it distributes network or application traffic between multiple servers in a server pool. Each load balancer resides between client devices and back-end servers, receiving and distributing incoming requests to any available server capable of fulfilling them.

![Alt text](Capture.PNG)
 ## Load Balancer Types
- [Classic load balancer](#classic)
- [Application load balancer](#application)
- [Network load balancer](#network)
- [Gateway load balancer](#gateway)

## 1. Classic load balancer <a name="classic"></a>
- Create atleast 3-4 instances with bootstrap script in the the 3 different availability zones.
![Alt text](<screenshots\Capture.PNG>)

- Check whether all the instances are running by copying their public IP-address on the browser. 
![Alt text](<screenshots\Screenshot (41).png>)
![Alt text](<screenshots\Screenshot (46).png>)
![Alt text](<screenshots\Screenshot (44).png>)