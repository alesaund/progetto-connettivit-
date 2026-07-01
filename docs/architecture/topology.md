# Topologia della rete

> Documento in evoluzione.

## Obiettivi
- Alta affidabilità
- Copertura Wi-Fi completa
- Mesh dedicata
- Documentazione completa

## Componenti principali

### Router
- OpenWrt x86 (Intel J4125)
- Gateway della rete
- WireGuard
- DHCP/DNS

### Access Point
- AP Studio
- AP Soggiorno (MX4200 tri-radio)
- AP Cucina (MX4200 tri-radio)
- AP Piano Superiore

## Principi progettuali
- SSID unico per i client.
- Mesh dedicata sulla terza radio degli MX4200.
- Canali Wi-Fi pianificati manualmente.
- Reboot completo dopo modifiche strutturali alle radio.
- Watchcat configurato in modalità ping_reboot.

## TODO
- Inserire schema fisico.
- Inserire schema logico.
- Aggiungere indirizzamento IP.
- Documentare switch e server Murmur.
- Collegare i documenti dell'inventory.