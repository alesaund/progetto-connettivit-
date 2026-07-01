# SOP - OpenWrt Upgrade

## Scope
Procedura standard per aggiornare router e access point OpenWrt.

## Pre-check
- Verifica uptime (`uptime`)
- Verifica memoria (`free -m`)
- Verifica spazio (`df -h`)
- Controlla log (`logread | tail -100`)

## Backup
- `sysupgrade -b /tmp/backup-$(hostname)-$(date +%F).tar.gz`
- Facoltativo: `uci export > /tmp/uci-$(hostname).txt`

## Upgrade
- Preferire Attended Sysupgrade mantenendo la configurazione.
- Dopo modifiche radio importanti (canale, larghezza, mesh), eseguire sempre un reboot completo.

## Post-upgrade
- Attendere 3-5 minuti.
- Verificare `iw dev`, `wifi status`, `logread | grep -iE "oom|ath11k|hostapd|failed"`.
- Verificare mesh, roaming, WireGuard e client.

## Burn-in
Lasciare il dispositivo in esercizio 24 ore e ricontrollare uptime, memoria e log.

## Note MX4200
- Watchcat: ping_reboot.
- forcedelay: 300 secondi.
- Evitare ripetuti `wifi reload`; preferire reboot dopo modifiche radio strutturali.
