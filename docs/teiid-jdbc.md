## SocketProfile

The java.sql.DriverManager class uses this class to connect to Teiid Server.

![SocketProfile](img/SocketProfile.gif)

## SocketServerConnection

SocketServerConnection represents a client connection that maintains session state and allows for service fail over. Implements a sticky random selection policy.

![SocketServerConnection](img/SocketServerConnection.gif)

## SocketServerConnectionFactory

SocketServerConnectionFactory responsible for creating socket based connections. The common approach is object based and layered. Connections manage failover and identity. ServerInstances represent the service layer to a particular cluster member.  ObjectChannels abstract the underlying IO.

![SocketServerConnectionFactory](img/SocketServerConnectionFactory.gif)

## SocketServerInstance

Client view of a socket server connection that exposes remote services. On construction this class will create a channel and exchange a handshake. That handshake will establish a Cryptor to be used for secure traffic.

![SocketServerInstance](img/SocketServerInstance.gif)
