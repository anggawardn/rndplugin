# Kong Plugins "rndplugin"
### kong plugin to check request token authorization and forward request to filter payload(by security-matrix) written in lua

 to add the plugin:
```
curl -X POST http://kong:8001/services/{service-name}/plugins \
--data "name=rndplugin" \
--data "config.securityMatrixPath=http://securitymatrixhost:port/path/to/filter" \
--data "config.checkAuthPath=http://securitymatrixhost:port/path/to/check"
```
