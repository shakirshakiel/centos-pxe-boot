# centos-pxe-boot

1. Download centos image http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Everything-1804.iso
2. Create a virtual machine
3. Install centos (Server with GUI)
4. Power off the machine
5. Create a host-only network

    a. VirtualBox -> Host Network Manager -> Create (vboxnet0)
    
    b. In centos machine -> Settings -> Network -> Adapter 2 -> Enable Network Adapter -> Host only network -> vboxnet0
    
6. Power on the machine
7. Check the bi-directional connectivity between guest and host
8. Setup pxe server in centos
  
  a. Follow the link - https://www.linuxtechi.com/configure-pxe-installation-server-centos-7/. Use the files in the repo
  
9. Create another machine (pxe-client)
  
  a. Choose redhat flavor
  
  b. Select RAM (2048 MB) and not 1024 MB (Ref: https://www.spinics.net/lists/centos/msg165578.html)
  
  c. Select only one Network adapter - Host only network
  
10. Boot the pxe-client
