<h3>mongodb_shard_cluster</h3><br>

<b>start config servers</b><br>
<code>sudo mongod --config "/var/mongodb/cfgsvr1/csrs.conf"</code><br>
<code>sudo mongod --config "/var/mongodb/cfgsvr2/csrs.conf"</code><br>
<code>sudo mongod --config "/var/mongodb/cfgsvr3/csrs.conf"</code><br>

<b>start shard servers</b><br>
<code>sudo mongod --config "/var/mongodb/shardsvr1/shard.conf"</code><br>
<code>sudo mongod --config "/var/mongodb/shardsvr2/shard.conf"</code><br>
<code>sudo mongod --config "/var/mongodb/shardsvr3/shard.conf"</code><br>

<b>start mongos / shard cluster</b><br>
<code>sudo mongos --config "/var/mongodb/mongos/mongos.conf"</code><br>


<b>connect to shard servers</b><br>
<code>sudo mongosh "mongodb://username:password@localhost:26000"</code><br>

<b>connect to config servers</b><br>
<code>sudo mongosh "mongodb://username:password@localhost:26001/admin"</code><br>
<code>sudo mongosh "mongodb://localhost:26002"</code><br>
<code>sudo mongosh "mongodb://localhost:26003"</code><br>

<b>connect to shard servers</b><br>
<code>sudo mongosh "mongodb://username:password</t>@localhost:27017/admin"</code><br>
<code>sudo mongosh "mongodb://localhost:27018"</code><br>
<code>sudo mongosh "mongodb://localhost:27019"</code>

<b>connect as authenticated user</b><br>
<code>sudo mongosh --host localhost --port 27017 --username user --password pass --authenticationDatabase admin</code>
