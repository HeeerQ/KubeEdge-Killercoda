# Setup Edge Side (KubeEdge Worker Node)

Run keadm gettoken in **cloud side** will return the token, which will be used when joining edge nodes.

`keadm gettoken`{{execute HOST1}}  
  
    
   
Next, run keadm join in **edge side** to join edge node.  
  
`keadm join --cloudcore-ipport=192.168.20.50:10000 --token=value`{{}}  
the value for token is the token returned from cloud side.

keadm join will install edgecore and mqtt, and --cloudcore-ipport flag is a mandatory flag.   
  
   
Now you can see KubeEdge edgecore is running.
