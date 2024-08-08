Low level design
+-------------------------+                     +-------------------------+
|                         |                     |                         |
|      React.js UI        |                     |   Node.js & Express.js  |
|-------------------------|                     |        Backend          |
| - Chat List             |<----API Request---->|-------------------------|
| - Chat Window           |                     | - /api/users            |
| - Contact List          |                     | - /api/chats            |
| - User Profile          |                     | - /api/messages         |
|                         |                     | - /api/contacts         |
+-------------------------+                     | - /api/auth             |
                                                 | - JWT & Encryption     |
                                                 | - Real-Time: Socket.io |
                                                 +-----------+-------------+
                                                             |
                                                             | CRUD
                                                             v
                                               +-------------+-------------+
                                               |                           |
                                               |         MongoDB           |
                                               |---------------------------|
                                               | - Users                   |
                                               | - Chats                   |
                                               | - Messages                |
                                               | - Contacts                |
                                               |                           |
                                               +---------------------------+
                                                 ^            ^             ^
                                                 |            |             |
                +------------------+             |            |             |
                |                  |             |            |             |
                |    |<------------+            |             |
                      |                          |             |
                +------------------+                          |             |
                                                               |             |
                +------------------+                           |             |
                |                  |                           |             |
                |     |<--------------------------+             |
                | )                                      |
                |                  |                                         |
                +------------------+                                         |
                                                                              |
                +------------------+                                         |
                |                  |                                         |
                |    Socket.io     |<----------------------------------------+
                |  Real-Time Comm. |
                +------------------+