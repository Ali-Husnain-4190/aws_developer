Step 1:
    - Create a Ec2 instance 
    - Download CWagent `wget https://s3.amazonaws.com/amazoncloudwatch-agent/amazon_linux/amd64/latest/amazon-cloudwatch-agent.rpm`

     - install it `sudo rpm -U ./amazon-cloudwatch-agent.rpm`

Step 2:
    - create IAM role
    - attach these policy 
             CloudWatchAgentServerPolicy
             AmazonSSMFullAccess 
    - attach role to EC2 

Step3:
    start cloud watch agent using this command
    - sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard





Command 
wget https://s3.amazonaws.com/amazoncloudwatch-agent/amazon_linux/amd64/latest/amazon-cloudwatch-agent.rpm

sudo rpm -U ./amazon-cloudwatch-agent.rpm


# IAM ROLE

EC2 Role
EC2
CloudWatchAgentServerPolicy
And AmazonSSMFullAccess 
CloudWatchRole

sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard
# Accept all defaults, until default metrics .. pick advanced.

# then when asking for log files to monitor

# 1 /VAR/LOG/SECURE
/var/log/secure
/var/log/secure
(Accept default instance ID)

# 2 /var/log/httpd/access_log
/var/log/httpd/access_log
/var/log/httpd/access_log
(Accept default instance ID)

# 3 /var/log/httpd/error_log
/var/log/httpd/error_log
/var/log/httpd/error_log
(Accept default instance ID)

# Config will be stored in /opt/aws/amazon-cloudwatch-agent/bin/config.json and stored in SSM

# Bug Fix
sudo mkdir -p /usr/share/collectd/
sudo touch /usr/share/collectd/types.db

# Load Config and start agent
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -c ssm:AmazonCloudWatch-linux -s
