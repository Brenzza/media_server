## How to

1. Clone the Repository
2. chmod +x config.sh
3. ./config.sh and add the requested information
4. chmod +x deploy_media_server.sh
5. ./deploy_media_server.sh
6. Add server: http://localhost:32400/web
7. Configure qbittorrent, radarr, sonarr and plex
* qbittorrent admin password: docker logs *container id*

## RADARR+SONARR CONFIG
Settings -> Media Management: /data/TVSHOWS/Shows
Settings -> Download Clients:

Host -> IP Address of qbittorrent
Remote Path -> /data/{ MOVIES | SHOWS }/Download/
Local Path  -> /data/{ MOVIES | SHOWS }/Download/
* MOVIES for radarr | SHOWS for sonarr

## Monitor Deletions: crontab -e
0 0 * * 0 /root/media_server/monitor_deletions.sh

Add to monitor deleted content from plex or torrents weekly #optional


## 💖 Support Me
If you like my work and want to support me, you can donate via PayPal:
<a href="https://www.paypal.com/paypalme/JoyceWythe" target="_blank">
    <img src="https://www.paypalobjects.com/webstatic/en_US/i/buttons/PP_logo_h_100x26.png" width="120" alt="Donate via PayPal">
</a>
