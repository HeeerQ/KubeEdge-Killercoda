# Setup Edge Side (KubeEdge Worker Node)

Run keadm gettoken in cloud side will return the token, which will be used when joining edge nodes. Save the returned value to the variable token_value.

`token_value=$(keadm gettoken)`{{execute}}  
  
    
   
Next, run keadm join to join edge node.  
  
`keadm join --cloudcore-ipport=172.30.1.2:10000 --token=echo $token_value`{{execute}}  
the value for token is the token returned from cloud side.

keadm join will install edgecore and mqtt, and --cloudcore-ipport flag is a mandatory flag.   
  
   
Now you can see KubeEdge edgecore is running.


