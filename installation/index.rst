.. _installation_index:

Installation
############

Before you begin:
	- Check if your hardware is supported on the system :doc:`requirements
	  page </prerequisites>`.
	- Disconnect all storage devices except the one to be used as operating system drive. This way you
	  avoid an accidental install on a storage drive (which will be configured
	  after installation anyway).
	- Select an appropriate installation variant and strictly follow instructions.
	
Installation variants:
	The available installation variants have different prerequisites on required user skills, strength and weaknesses of approach.

- Recommended method for x86 architecture 
	* :doc:`Dedicated drive </installation/via_iso>`  This approach uses a completely pre-build ISO image based on Debian OS and installs |omv| to run from its own dedicated drive.
- Recommended method for SBCs and alternate installation for x86, starting with a hardware specific Debian OS image
	* :doc:`Debian Operating System </installation/on_debian>` - This installs Debian OS and |omv| to a storage device of choice like memory card, USB-connected storage, etc.

First time use:
	If you have a screen attached, KVM or IMPI console the login screen will
	display the current IP address assigned for the |webui|. Open your browser
	and type that IP address. The default |webui| login credential is
	``admin:openmediavault``, the ``root`` password is the one you set during
	installation or was preconfigured by the choosen Debian distribution (i.e. Raspberry Pi OS).


Note:
   |omv| will enable SSH access for the user ``root`` by default to be
   able to access a headless system in case of a broken installation or
   other maintenance situations. You can disable this behaviour in the
   ``Services | SSH`` page.

   To still get ``root`` access you need to create a non-privileged user
   and add them to the ``ssh`` and ``sudo`` groups. After that you can
   SSH into the system with this non-privileged user and run ``sudo su``.
