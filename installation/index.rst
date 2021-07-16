.. _installation_index:

Installation
############

Before you begin:
	- Check if your hardware is supported on the system :doc:`requirements
	  page </prerequisites>`.
	- Disconnect all disk devices except the one for the system drive. This way you
	  avoid an accidental install on a storage drive (which will be configured
	  after installation anyway).
	- Select an appropriate installation variant and strictly follow instructions.
	
Installation variants:
	The available installation variants have different prerequisites on required user skills, strength and weaknesses of approach.

- Recommended method for x86 architecture - used as simplest starting point
	* :doc:`Dedicated drive </installation/via_iso>`  This approach uses an ISO image and installs |omv| to run from its own dedicated drive.
- Recommended method for SBCs and low cost x86 architecture computers - used as simple starting point
	* :doc:`SD card </installation/via_image>` - This installs |omv| to run from a SD card.
	* :doc:`USB flash drive </installation/on_usb>` - This installs |omv| to run from a USB flash drive.
	
- Advanced method - used by experienced Linux users with complex requirements	
	* :doc:`Debian Operating System </installation/on_debian>` - This installs |omv| to a customized storage device setup
	* `Debian Operating System via debootstrap <https://forum.openmediavault.org/index.php/Thread/12070-GUIDE-DEBOOTSTRAP-Installing-Debian-into-a-folder-in-a-running-system/>`_. 
	Note: Use this approach as a last resort in case the x86 ISO image installer does not recognize a specific essential hardware component like hard disk (NVME) or a network card that needs a higher kernel (backport).
	

First time use:
	If you have a screen attached, KVM or IMPI console the login screen will
	display the current IP address assigned for the |webui|. Open your browser
	and type that IP address. The default |webui| login credential is
	``admin:openmediavault``, the ``root`` password is the one you set during
	installation or was preconfigured by the choosen Debian distribution (i.e. Raspberry Pi OS).


.. note::
   |omv| will enable SSH access for the user ``root`` by default to be
   able to access a headless system in case of a broken installation or
   other maintenance situations. You can disable this behaviour in the
   ``Services | SSH`` page.

   To still get ``root`` access you need to create a non-privileged user
   and add them to the ``ssh`` and ``sudo`` groups. After that you can
   SSH into the system with this non-privileged user and run ``sudo su``.
