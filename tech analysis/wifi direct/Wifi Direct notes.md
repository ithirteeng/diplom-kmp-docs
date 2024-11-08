# Теория
## Поиск девайсов
Есть такая тема, как локальные сервисы, позволяющие заранее сказать, вот нам нужно искать девайсы из списка только с этим запущенным приложением.
Из [документации](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager):
> [!quote] 
> With peer discovery using `[discoverPeers(Channel, ActionListener)](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))`, an application discovers the neighboring peers, but has no good way to figure out which peer to establish a connection with. For example, if a game application is interested in finding all the neighboring peers that are also running the same game, it has no way to find out until after the connection is setup. Pre-association service discovery is meant to address this issue of filtering the peers based on the running services.
> 
> With pre-association service discovery, an application can advertise a service for a application on a peer device prior to a connection setup between the devices. Currently, DNS based service discovery (Bonjour) and Upnp are the higher layer protocols supported. Get Bonjour resources at dns-sd.org and Upnp resources at upnp.org As an example, a video application can discover a Upnp capable media renderer prior to setting up a Wi-fi p2p connection with the device.

Bonjur, Upnp - технологии, на основе [DNS](https://skillbox.ru/media/code/dns-chto-eto-takoe-i-kak-eye-ispolzuyut/)



