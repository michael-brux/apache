## Main configuration file
Main configuration file and document root in different distributions:

| System | ServerRoot |Configuration | DocumentRoot |
|--------|----------|----------|---------|
| Apache default | /usr/local/apache | conf/httpd.conf | /usr/local/apache/htdocs
| Debian, Ubuntu  | /etc/apache2 | apache2.conf    | /var/www/html/    |
| Fedora, Red Hat | /etc/httpd | conf/httpd.conf | /var/www/html/    |
| Free BSD        | /usr/local | etc/apache24/httpd.conf | /usr/local/www/apache24/data    |

Find main configuration file from command line:

```
# default (incl Red Hat, Fedora, Free BSD)
httpd -V | grep SERVER_CONFIG_FILE
# for debian, ubuntu
apache2 -V | grep SERVER_CONFIG_FILE
```

[DocumentRoot Directive](https://httpd.apache.org/docs/2.4/mod/core.html#documentroot)

See e.g. [Fedora Documentation](https://docs.fedoraproject.org/en-US/quick-docs/getting-started-with-apache-http-server/#_configuring_apache_httpd) or
[Ubuntu Documentation](https://ubuntu.com/server/docs/how-to-configure-apache2-settings)

[Apache default configuration](https://github.com/apache/httpd/blob/trunk/docs/conf/httpd.conf.in)

[Debian default configuration](https://sources.debian.org/src/apache2/2.4.62-6/debian/config-dir/apache2.conf.in/)

[Fedora default configuration](https://src.fedoraproject.org/rpms/httpd/blob/rawhide/f/httpd.conf)
