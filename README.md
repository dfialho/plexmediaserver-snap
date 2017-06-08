# Plex Media Server snap

Unofficial snap for the Plex media server

Plex organizes all of your personal media so you can easily
access and enjoy it. See https://www.plex.tv/

## Installation Instructions ##

Installing a snap package is the easiest thing in the world. To install this snap just enter the following command:

    sudo snap install menta-plexmediaserver
    
That is it! The plexmediaserver is now installed and already running on the background. You can check this with the command:

    sudo systemctl status snap.menta-plexmediaserver.server
    
## Adding Media from External Drives ##

A snap has very limited access to the system. By default, a snap does not have permission to access external drives. To fix this you need to enter an extra command:

    sudo snap connect menta-plexmediaserver:removable-media
    
After entering this command the plexmediaserver will be able to access any data inside the '/media/' directory (where external drives are usually mounted on).
