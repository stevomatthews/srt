# SRT Feature Matrix

Live streaming over public networks

## Connectivity

| Feature                     | Version | Status       | Description/Comments                   |
| --------------------------- | ------- | ------------ | -------------------------------------- |
| Firewall traversal          | 1.X.X   | Done         |                                        |
| NAT traversal               | 1.X.X   |              | To do?: RFC-8445 ICE                   |
| Connection migration        | 1.X.X   |              | ?                                      |
| Network switching           | 1.X.X   |              | ?                                      |
| Connection rejection reason | 1.X.X   |              | !                                      |




## Access Control

| Feature                     | Version | Status       | Description/Comments                   |
| --------------------------- | ------- | ------------ | -------------------------------------- |
| User authentication         | 1.X.X   | Done         | User name is not encrypted             |
| Resource request            | 1.X.X   | Done         | Not encrypted                          |
| Stream definition           | 1.X.X   |              | To do: RFC-4566: SDP                   |
| <img width=150px height=1px/> |         | <img width=60px height=1px/> | <img width=500px height=1px/> |



## Security

| Feature                     | Version | Status       | Description/Comments                   |
| --------------------------- | ------- | ------------ | -------------------------------------- |
| Encryption                  | 1.X.X   | Done         | AES-CTR 128/192/256                    |
| Pre-shared password + PBKD2 | 1.X.X   | Done         | TBD                                    |
| TLS                         | 1.X.X   |              | Could be added?                        |
| DTLS                        | 1.X.X   |              | Potentially works                      |
| <img width=150px height=1px/> |         | <img width=60px height=1px/> | <img width=500px height=1px/> |


## Content Delivery

| Feature                     | Version | Status       | Description/Comments                   |
| --------------------------- | ------- | ------------ | -------------------------------------- |
| Content agnostic            | 1.X.X   | Done         | MPEG-TS, RTP, ES ...                   |
| Stream multiplexing         | 1.X.X   | Done         |                                        |
| UDP unicast (bidirectional) | 1.X.X   | Done         |                                        |
| UDP multicast               | 1.X.X   |              | To do?                                 |
| Loss recovery (ARQ)         | 1.X.X   | Done         | ACK, NAK, retransmit                   |
| Loss recovery (FEC)         | 1.4.0   | Done         |                                        |
| Loss recovery (Bonding)     | 1.5.0   | In progress  | Connection bonding: broadcast          |
| Packet reordering/jitter    | 1.X.X   | Done         | TBD                                    |
| Varying latency (RTT)       | 1.X.X   | Done         | Ability to handle                      |
| Too Late Packet Drop (RT)   | 1.X.X   | Done         | Real-time                              |
| Congestion control          | 1.X.X   | Done         | To be improved                         |
| Flow control                | 1.X.X   | Done         | To be improved                         |
| Network friendliness        | 1.X.X   | Done         | To be improved                         |
| <img width=150px height=1px/> |         | <img width=60px height=1px/> | <img width=500px height=1px/> |



## Connection Bonding

| Feature                     | Version | Status       | Description/Comments                   |
| --------------------------- | ------- | ------------ | -------------------------------------- |
| Data duplication            | 1.5.0   | In progress  | Broadcast                              |
| Backup link                 | 1.5.0   | In progress  |                                        |
| Smart link utilization      | 1.5.0   | In progress  | Balancing                              |
| <img width=150px height=1px/> |         | <img width=60px height=1px/> | <img width=500px height=1px/> |











