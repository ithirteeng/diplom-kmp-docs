### Описание
Пока что звучит, как то, что нужно
### Что такое P2P
Очень хорошо объяснено [тут](https://www.geeksforgeeks.org/what-is-p2p-peer-to-peer-process/)
По сути мы будем создавать ту же Mesh-сеть. 
### Краткая информация по платформам
**Из [коммента](https://stackoverflow.com/a/35422117):**
The easiest (and most supported) way of getting multiple devices to connect to each other is using WiFi. Since your goal is to achieve data transfer with no internet, the most appealing solution would be to use a [Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer) network structure.
The two major smartphone OS's (Android and iOS) have API's and documentation on creating and transferring data over a Peer-to-Peer network.
- [Android WiFi P2P](https://developer.android.com/guide/topics/connectivity/wifip2p.html)
- [Apple Multipeer Connectivity](https://developer.apple.com/library/ios/documentation/MultipeerConnectivity/Reference/MultipeerConnectivityFramework/)

These two also have a means to encrypt the data being transferred.
Windows doesn't seem to have an API to allow multiple peers connected, but their [Proximity Class](https://msdn.microsoft.com/en-us/library/windows/apps/hh465215.aspx) will work for one device at a time.

---
**Android**
Android's WiFi P2P (peer-to-peer) API was created for transferring data without internet or another network. 

From their documentation:

> The Wi-Fi peer-to-peer (P2P) APIs allow applications to connect to nearby devices without needing to connect to a network or hotspot (Android's Wi-Fi P2P framework complies with the Wi-Fi Direct™ certification program). Wi-Fi P2P allows your application to quickly find and interact with nearby devices, at a range beyond the capabilities of Bluetooth. 

Google even has [Documentation](https://developer.android.com/reference/android/net/wifi/p2p/package-summary.html) and [training](https://developer.android.com/training/connect-devices-wirelessly/wifi-direct.html) on this API.

---
**iOS**
Apple's [Multipeer Connectivity](https://developer.apple.com/library/ios/documentation/MultipeerConnectivity/Reference/MultipeerConnectivityFramework/).
Very similar to Android's P2P API, they claim:

> The Multipeer Connectivity framework provides support for discovering services provided by nearby iOS devices using infrastructure Wi-Fi networks, peer-to-peer Wi-Fi, and Bluetooth personal area networks and subsequently communicating with those services by sending message-based data, streaming data, and resources (such as files).

Here is a decent looking [tutorial](http://nshipster.com/multipeer-connectivity/) on using Multipeer Connectivity.

### Проблемы
Есть ли возможность соединения между устройствами разных ОС. В интернете пишут, что используя Multipeer Connectivity едва ли получится, однако установить соединение все же можно.
[Чел пишет](https://developer.apple.com/forums/thread/12885): ```
```
Just as an aside, you can access peer-to-peer Wi-Fi without using Multipeer Connectivity. The underlying technology is Bonjour + TCP/IP, and you can access that directly from your app. The [WiTap sample code](https://developer.apple.com/library/ios/#samplecode/WiTap/) shows how.
```
короче какие-то способы есть
### Дополнительная информация
- [Статья](https://habr.com/ru/articles/333388/) о разработке библиотеки для соединения через Wifi Direct
- [Коммент на StackOverflow](https://stackoverflow.com/a/35422117) , с инфой по P2P-соединениях
- [Хороший гитхаб](https://github.com/onaio/android-p2p?ysclid=m27ta588hw840990223)