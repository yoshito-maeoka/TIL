# Symfony v3.4.*
## 500 Error because of 'Failed opening'

got error like something:
```
Got error 'PHP message: PHP Fatal error:  require(): Failed opening required '/var/www/ProjectX/var/cache/dev/doctrine/orm/Proxies/__CG__EntityXX.php' (include_path='.:/usr/share/php') in /var/www/ProjectX/vendor/doctrine/common/lib/Doctrine/Common/Proxy/AbstractProxyFactory.php on line 206
```

then erase only app* files like that:
```
$ rm -rf var/cache/dev/app*
```
