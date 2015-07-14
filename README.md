## Sensu-Plugins-twemproxy

[ ![Build Status](https://travis-ci.org/sensu-plugins/sensu-plugins-twemproxy.svg?branch=master)](https://travis-ci.org/sensu-plugins/sensu-plugins-twemproxy)
[![Gem Version](https://badge.fury.io/rb/sensu-plugins-twemproxy.svg)](http://badge.fury.io/rb/sensu-plugins-twemproxy)
[![Code Climate](https://codeclimate.com/github/sensu-plugins/sensu-plugins-twemproxy/badges/gpa.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-twemproxy)
[![Test Coverage](https://codeclimate.com/github/sensu-plugins/sensu-plugins-twemproxy/badges/coverage.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-twemproxy)
[![Dependency Status](https://gemnasium.com/sensu-plugins/sensu-plugins-twemproxy.svg)](https://gemnasium.com/sensu-plugins/sensu-plugins-twemproxy)
[![Codeship Status for sensu-plugins/sensu-plugins-twemproxy](https://codeship.com/projects/145ac380-e2dc-0132-54f7-76e3d81118b5/status?branch=master)](https://codeship.com/projects/81584)

## Functionality

**metrics-twemproxy**

Acquire twemproxy metrics from its stats json output.

```json
{  
   "service":"nutcracker",
   "source":"twemproxy01",
   "version":"0.4.0",
   "uptime":3839769,
   "timestamp":1425500928,
   "total_connections":2936,
   "curr_connections":12,
   "backend":{  
      "client_eof":676,
      "client_err":2224,
      "client_connections":0,
      "server_ejects":0,
      "forward_error":0,
      "fragments":0,
      "shard01":{  
         "server_eof":3,
         "server_err":0,
         "server_timedout":0,
         "server_connections":1,
         "server_ejected_at":0,
         "requests":19145560,
         "request_bytes":6137042859,
         "responses":19145557,
         "response_bytes":584731733,
         "in_queue":0,
         "in_queue_bytes":0,
         "out_queue":0,
         "out_queue_bytes":0
      },
  }
}
```

## Files
 * bin/metrics-twemproxy.rb

## Usage

```
/etc/sensu/plugins/twemproxy-graphite.rb -p 22222 -s twemproxy01.twemproxy
```

```
twemproxy01.twemproxy.client_eof 676 1425501320
twemproxy01.twemproxy.client_err 2224 1425501320
twemproxy01.twemproxy.client_connections 0 1425501320
twemproxy01.twemproxy.server_ejects 0 1425501320
twemproxy01.twemproxy.forward_error 0 1425501320
twemproxy01.twemproxy.fragments 0 1425501320
twemproxy01.twemproxy.shard01.server_eof 3 1425501320
twemproxy01.twemproxy.shard01.server_err 0 1425501320
twemproxy01.twemproxy.shard01.server_timedout 0 1425501320
twemproxy01.twemproxy.shard01.server_connections 1 1425501320
twemproxy01.twemproxy.shard01.server_ejected_at 0 1425501320
twemproxy01.twemproxy.shard01.requests 19145560 1425501320
twemproxy01.twemproxy.shard01.request_bytes 6137042859 1425501320
twemproxy01.twemproxy.shard01.responses 19145557 1425501320
twemproxy01.twemproxy.shard01.response_bytes 584731733 1425501320
twemproxy01.twemproxy.shard01.in_queue 0 1425501320
twemproxy01.twemproxy.shard01.in_queue_bytes 0 1425501320
twemproxy01.twemproxy.shard01.out_queue 0 1425501320
twemproxy01.twemproxy.shard01.out_queue_bytes 0 1425501320
```

## Installation

[Installation and Setup](https://github.com/sensu-plugins/documentation/blob/master/user_docs/installation_instructions.md)

## Notes
