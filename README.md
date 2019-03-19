# Compile and Install with GO
```
 # cd /usr /src
 # git clone https://github.com/mobarrio/sapccmsget.git
 # cd sapccmsget/
 # wget https://dl.google.com/go/go1.12.1.linux-amd64.tar.gz
 # tar -C /usr/local -xzf go1.12.1.linux-amd64.tar.gz
 # rm go1.12.1.linux-amd64.tar.gz
 # export PATH=$PATH:/usr/local/go/bin
 # export GOBIN="/usr/src/sapccmsget/bin/"
 # export GOPATH="/usr/src/sapccmsget/"
 # export GOROOT="/usr/local/go"
 # go install
```

# sapccmsget
Utility to get performance data from SAP CCMS monitoring tree element by full name. Used by zabbix-agent.

# example: 

Command 
>`[user@host1 ~]$ zabbix_agentd -c /etc/zabbix/zabbix_agentd.conf -t "sap.ccms.get[SID, 'SID\\host1_SID_00\\R3Services\\Dialog\\ResponseTime']"`

will produce output:
>`sap.ccms.get[SID, 'SID\host1_SID_00\R3Services\Dialog\ResponseTime'] [t|89]`
