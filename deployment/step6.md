# title

add environment config  
`vi /etc/systemd/system/edgecore.service`{{execute}}  

[Service]  
**Environment=CHECK_EDGECORE_ENVIRONMENT='false'**  --add this line 
Type=simple  
ExecStart=/usr/local/bin/edgecore  
Restart=always  
RestartSec=10  


`vi /etc/kubeedge/config/edgecore.yaml`{{execute}}

edged:  
    **cgroupDriver: systemd**  --change from 'cgroupf' to 'systemd'  
    cgroupRoot: ""  
    cgroupsPerQOS: true  

restart  
`systemctl daemon-reload && sudo systemctl enable edgecore && sudo systemctl start edgecore`{{execute}}
