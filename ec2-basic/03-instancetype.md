# Ec2 instance Type:
    When you choose Ec2 instance you think different point
        1) RAW; see local storage, CPU, Memory and type
        2) resource ratio (mean what thing you want more memory or storage or somthing else)
        3) Storage , Data Network bandwidth . for example you have  are using high available EBS but you instance is not compatible with it
        4) System architecture / vender like arm or intel
        5) 

Ec2 categories:
    General purpose:
        Default , driver workload, requal resources 
    Compute optimize:
        media processing, gameing High perforamance CPU, machine learning 
    Memory optimize:
        Processing larg in memory dataset, some database workload
    Accerlrating computing:
        Hardware GPU, filed programmable gate array (FPGA)
    Storage optimize:
        Sequential and random IO, scale out transactional database , data warehousing , Elastic search, analytic workload
    


# Decoding Ec2 Type:   

        R5dn.8xlarg : The whole thing is known as instance type.
        R: instance family 
        5: generation  R5 mean fifht generation of R family
        8xlarg: size, which mean how much memory and cpu instance using
            we have small, larg, medium, extra larg and so on
        dn: additional capabilities common example lower case a represent amd ,b which represent NVM storage.


```
https://aws.amazon.com/ec2/instance-types/
```

```
https://instances.vantage.sh/
```




    