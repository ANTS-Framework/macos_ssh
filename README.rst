macOS ssh
=========

Description
-----------
This role is used to enable remote login (SSH) for admins or for everyone. 

Usage
---------
By default, remote login will be enabled for members of the admin group only.

Set the value :code:`macos_ssh__ssh_access_everyone` to :code:`True` if you want to enable access for everyone.

To disalbe ssh login on the managed machine, set :code:`macos_ssh__ssh_enabled` to :code:`False`.

Use group\_vars to manage these variables.
