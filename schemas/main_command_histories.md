| id | created\_at | updated\_at | session\_id | job\_id | command | args |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | job\_id | command\_type | content |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | name | addr | type | port |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | host |
| :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | url | status | title | content\_type | body\_length |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | class\_c | count |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | host | port | scheme | username | password |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | finger | count |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | host | port | network | computer\_name | work\_group | is\_domain\_controllers | banner |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | host | port |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | url | status | title | content\_type | body\_length | server | fingers |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | host | port | scheme | banner | url |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | session\_id | task\_id | target | po\_c\_name |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | name | session\_id | start\_time | end\_time | current\_status | completed\_status | target | port | options | stat\_alive\_ip\_cnt | stat\_brute\_page\_cnt | stat\_class\_c\_cnt | stat\_crack\_auth\_cnt | stat\_finger\_cnt | stat\_net\_bios\_cnt | stat\_open\_addr\_cnt | stat\_page\_info\_cnt | stat\_service\_cnt | stat\_yaml\_poc\_cnt |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| id | created\_at | updated\_at | remote\_ip | internal\_ip | last\_date | last\_interval | status | listener\_name | listener\_id | os | user\_name | hostname | user\_guid | arch | process | p\_id | note |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| type | name | tbl\_name | rootpage | sql |
| :--- | :--- | :--- | :--- | :--- |
| table | sessions | sessions | 2 | CREATE TABLE \`sessions\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`remote\_ip\` text,\`internal\_ip\` text,\`last\_date\` datetime,\`last\_interval\` text,\`status\` text,\`listener\_name\` text,\`listener\_id\` text,\`os\` text,\`user\_name\` text,\`hostname\` text,\`user\_guid\` text,\`arch\` text,\`process\` text,\`p\_id\` integer,\`note\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_sessions\_1 | sessions | 3 | NULL |
| table | listeners | listeners | 4 | CREATE TABLE \`listeners\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`name\` text,\`addr\` text,\`type\` text,\`port\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_listeners\_1 | listeners | 5 | NULL |
| table | command\_histories | command\_histories | 6 | CREATE TABLE \`command\_histories\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`job\_id\` text,\`command\` text,\`args\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_command\_histories\_1 | command\_histories | 7 | NULL |
| table | command\_results | command\_results | 8 | CREATE TABLE \`command\_results\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`job\_id\` text,\`command\_type\` text,\`content\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_command\_results\_1 | command\_results | 9 | NULL |
| table | users | users | 10 | CREATE TABLE \`users\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`username\` text,\`password\` text,\`token\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_users\_1 | users | 11 | NULL |
| table | web\_deliveries | web\_deliveries | 12 | CREATE TABLE \`web\_deliveries\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`file\_name\` text,\`delivery\_id\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_web\_deliveries\_1 | web\_deliveries | 13 | NULL |
| table | scan\_tasks | scan\_tasks | 14 | CREATE TABLE \`scan\_tasks\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`name\` text,\`session\_id\` text,\`start\_time\` text,\`end\_time\` text,\`current\_status\` text,\`completed\_status\` text,\`target\` text,\`port\` text,\`options\` text,\`stat\_alive\_ip\_cnt\` integer,\`stat\_brute\_page\_cnt\` integer,\`stat\_class\_c\_cnt\` integer,\`stat\_crack\_auth\_cnt\` integer,\`stat\_finger\_cnt\` integer,\`stat\_net\_bios\_cnt\` integer,\`stat\_open\_addr\_cnt\` integer,\`stat\_page\_info\_cnt\` integer,\`stat\_service\_cnt\` integer,\`stat\_yaml\_poc\_cnt\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_tasks\_1 | scan\_tasks | 15 | NULL |
| table | scan\_task\_alive\_ips | scan\_task\_alive\_ips | 16 | CREATE TABLE \`scan\_task\_alive\_ips\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`host\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_alive\_ips\_1 | scan\_task\_alive\_ips | 17 | NULL |
| table | scan\_task\_open\_addrs | scan\_task\_open\_addrs | 18 | CREATE TABLE \`scan\_task\_open\_addrs\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`host\` text,\`port\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_open\_addrs\_1 | scan\_task\_open\_addrs | 19 | NULL |
| table | scan\_task\_net\_bios | scan\_task\_net\_bios | 20 | CREATE TABLE \`scan\_task\_net\_bios\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`host\` text,\`port\` integer,\`network\` text,\`computer\_name\` text,\`work\_group\` text,\`is\_domain\_controllers\` numeric,\`banner\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_net\_bios\_1 | scan\_task\_net\_bios | 21 | NULL |
| table | scan\_task\_services | scan\_task\_services | 22 | CREATE TABLE \`scan\_task\_services\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`host\` text,\`port\` integer,\`scheme\` text,\`banner\` text,\`url\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_services\_1 | scan\_task\_services | 23 | NULL |
| table | scan\_task\_page\_infos | scan\_task\_page\_infos | 24 | CREATE TABLE \`scan\_task\_page\_infos\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`url\` text,\`status\` integer,\`title\` text,\`content\_type\` text,\`body\_length\` integer,\`server\` text,\`fingers\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_page\_infos\_1 | scan\_task\_page\_infos | 25 | NULL |
| table | scan\_task\_crack\_auths | scan\_task\_crack\_auths | 27 | CREATE TABLE \`scan\_task\_crack\_auths\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`host\` text,\`port\` integer,\`scheme\` text,\`username\` text,\`password\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_crack\_auths\_1 | scan\_task\_crack\_auths | 28 | NULL |
| table | scan\_task\_brute\_pages | scan\_task\_brute\_pages | 30 | CREATE TABLE \`scan\_task\_brute\_pages\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`url\` text,\`status\` integer,\`title\` text,\`content\_type\` text,\`body\_length\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_brute\_pages\_1 | scan\_task\_brute\_pages | 31 | NULL |
| table | scan\_task\_yaml\_po\_cs | scan\_task\_yaml\_po\_cs | 32 | CREATE TABLE \`scan\_task\_yaml\_po\_cs\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`target\` text,\`po\_c\_name\` text,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_yaml\_po\_cs\_1 | scan\_task\_yaml\_po\_cs | 33 | NULL |
| table | scan\_task\_class\_c\_stats | scan\_task\_class\_c\_stats | 34 | CREATE TABLE \`scan\_task\_class\_c\_stats\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`class\_c\` text,\`count\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_class\_c\_stats\_1 | scan\_task\_class\_c\_stats | 35 | NULL |
| table | scan\_task\_finger\_stats | scan\_task\_finger\_stats | 36 | CREATE TABLE \`scan\_task\_finger\_stats\` \(\`id\` text,\`created\_at\` datetime,\`updated\_at\` datetime,\`session\_id\` text,\`task\_id\` text,\`finger\` text,\`count\` integer,PRIMARY KEY \(\`id\`\)\) |
| index | sqlite\_autoindex\_scan\_task\_finger\_stats\_1 | scan\_task\_finger\_stats | 37 | NULL |

| id | created\_at | updated\_at | username | password | token |
| :--- | :--- | :--- | :--- | :--- | :--- |
| cbodibh2871htb6r9r1g | 2022-08-08 17:36:46.7981343+08:00 | 2022-08-08 17:36:46.7981343+08:00 | admin | A313EB99A477A1085BDF70C581445399067A2F55B9D18C040C6A5E463FFE7D01 | h7e0rrtd |

| id | created\_at | updated\_at | file\_name | delivery\_id |
| :--- | :--- | :--- | :--- | :--- |
