## Created by Greg Pearson
## This is how I install SonarQube on Redhat Rhel 9

### Step One ###
#### 1. Install RHel 9

#### 2. Setup RedHat Registration 
#### taken from (https://access.redhat.com/solutions/253273)

```Registration
  subscription-manager register --username <username> --password <password> --auto-attach
```

```Registration
  subscription-manager register
```

#### Per-sonarQube Instructions:
##### Proceed as follows to install SonarQube on server side:

    Install the SonarQube database.
    Install the SonarQube server and perform a basic setup. You can install the server either from the ZIP file or from the Docker image. 
    If necessary, perform advanced setup.


#### Install Java 11
```
sudo yum install java-11-openjdk-devel -y
```

#### Install the PostgreSQL Repository
```
sudo yum install -y https://download.postgresql.org/pub/repos/yum/reporpms/EL-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm

sudo yum -qy module disable postgresql
```


#### Problems:
```
There is an error with some of the repos

Error: Failed to download metadata for repo 'pgdg-common': repomd.xml GPG signature verification error: Bad GPG signature
```


#### Links
```
https://docs.sonarsource.com/sonarqube/latest/setup-and-upgrade/install-the-server-as-a-cluster/
```