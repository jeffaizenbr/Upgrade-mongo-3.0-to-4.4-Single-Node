# Upgrade-mongo-3.0-to-4.4-Single-Node to replica set

############################ STEP 1 ##############################

## 01 - Upgrade 3.0 to 3.2
obs: First, disable authentication and then edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 3.0 to 3.2
```bash
[mongodb-org-4.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/7/mongodb-org/3.2/x86_64/
gpgcheck=0
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.4.asc
```
## 02 - Upgrade 3.0 to 3.2
Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```
############################ STEP 2 ##############################

## 01 - Upgrade 3.2 to 3.4
Stop de mongod daemon, and edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 3.2 to 3.4

## 02 - Upgrade 3.2 to 3.4

Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```
## 03 - Upgrade 3.2 to 3.4

Verify de compability mode
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { getParameter: 1, featureCompatibilityVersion: 1 } )'
```
chage to mongo 3.4
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "3.4" } )'
```

############################ STEP 3 ##############################

## 01 - Upgrade 3.4 to 3.6

Stop de mongod daemon, and edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 3.4 to 3.6

## 02 - Upgrade 3.4 to 3.6

Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```

## 03 - Upgrade 3.4 to 3.6

Verify de compability mode
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { getParameter: 1, featureCompatibilityVersion: 1 } )'
```
chage to mongo 3.6
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "3.6" } )'
```

############################ STEP 4 ##############################

## 01 - Upgrade 3.6 to 4.0
Stop de mongod daemon, and edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 3.6 to 4.0


## 02 - Upgrade 3.6 to 4.0
Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```

## 03 - Upgrade 3.6 to 4.0
Verify de compability mode
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { getParameter: 1, featureCompatibilityVersion: 1 } )'
```
chage to mongo 3.6
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "3.6" } )'
```


############################ STEP 5 ##############################

## 01 - Upgrade 4.0 to 4.2

Stop de mongod daemon, and edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 4.0 to 4.2

## 02 - Upgrade 4.2 to 4.2
Verify de compability mode
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { getParameter: 1, featureCompatibilityVersion: 1 } )'
```
chage to mongo 4.0
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "4.2" } )'

```

## 03 - Upgrade 4.0 to 4.2
backup the database: 

backup the database with "mmapv1"  storage
```bash
 mongodump --port 27007 --out /backup
```


## 04 - Upgrade 4.0 to 4.2
Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```

## 05 - Upgrade 4.0 to 4.2
enable wiredtiger storage mode  /etc/mongo.conf
```bash
  wiredTiger:
    engineConfig:
     cacheSizeGB: 12
```

############################ STEP 6 ##############################

## 01 - Upgrade 4.2 to 4.4

Stop de mongod daemon, and edit the config file /etc/yum.repos.d/mongo.conf and change on BASEURL line de version 4.2 to 4.4

## 02 - Upgrade 4.2 to 4.4

Verify de compability mode
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { getParameter: 1, featureCompatibilityVersion: 1 } )'
```
chage to mongo 4.2
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "4.2" } )'
```

## 03 - Upgrade 4.2 to 4.4

Clean the repository cache, and update the mongo packages
```bash
yum clean all
yum repolist
yum update mongo*
systemctl daemon-reload
systemctl start mongod
```

## 04 - Upgrade 4.2 to 4.4
chage to mongo 4.4
```bash
 mongo --port 27007 --quiet --eval 'db.adminCommand( { setFeatureCompatibilityVersion: "4.4" } )'
```

############################ STEP 7 ##############################


```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```
```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```

```bash

```
