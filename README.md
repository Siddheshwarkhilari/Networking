# Networking
# Proxy
1. Forward Proxy:
     1] Forward proxy is an intermediary between client and the Internet(server).
     2] Forwards the requests to the internet by performing client IP masking and sending the request back to user
        using some security policies.
     3] Squid proxy is example of Forward proxy.
     4] Here request is originated from client in its private network (Intranet).
2. Reverse Proxy:
     1] Reverese proxy is intermediary lying between internet and intranet.
     2] They performs the task of sheilding the backend servers , providing security and load balancing across them.
     3] Nginx can be used as reverse proxy.
     4] Here request is originated from client in the public network (Internet).


# SSL/TLS termination
     1] It is process of decrypting SSL/TLS encrypted traffic before passing it to backend server. It is basically done by 
     2] Load balancer, reverse proxy, or edge server and forwards unencrypted traffic to backend servers. These components 
        are used to decrease the load of High CPU usageon backend application servers, which slows the reponse time.
               # TLS handshsake
                    # TLS handshake is process that establishes secure communication channel between a client(web browser) and web server.
                    # The handshake ensures authentication, encryption and data integrity before any actual data is exchanged.
                    1. The client (e.g., browser) sends a ClientHello message to the server, This message includes
                         Supported TLS versions
                         A list of supported cipher suites 
                         A random value (client random) used for key generation
                    2. The server responds with a ServerHello message.This message includes
                         selected TLS version
                         chosen cipher suite
                         A random value (server random)
                         server's digital certificate (signed by a Certificate Authority (CA)).
                    3. The server presents an SSL/TLS certificate issued by a Certificate Authority (CA). This certificate contains
                         The domain name 
                         The public key of server
                         The CA's signature.
                    4. Verification process takes plavce in which 
                         Client validates the certificate by checking whether CA is trusted
                         Whether the certificate is expired or revoked
                         Whether domain name matche the certificate
                    5.  IF certificate is invalid , handshake fails
                    6. Key exchange takes place if successfull and then server securely establish shared session key for further communication 
     
