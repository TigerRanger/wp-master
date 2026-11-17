# WP Master

A local WordPress development site running on WampServer.

## Local site

| Setting | Value |
| --- | --- |
| Site title | WP Master |
| Site URL | http://wp-masetr.nz |
| Dashboard | http://wp-masetr.nz/wp-admin/ |
| Project directory | `C:\wamp\www\wp-master` |
| WordPress | 7.1.4 |
| PHP | 8.3.20 |
| MySQL | 8.0.31 |

The hostname `wp-masetr.nz` uses the spelling configured for this project.

## Running locally

1. Start WampServer and ensure Apache and MySQL are running.
2. Open [WP Master](http://wp-masetr.nz).
3. Sign in to the [dashboard](http://wp-masetr.nz/wp-admin/) with your WordPress administrator credentials.

The WordPress administrator username is `admin`. The administrator password is not stored in this README.

## Database

The local database connection is configured in `wp-config.php`:

| Setting | Value |
| --- | --- |
| Host | `127.0.0.1` |
| Database | `wp-master` |
| Username | `root` |
| Password | Empty |
| Table prefix | `wp_` |

These database settings are for local development only.

## Virtual host

Apache serves this project from `C:\wamp\www\wp-master` using the virtual host `wp-masetr.nz`. The Windows hosts file contains:

```text
127.0.0.1 wp-masetr.nz
::1 wp-masetr.nz
```

The hosts file is located at `C:\Windows\System32\drivers\etc\hosts`. Restart Apache after changing its virtual-host configuration.

## Development

- Place custom themes in `wp-content/themes/`.
- Place custom plugins in `wp-content/plugins/`.
- Avoid editing WordPress core files; updates can overwrite those changes.
- Back up the database and `wp-content/` before updates or migrations.
- ZIP archives are excluded by the `*.zip` rule in `.gitignore`.

## Site settings

- Timezone: `Asia/Dhaka`.
- Search engine visibility: indexing discouraged for this local installation.

## Resources

- [WordPress documentation](https://wordpress.org/documentation/)
- [WordPress developer resources](https://developer.wordpress.org/)
