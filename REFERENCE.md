# Reference

<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

### Classes

#### Public Classes

* [`oxidized`](#oxidized): Manage Oxidized

#### Private Classes

* `oxidized::config`: Manage oxidized configs
* `oxidized::install`: Manage oxidized packages
* `oxidized::repo`: Manage repos needed for oxidized
* `oxidized::service`: Manage oxidized service
* `oxidized::user`: Manage Oxidzed user

### Defined types

* [`oxidized::model`](#oxidized--model): Manage oxidized models

## Classes

### <a name="oxidized"></a>`oxidized`

Manage Oxidized

#### Examples

##### 

```puppet
include oxidized
```

#### Parameters

The following parameters are available in the `oxidized` class:

* [`manage_repo`](#-oxidized--manage_repo)
* [`ruby_dependencies`](#-oxidized--ruby_dependencies)
* [`install_dependencies`](#-oxidized--install_dependencies)
* [`with_web`](#-oxidized--with_web)
* [`package_ensure`](#-oxidized--package_ensure)
* [`script_package_ensure`](#-oxidized--script_package_ensure)
* [`web_package_ensure`](#-oxidized--web_package_ensure)
* [`rugged_version`](#-oxidized--rugged_version)
* [`user`](#-oxidized--user)
* [`user_group`](#-oxidized--user_group)
* [`user_uid`](#-oxidized--user_uid)
* [`user_group_gid`](#-oxidized--user_group_gid)
* [`user_home`](#-oxidized--user_home)
* [`user_home_mode`](#-oxidized--user_home_mode)
* [`config`](#-oxidized--config)
* [`config_mode`](#-oxidized--config_mode)
* [`source_type`](#-oxidized--source_type)
* [`devices`](#-oxidized--devices)
* [`devices_map`](#-oxidized--devices_map)
* [`devices_vars_map`](#-oxidized--devices_vars_map)
* [`with_service`](#-oxidized--with_service)
* [`service_start`](#-oxidized--service_start)
* [`show_diff`](#-oxidized--show_diff)
* [`log`](#-oxidized--log)
* [`log_mode`](#-oxidized--log_mode)
* [`models`](#-oxidized--models)

##### <a name="-oxidized--manage_repo"></a>`manage_repo`

Data type: `Boolean`

Sets if repos needed for oxidize are managed.

Default value: `true`

##### <a name="-oxidized--ruby_dependencies"></a>`ruby_dependencies`

Data type: `Array`

Ruby dependencies

Default value: `[]`

##### <a name="-oxidized--install_dependencies"></a>`install_dependencies`

Data type: `Array`

Additional install dependencies

Default value: `[]`

##### <a name="-oxidized--with_web"></a>`with_web`

Data type: `Boolean`

Sets if the oxidized web should be installed and configured

Default value: `false`

##### <a name="-oxidized--package_ensure"></a>`package_ensure`

Data type: `String`

Ensure value for main oxidized package

Default value: `'installed'`

##### <a name="-oxidized--script_package_ensure"></a>`script_package_ensure`

Data type: `String`

Ensure value for oxidized-script package

Default value: `'installed'`

##### <a name="-oxidized--web_package_ensure"></a>`web_package_ensure`

Data type: `Optional[String]`

Ensure value for oxidized web package
Defaults to `installed` when `with_web` is `true`

Default value: `undef`

##### <a name="-oxidized--rugged_version"></a>`rugged_version`

Data type: `String`

Version of rugged to install with SSH support

Default value: `'1.6.3'`

##### <a name="-oxidized--user"></a>`user`

Data type: `String`

Oxidize user

Default value: `'oxidized'`

##### <a name="-oxidized--user_group"></a>`user_group`

Data type: `String`

Oxidize user's group

Default value: `'oxidized'`

##### <a name="-oxidized--user_uid"></a>`user_uid`

Data type: `Optional[Integer]`

Oxidize user's UID

Default value: `undef`

##### <a name="-oxidized--user_group_gid"></a>`user_group_gid`

Data type: `Optional[Integer]`

Oxidize user's group GID

Default value: `undef`

##### <a name="-oxidized--user_home"></a>`user_home`

Data type: `Stdlib::Absolutepath`

Oxidize user's home directory path

Default value: `'/home/oxidized'`

##### <a name="-oxidized--user_home_mode"></a>`user_home_mode`

Data type: `Stdlib::FileMode`

The permissions of oxidized user's home directory

Default value: `'0700'`

##### <a name="-oxidized--config"></a>`config`

Data type: `Hash`

Oxidize config hash

Default value: `{}`

##### <a name="-oxidized--config_mode"></a>`config_mode`

Data type: `Stdlib::FileMode`

Oxidized config file permission mode

Default value: `'0600'`

##### <a name="-oxidized--source_type"></a>`source_type`

Data type: `Enum['csv']`

Sets type of source to be used

Default value: `'csv'`

##### <a name="-oxidized--devices"></a>`devices`

Data type: `Array[Hash]`

Information about devices.
Only used when `source_type` is `csv`

Default value: `[]`

##### <a name="-oxidized--devices_map"></a>`devices_map`

Data type: `Hash[String, Integer]`

Map of CSV fields for devices
Only used when `source_type` is `csv`

Default value: `{ 'name' => 0, 'model' => 1 }`

##### <a name="-oxidized--devices_vars_map"></a>`devices_vars_map`

Data type: `Optional[Hash[String, Integer]]`

Set `vars_map` for device CSV configuration
Only used when `source_type` is `csv`

Default value: `undef`

##### <a name="-oxidized--with_service"></a>`with_service`

Data type: `Boolean`

Sets if the oxidized service should be installed and running

Default value: `false`

##### <a name="-oxidized--service_start"></a>`service_start`

Data type: `String`

The command to use to start oxidized service

Default value: `'/usr/local/bin/oxidized'`

##### <a name="-oxidized--show_diff"></a>`show_diff`

Data type: `Boolean`

Boolean that sets show_diff property for files

Default value: `true`

##### <a name="-oxidized--log"></a>`log`

Data type: `Optional[String]`

Path to oxidized log file

Default value: `undef`

##### <a name="-oxidized--log_mode"></a>`log_mode`

Data type: `Stdlib::FileMode`

The permissions of oxidized log file

Default value: `'0644'`

##### <a name="-oxidized--models"></a>`models`

Data type: `Hash`

Hash of models passed to oxidized::model

Default value: `{}`

## Defined types

### <a name="oxidized--model"></a>`oxidized::model`

Manage oxidized models

#### Parameters

The following parameters are available in the `oxidized::model` defined type:

* [`source`](#-oxidized--model--source)

##### <a name="-oxidized--model--source"></a>`source`

Data type: `String`

Source of model

