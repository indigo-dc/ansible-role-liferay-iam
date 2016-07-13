Ansible Role for Liferay IAM modules
====================================

The role installs IAM module plug-ins in a running Liferay 7.0.x instance.

Requirements
------------

NONE

Role Variables
--------------

Defaults variable for the role are the references for the module to install and the
repository where these are made available. These include:

| **Variable**        |                   **Values**                               |
|---------------------|------------------------------------------------------------|
|  *modules*          | com.liferay.login.authentication.iam.web                   |
|                     | com.liferay.portal.security.sso.iam.api                    |
|                     | com.liferay.portal.security.sso.iam                        |
|                     | com.liferay.portal.security.sso.iam.service                |
|                     | com.liferay.portal.settings.authentication.iam.web         |
|                     |                                                            |
|  *module_version*   | 1.0.0                                                      |
|                     |                                                            |
|  *package*          | LiferayIAM-binary.tgz                                      |
|                     |                                                            |
|  *release*          | v1.0-rc.1                                                  |
|                     |                                                            |
|  *repository*       | https://github.com/indigo-dc/LiferayIAM/releases/download/ |

Two variable must be configured to execute the playbook and they are:

* *liferay_deploy_dir*: containing the path to the Liferay deploy directory
* *liferay_osgi_dir*: containing the path to the osgi directory of Liferay modules

Dependencies
------------

NONE

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: fmarco76.LiferayIAM, liferay_deploy_dir: /some_path/deploy, liferay_osgi_dir: /some_other_path/osgi }

License
-------

Apache v. 2.0

Author Information
------------------

Italian National Institute for Nuclear Physics (INFN)
Marco Fargetta (marco.fargetta@ct.infn.it)
