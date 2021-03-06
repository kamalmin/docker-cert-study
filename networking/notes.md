
# Networking

From here: https://docs.docker.com/engine/userguide/networking/work-with-networks/#link-containers-without-using-user-defined-networks

Note: Any link between containers created with legacy link is static in nature and hard-binds the container with the alias. It does not tolerate linked container restarts. The new link functionality in user defined networks supports dynamic links between containers, and tolerates restarts and IP address changes in the linked container.

That is probably the best reason I've heard for why they are deprecating the `--link` flag.

User defined bridge networks allow you to resolve other containers in the same network by there container name. This is not true for the default bridge network.

They really hammer home that you should be using Overlay networks for Docker Swarm and other multi-node setups. I suspect that will come up a lot on the exam.

I did not know you could do something like `-p="192.168.2.6::80"` to bind to a specific IP, and still assign an ephemeral port. I should have guessed.

From here: https://blog.docker.com/2016/12/understanding-docker-networking-drivers-use-cases/

The overlay driver utilizes an industry-standard VXLAN data plane that decouples the container network from the underlying physical network (the underlay).

Need to read more into MACVLAN networks.

There are lots of UCP components, and I don't know how much you'll need to know for the exam about which does what.
I'll rewatch this to be safe.
https://linuxacademy.com/cp/courses/lesson/course/1377/lesson/8/completed/7/module/150

Review this video, and the components, of UCP, and DTR.

https://docs.docker.com/v17.09/datacenter/dtr/2.4/guides/architecture/
