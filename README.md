![](https://github.com/Kaisa-Marysia/sslchecker/blob/main/sslchecker.png?raw=true)
# sslchecker
**sslcheker** is wrapper written in bash for openssl and nmap, which checks the ssl certs and used TLS ciphers of a host. This tool checks when a certificate has been valid and when it expires. Also you get the information about the CA, for which domains the SSL certificate is valid and the IP adresse and PTR Record of the host. 

## Depends
You need 'nmap', 'openssl' and 'xmlstarlet'.

## Install
Copy this repository <br>
```git clone https://github.com/Kaisa-Marysia/sslchecker``` <br>
or download the script file with wget <br>
```wget https://raw.githubusercontent.com/Kaisa-Marysia/sslchecker/main/sslchecker``` <br>
or with curl <br>
```curl https://raw.githubusercontent.com/Kaisa-Marysia/sslchecker/main/sslchecker -o ./sslchecker```.  <br>

If you want and trust me, you may also download the file into ```/usr/bin/``` so you can run it global <br>
```sudo curl https://raw.githubusercontent.com/Kaisa-Marysia/sslchecker/main/sslchecker -o /usr/bin/sslchecker``` and make it executable ```sudo chmod +x /usr/bin/sslchecker``` <br>
In this case you can update the script file by running `sslchecker` with the `-u` option.

## Usage

```
Usage: sslchecker [options]
Options:
  -f    local file
  -h    remote host
  -p    custome port
  -c    list ciphers
  -u    update sslchecker
  -v    show version
  --help show this help page
```
### SSL Certificates
The local file option give you an overview about certificate file. Just use ```sslchecker -f [/path/to/file]``` <br>
With the `-h [host]` option you can check the ssl certificate of a remote host, like github.com. 

![](https://github.com/Kaisa-Marysia/sslchecker/blob/main/screenshot.png?raw=true)

If your application runs on another port number, you may set the port with the `-p [port]` option. <br>
```sslchecker -h github.com -p 8443``` <br>

### TLS Ciphers
To get a list of used ciphers of the use the `-c [host]` option.

![](https://github.com/Kaisa-Marysia/sslchecker/blob/main/screenshot2.png?raw=true)

### Update
The update option `-u` will download the script file from github into `/usr/bin/`. If you don't drop the script file into this path, the update option will. You need root priviliges for this.
