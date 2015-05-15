---
layout: post
title: ubuntu 维护命令
category: 工具
tags: [linux]
keywords: ubuntu
description: ubuntu 常用命令
---
## clean un-use soft
```bash
sudo apt-get -y remove account-plugin-facebook 
sudo apt-get -y remove account-plugin-flickr
sudo apt-get -y remove account-plugin-google
sudo apt-get -y remove account-plugin-jabber
sudo apt-get -y remove account-plugin-twitter
sudo apt-get -y remove webapps-common
sudo apt-get -y remove ibus
sudo apt-get -y remove tomboy

# game
sudo apt-get -y remove gnome-mahjongg
sudo apt-get -y remove gnome-mines 
sudo apt-get -y remove gnome-sudoku
sudo apt-get -y remove gnome-chess
sudo apt-get -y remove four-in-a-row
sudo apt-get -y remove gnome-klotski
sudo apt-get -y remove gnome-robots
sudo apt-get -y remove swell-foop 
sudo apt-get -y remove gnome-tetravex
sudo apt-get -y remove quadrapassel
sudo apt-get -y remove gnome-nibbles
sudo apt-get -y remove gnome-chess
sudo apt-get -y remove Iagno

# system no wanted tools
sudo apt-get -y remove software-center
sudo apt-get -y remove unity-webapps-common
sudo apt-get -y remove gedit
sudo apt-get -y remove totem
sudo apt-get -y remove aisleriot
sudo apt-get -y remove rhythmbox
sudo apt-get -y remove webbrowser-app
sudo apt-get -y remove empathy
sudo apt-get -y remove imagemagick
sudo apt-get purge apt-xapian-index
sudo apt-get -y remove libreoffice-core
sudo apt-get -y remove gnome-contacts
sudo apt-get -y remove gnome-orca
sudo apt-get -y remove onboard

# remove libreoffice
sudo apt-get -y remove libreoffice-core
sudo apt-get -y remove libreoffice-common

#sudo apt-get -y --auto-remove purge unity
#sudo apt-get -y --auto-remove purge unity-common
#sudo apt-get -y --auto-remove purge unity-lens*
#sudo apt-get -y --auto-remove purge unity-services
#sudo apt-get -y --auto-remove purge unity-asset-pool 

sudo apt-get autoremove
sudo apt-get autoclean
```
