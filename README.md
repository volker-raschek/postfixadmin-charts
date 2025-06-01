# postfixadmin-charts

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/volker-raschek)](https://artifacthub.io/packages/search?repo=volker-raschek)

This is an inofficial helm chart for
[postfixadmin](https://github.com/postfixadmin/postfixadmin), because the
maintainer does not provide currently an official one.

This helm chart can be found on [artifacthub.io](https://artifacthub.io/) and
can be installed via helm.

```bash
helm repo add volker.raschek https://charts.cryptic.systems/volker.raschek
helm install postfixadmin volker.raschek/postfixadmin
```

## Customization

The list below is only an excerpt of the listed environment variables from the
used [container image](https://github.com/volker-raschek/postfixadmin-docker).

The environment variables are composed on the key of the PHP configuration with
the prefix `POSTFIXADMIN_`. You can take an example
[configuration](https://github.com/postfixadmin/postfixadmin/blob/master/config.inc.php)
from the upstream project.

| value                                        | reference                                                                                             |
| ------------------------------------------- | -----------------------------------------------------------------------------------------------       |
| `.config.POSTFIXADMIN_ADMIN_EMAIL`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_admin_email)       |
| `.config.POSTFIXADMIN_ADMIN_SMTP_PASSWORD`  | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_smtp_password)     |
| `.config.POSTFIXADMIN_ADMIN_NAME`           | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_admin_name)        |
| `.config.POSTFIXADMIN_DATABASE_TYPE`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_type)     |
| `.config.POSTFIXADMIN_DATABASE_USER`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_user)     |
| `.config.POSTFIXADMIN_DATABASE_PASSWORD`    | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_password) |
| `.config.POSTFIXADMIN_DATABASE_HOST`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_host)     |
| `.config.POSTFIXADMIN_DATABASE_PORT`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_port)     |
| `.config.POSTFIXADMIN_DATABASE_NAME`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_name)     |
| `.config.POSTFIXADMIN_DEFAULT_LANGUAGE`     | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_default_language)  |
| `.config.POSTFIXADMIN_DATABASE_USE_SSL`     | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_use_ssl)  |
| `.config.POSTFIXADMIN_DATABASE_KEY`         | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_key)      |
| `.config.POSTFIXADMIN_DATABASE_CERT`        | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_cert)     |
| `.config.POSTFIXADMIN_DATABASE_CA`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_ca)       |
| `.config.POSTFIXADMIN_DATABASE_PREFIX`      | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_database_prefix)   |
| `.config.POSTFIXADMIN_ENCRYPT`              | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_encrypt)           |
| `.config.POSTFIXADMIN_SMTP_SERVER`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_smtp_server)       |
| `.config.POSTFIXADMIN_SMTP_PORT`            | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_smtp_port)         |
| `.config.POSTFIXADMIN_SMTP_CLIENT`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_smtp_client)       |
| `.config.POSTFIXADMIN_SHOW_FOOTER_TEXT`     | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_show_footer_text)  |
| `.config.POSTFIXADMIN_FOOTER_TEXT`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_footer_text)       |
| `.config.POSTFIXADMIN_FOOTER_LINK`          | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_footer_link)       |
| `.config.POSTFIXADMIN_FETCHMAIL`            | [Documentation](https://github.com/volker-raschek/postfixadmin-docker#postfixadmin_fetchmail)         |

## Postfixadmin-Fetchmail

As addon can be additionally the helm chart
`volker.raschek/postfixadmi-fetchmail` installed. The the `fetchmail.pl` script
has been packaged into an own container to support among others non-kubernetes
based postfixadmin instances with the `fetchmail.pl` script on kubernetes basis.

More about the addon is documented
[here](https://github.com/volker-raschek/postfixadmin-fetchmail-charts).
