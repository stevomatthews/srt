# SRT Feature Matrix

Live streaming over public networks

| Feature                       | Version | Status                       | Description/Comments                   |
| ----------------------------- | ------- | ---------------------------- | -------------------------------------- |
|                               |         |                              |                                        |
| <h3>Connectivity</h3>         |         |                              |                                        |
| Firewall traversal            | 1.X.X   | Done                         |                                        |
| NAT traversal                 | 1.X.X   |                              | To do?: RFC-8445 ICE                   |
| Connection migration          | 1.X.X   |                              | ?                                      |
| Network switching             | 1.X.X   |                              | ?                                      |
| Connection rejection reason   | 1.X.X   |                              | !                                      |
|                               |         |                              |                                        |
| <h3>Access Control</h3>       |         |                              |                                        |
| User authentication           | 1.X.X   | Done                         | User name is not encrypted             |
| Resource request              | 1.X.X   | Done                         | Not encrypted                          |
| Stream definition             | 1.X.X   |                              | To do: RFC-4566: SDP                   |
|                               |         |                              |                                        |
| <h3>Security</h3>             |         |                              |                                        |
| Encryption                    | 1.X.X   | Done                         | AES-CTR 128/192/256                    |
| Pre-shared password + PBKD2   | 1.X.X   | Done                         | TBD                                    |
| TLS                           | 1.X.X   |                              | Could be added?                        |
| DTLS                          | 1.X.X   |                              | Potentially works                      |
|                               |         |                              |                                        |
| <h3>Content Delivery</h3>     |         |                              |                                        |
| Content agnostic              | 1.X.X   | Done                         | MPEG-TS, RTP, ES ...                   |
| Stream multiplexing           | 1.X.X   | Done                         |                                        |
| UDP unicast (bidirectional)   | 1.X.X   | Done                         |                                        |
| UDP multicast                 | 1.X.X   |                              | To do?                                 |
| Loss recovery (ARQ)           | 1.X.X   | Done                         | ACK, NAK, retransmit                   |
| Loss recovery (FEC)           | 1.4.0   | Done                         |                                        |
| Loss recovery (Bonding)       | 1.5.0   | In progress                  | Connection bonding: broadcast          |
| Packet reordering/jitter      | 1.X.X   | Done                         | TBD                                    |
| Varying latency (RTT)         | 1.X.X   | Done                         | Ability to handle                      |
| Too Late Packet Drop (RT)     | 1.X.X   | Done                         | Real-time                              |
| Congestion control            | 1.X.X   | Done                         | To be improved                         |
| Flow control                  | 1.X.X   | Done                         | To be improved                         |
| Network friendliness          | 1.X.X   | Done                         | To be improved                         |
|                               |         |                              |                                        |
| <h3>Connection Bonding</h3>   |         |                              |                                        |
| Data duplication              | 1.5.0   | In progress                  | Broadcast                              |
| Backup link                   | 1.5.0   | In progress                  |                                        |
| Smart link utilization        | 1.5.0   | In progress                  | Balancing                              |
| <img width=150px height=1px/> |         | <img width=75px height=1px/> | <img width=425px height=1px/>          |











