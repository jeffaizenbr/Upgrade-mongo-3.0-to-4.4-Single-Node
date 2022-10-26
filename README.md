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

```bash

```

```bash

```
