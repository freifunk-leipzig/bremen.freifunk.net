---
layout: default
title: Technik
category_id: 2
---
## Netzwerk

Das Freifunk-Netz besteht aus einer Kombination von klassischen WLANs, Ad-hoc WLANs (Mesh) und VPNs.

<img src="/images/diagram.png" style="float:right; margin-left: 10px;" alt="Erläuterndes Diagramm">

Das klassische WLAN ist das, worüber du und jeder andere sich einfach verbinden kann. Es bietet einen einfachen und schnellen Zugang zum Freifunk-Netz.

Das Ad-hoc WLAN verbindet die Router untereinander zum sogenannten Mesh. Wenn zwei Router nah genug beieinander stehen, um sich per WLAN erreichen zu können, bauen Sie eine Funkverbindung auf. So können sie und alle mit ihnen verbundenen Geräte unabhängig vom Internetanschluss der Betreiber miteinander kommunizieren. Hier verwenden wir [B.A.T.M.A.N. Advanced], ein Layer-2-Routingprotokoll, das schnell auf Topologieänderungen im Mesh reagieren kann.

Schließlich sind wegen der Entfernungen aber nicht alle Router per Funk verbunden. Deswegen gibt es außerdem sogenannte VPNs zu den von uns betriebenen VPN-Servern. Damit können die Router auch das allgemeine Internet als Verbindung untereinander nutzen. Auch hier kommt B.A.T.M.A.N. Advanced zum Einsatz, die VPNs selbst bauen wir mit Hilfe von [fastd] auf. Über die VPN-Server läuft auch deine Verbindung, wenn du über das Freifunk-Netz auf eine Seite im Internet zugreifst. Von dort wird sie nochmals umgeleitet, zum Beispiel über einen [Server des Verein freie Netze e.V.](http://wiki.freifunk.net/Vpn03), um auch unsere Identität nicht im Netz preiszugeben.

## Autoupdate

[fastd]: https://projects.universe-factory.net/projects/fastd
[B.A.T.M.A.N. Advanced]: http://www.open-mesh.org/projects/batman-adv
