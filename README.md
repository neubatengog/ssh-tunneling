ssh-tunneling
=============

```
SYNOPSIS :
    tunnel.bash
        --help
        --configure
        --local-port  <LOCAL_PORT>
        --remote-port <REMOTE_PORT>
        --local-to-remote
        --remote-to-local
        --remote-user <REMOTE_USER>
        --remote-host <REMOTE_HOST>

DESCRIPTION :
    --help               Help page
    --configure          Config remote server to support forwarding (optional)
                         This option will require arguments '--remote-user' and '--remote-host'
    --local-port         Local port number (require)
    --remote-port        Remote port number (require)
    --local-to-remote    Forward request from local machine to remote machine
                         Either '--local-to-remote' or '--remote-to-local' argument must be specified
    --remote-to-local    Forward request from remote machine to local machine (require)
                         Either '--local-to-remote' or '--remote-to-local' argument must be specified
    --remote-user        Remote user (require)
    --remote-host        Remote host (require)

EXAMPLES :
    ./tunnel.bash --help
    ./tunnel.bash
        --configure
        --remote-user 'root'
        --remote-host 'my-server.com'
    ./tunnel.bash
        --local-port 8080
        --remote-port 9090
        --local-to-remote
        --remote-user 'root'
        --remote-host 'my-server.com'
    ./tunnel.bash
        --local-port 8080
        --remote-port 9090
        --remote-to-local
        --remote-user 'root'
        --remote-host 'my-server.com'
```
