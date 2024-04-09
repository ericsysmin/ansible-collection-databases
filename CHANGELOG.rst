==================================
Ericsysmin.Databases Release Notes
==================================

.. contents:: Topics


v1.1.0
======

Release Summary
---------------

Update to the ericsysmin.database collection to meet new ansible-lint requirements and updates to the molecule testing on GitHub Actions.

Major Changes
-------------

- mongodb Role - Added support for Ubuntu 22.04
- pgadmin4 Role - Added support for Debian 11
- pgadmin4 Role - Added support for Ubuntu 22.04
- postgresql Role - Added support for Debian 11

Removed Features (previously deprecated)
----------------------------------------

- mongodb role - Removed support for Debian 10
- mongodb role - Removed support for Ubuntu 18.04
- postgresql role - Removed support for Debian 10

New Roles
---------

- ericsysmin.databases.mongodb - Role to configure MongoDB and install MongoDB CLI
- ericsysmin.databases.pgadmin4 - Role to configure PgAdmin4 application and server.
- ericsysmin.databases.postgresql - Role to install Postgresql database.
