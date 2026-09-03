
# Woodeys Place V2 Testing
Thanks for being part of my little project, I hope its of some use to you, it's already proving useful to me as its the one place I can keep everything together. Whether i haev films store on a NAS, blu-ray disc or bought from APPLE TV, i can add everything to a single library, so i know what i have.

## Media server integration
I have built in media server importing to this version and i have tested on Jellyfin, Emby and Plex. All services allow you to connect to your server and then choose a libary to import. When importing it will add to whatever is your library already and not overwrite, unless you have added the same film manually.  
PLEASE NOTE: This functionality has only been tested on my setup, so if you have any issues i would need to know your configuration to see if there would be a fix.

### Connectiing to your server
In order to connect to your server of choice, you will need to allow the connection. For jellyfin and emby, you will need to create an API key (Dashboard -> Advancced -> API Keys) and know the IP address of you server. It will look something like: 192.168.1.100:8096, paste this along with the API key and it should connect.

Jellyfin and Emby should also allow control directly from the app to your player, so you can start and stop films directly from the App. This, unfortunately is a bit trickier on Plex but it should be working if you use the Apple TV version.

