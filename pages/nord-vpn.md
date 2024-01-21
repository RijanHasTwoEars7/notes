# How to set nord-vpn meshnet to always on
- `sudo nano /etc/systemd/system/nordvpn.service`
  logseq.order-list-type:: number
- logseq.order-list-type:: number
  ```
  [Unit]
  Description=NordVPN
  After=network.target
  
  [Service]
  ExecStart=/usr/bin/nordvpn connect
  Restart=on-failure
  
  [Install]
  WantedBy=multi-user.target
  ```
- `sudo systemctl enable nordvpn.service`
  logseq.order-list-type:: number
- `sudo systemctl start nordvpn.service`
  logseq.order-list-type:: number
-