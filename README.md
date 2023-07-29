```
██████╗░██████╗░░█████╗░░██████╗░░█████╗░███╗░░██╗
██╔══██╗██╔══██╗██╔══██╗██╔════╝░██╔══██╗████╗░██║
██║░░██║██████╔╝███████║██║░░██╗░██║░░██║██╔██╗██║
██║░░██║██╔══██╗██╔══██║██║░░╚██╗██║░░██║██║╚████║
██████╔╝██║░░██║██║░░██║╚██████╔╝╚█████╔╝██║░╚███║
╚═════╝░╚═╝░░╚═╝╚═╝░░╚═╝░╚═════╝░░╚════╝░╚═╝░░╚══╝
```
# DRAGON Rust port scanner tool

Scan all ports in one second, basically no missing
### Install
`cargo build --release`
`cargo run`

### Usage
`cargo run -- -i google.com -p1-65535`

``` 
DRAGON
Asynchronous Port Scanner written in rust 

FLAGS:
    -h, --help       Prints help information
    -u, --udp        Scanning with UDP
    -V, --version    Prints version information

OPTIONS:
    -c, --concurrency <concurrency>    Number of concurrent scans [default: 65535]
    -i, --ip <ip>                      Scanned IP address
    -f, --outfile <outfile>            Result output file address
    -p, --port <port>                  Port Range <port,port,port> or <port-port> [default:
                                       21,22,23,25,69,79,80,88,110,113,119,220,443,1433,1521,2082,2083,2086,2087,2095,2096,2077,2078,3306,3389,5432,6379,8080,9000,9001,9200,9300,11211,27017]
    -t, --timeout <timeout>            Timeout  Milliseconds [default: 800]
```

### speed
Amazing speed Not a single port is missed
``` 
ubuntu@ubuntu:~/$ cargo run -- -i youtube.com -p1-65535

██████╗░██████╗░░█████╗░░██████╗░░█████╗░███╗░░██╗
██╔══██╗██╔══██╗██╔══██╗██╔════╝░██╔══██╗████╗░██║
██║░░██║██████╔╝███████║██║░░██╗░██║░░██║██╔██╗██║
██║░░██║██╔══██╗██╔══██║██║░░╚██╗██║░░██║██║╚████║
██████╔╝██║░░██║██║░░██║╚██████╔╝╚█████╔╝██║░╚███║
╚═════╝░╚═╝░░╚═╝╚═╝░░╚═╝░╚═════╝░░╚════╝░╚═╝░░╚══╝

Dragon
Asynchronous Port Scanner written in rust


youtube.com:80
youtube.com:443
youtube.com:2000
youtube.com:5060

real    0m1.637s
user    0m1.196s
sys     0m1.672s
``` 