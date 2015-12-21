# Ansible Role: Nginx

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-php5-fpm.svg)](https://travis-ci.org/tschifftner/ansible-role-php5-fpm)

Installs php5-fpm on Debian/Ubuntu linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

### php.ini variables
```
php_expose_php: "On"
php_memory_limit: "256M"
php_max_execution_time: "60"
php_max_input_time: "60"
php_max_input_vars: "1000"
php_realpath_cache_size: "32K"
php_realpath_cache_ttl: "120"
php_upload_max_filesize: "64M"
php_post_max_size: "32M"
php_date_timezone: "Europe/Berlin"
php_sendmail_path: "/usr/sbin/sendmail -t -i"
php_short_open_tag: false
php_error_reporting: "E_ALL & ~E_DEPRECATED & ~E_STRICT"
php_display_errors: "Off"
php_display_startup_errors: "Off"
```

### APCu variables
```
php_apc_enabled_in_ini: true
apc_enabled: "1"
apc_shm_size: "256M"
apc_ttl: "7200"
apc_user_ttl: "7200"
apc_gc_ttl: "3600"
apc_cache_by_default: "1"
apc_filters: ""
apc_file_update_protection: "2"
apc_enable_cli: "0"
apc_max_file_size: "1M"
apc_stat: "1"
apc_include_once_override: "0"
```

### Opcache variables
```
php_opcache_enabled_in_ini: true
php_opcache_enable: "1"
php_opcache_enable_cli: "0"
php_opcache_memory_consumption: "96"
php_opcache_interned_strings_buffer: "16"
php_opcache_max_accelerated_files: "4096"
php_opcache_max_wasted_percentage: "5"
php_opcache_validate_timestamps: "1"
php_opcache_revalidate_freq: "2"
php_opcache_max_file_size: "0"
```

## Dependencies

None.

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.ansible-role-php5-fpm }

## License

MIT / BSD

## Author Information

 - Tobias Schifftner, @tschifftner