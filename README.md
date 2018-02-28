# bmQueues

Useful links for JMS queue - thread management for consumer / producers.

http://www.ateam-oracle.com/inside-fusion-middleware-12c-increasing-scalability-with-jms-adapter-12c/

No. of threads we specify in - adapter.jms.receive.threads ( Consume_Message ) = 10 



JMS Adapter threads in SOA Suite 12c

The new 12c feature to control the thread creation is provided as a new configuration property:

adapter.jms.DistributedDestinationConnectionEveryMember=false  (default is true)

The documentation describes the usage of this property (see chapter 8.3.1.6 in  “Understanding Technology Adapters”):

When true, the JMS Adapter creates a consumer/subscriber for each member of the Distributed Destinations (the author: this is the default and was the setting in 11g). If set to false, the JMS Adapter creates a consumer/subscriber for only local members of the distributed destination.
When the JMS Adapter is connecting to distributed destination on a remote cluster or a server on remote domain, the property ‘adapter.jms.DistributedDestinationConnectionEveryMember’ should always be set to true. When the JMS Adapter is connecting to distributed destination on a local cluster, the property can be set to either true or false. If set to true, the JMS Adapter behavior remains the same as before (that is, there is a consumer for each Distributed Destination is created). If set to false, the JMS Adapter only creates consumer/subscriber for the local members.
