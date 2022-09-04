**mongodb_shard_cluster**
**start config servers**
sudo mongod --config "/var/mongodb/cfgsvr1/csrs.conf"
sudo mongod --config "/var/mongodb/cfgsvr2/csrs.conf"
sudo mongod --config "/var/mongodb/cfgsvr3/csrs.conf"

**Start shard servers**
sudo mongod --config "/var/mongodb/shardsvr1/shard.conf"
sudo mongod --config "/var/mongodb/shardsvr2/shard.conf"
sudo mongod --config "/var/mongodb/shardsvr3/shard.conf"

**start mongos / shard cluster**
sudo mongos --config "/var/mongodb/mongos/mongos.conf"


**connect to shard servers**
sudo mongosh "mongodb://<*username*>:<*password*>@localhost:26000"

**connect to config servers**
sudo mongosh "mongodb://<*username*>:<*password*>@localhost:26001/admin"
sudo mongosh "mongodb://localhost:26002"
sudo mongosh "mongodb://localhost:26003"

**connect to shard servers**
sudo mongosh "mongodb://<*username*>:<*password*>@localhost:27017/admin"
sudo mongosh "mongodb://localhost:27018"
sudo mongosh "mongodb://localhost:27019"
