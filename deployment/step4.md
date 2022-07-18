# Setup Cloud Side (KubeEdge Master Node)

keadm init will install cloudcore, generate the certs and install the CRDs.

`keadm init --advertise-address=172.30.1.2`{{execute HOST1}}

--advertise-address (non-mandatory flag) is the address exposed by the cloud side (will be added to the SANs of the CloudCore certificate), the default value is the local IP.

Now you can see KubeEdge cloudcore is running.
