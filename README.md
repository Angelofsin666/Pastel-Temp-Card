#
🌡️ Pastel Temp Card

Card Lovelace per Home Assistant con sfondo colorato monocromatico, termometro SVG, media zona, righe stanza con slider e badge umidità.


#
Funzionalità

    Sfondo colorato su tutta la card — un colore scelto via visual editor, nessun override

    Panel summary con termometro SVG + media zona + badge umidità

    Barra progresso proporzionale alla temperatura sulla scala configurata

    Righe stanza con icona MDI + nome + temperatura + slider + umidità

    Alert temperatura e umidità segnalati con testo/icona, senza cambiare il colore della card

    Visual editor completo — colore, stanze, entità, icone, soglie alert, scala temp

    Trend opzionale calcolato dalla history di HA

    8 palette disponibili: blue, green, purple, teal, amber, pink, indigo, cyan

#
Installazione via HACS

    HACS → Frontend → menu ⋮ → Custom repositories

    URL: https://github.com/Angelofsin666/pastel-temp-card — Categoria: Lovelace

    Installa e riavvia HA

#
Installazione manuale

Copia pastel-temp-card.js in /config/www/ e aggiungi in configuration.yaml:

lovelace:
  resources:
    - url: /local/pastel-temp-card.js
      type: module

#
Configurazione YAML

type: custom:pastel-temp-card
title: Piano Terra
subtitle: Temperature ambiente
color: blue          # blue | green | purple | teal | amber | pink | indigo | cyan
temp_min: 15         # scala minima barra (°C)
temp_max: 35         # scala massima barra (°C)
alert_temp: 30       # soglia alert caldo (°C)
alert_hum: 65        # soglia alert umidità (%)
show_trend: true     # mostra trend da HA history
rooms:
  - name: Ingresso
    icon: mdi:door
    temp_entity: sensor.temperatura_ingresso
    hum_entity: sensor.umidita_ingresso
  - name: Salotto
    icon: mdi:sofa
    temp_entity: sensor.temperatura_salotto
    hum_entity: sensor.umidita_salotto

#
Palette colori
Chiave
	
Colore
blue
	
Azzurro
green
	
Verde
purple
	
Viola
teal
	
Verde acqua
amber
	
Ambra
pink
	
Rosa
indigo
	
Indaco
cyan
	
Ciano
#
Licenza

MIT — Angelofsin666


