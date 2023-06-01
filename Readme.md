### Go and the  SSH

#### Taken from the gopher academy blog. [GO and SSH](https://blog.gopheracademy.com/go-and-ssh/?utm_source=golangweekly&utm_medium=email)


#### golang weekly episode 41.


### goal of this practice
#### Let’s design a simple authentication system. Imagine we have a distributed system made up of services. There is always one service per host, and a central discovery service which stores host information: ID, service type, IP address and public key. Each server hard-codes the discovery service’s IP address and public key. At deploy time, the deploy machine generates a key pair for the new service and securely adds the new host to the the discovery service. Private keys are never shared. When a service receives a connection for first time, it compares the source IP address and received public key with the information from the discovery service, and accepts or rejects it. And that is it.