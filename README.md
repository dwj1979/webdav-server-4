# WebDAV Server
A simple webdav server with basic auth using Golang.

## Files and Folders
* keygen : OpenSSL to create certificates
* pem : Cert files in here
* storage : Service storage
* win_conn_example : Batch files for connection
* server.go : WebDAV server

## Create certificates
Via HTTPS, you should create or have your own certificates.
* Create and copy certs as below.
```
cd keygen
keygen.cmd

move *.pem ../pem/
```

## Open in MS-Windows Explorer
* If you use ```RMB > Map Network Drive...``` in explorer window, You should enable ```Connect using different credentials```.
* Via HTTP, you should modify set in registry as below.
```
regedit > HKLM\SYSTEM\CurrentControlSet\Services\WebClient\Parameters
BasicAuthLevel to 2
```
* Via HTTPS
  * See files in win_conn_example

## Run or Open in Other OS
I hope that you can do it yourself well. ^_^

## License
Public domain. Use at your own risk.

## Reference
* https://gist.github.com/staaldraad/d835126cd46969330a8fdadba62b9b69
* https://golang.org/pkg/net/http/#Request.BasicAuth
