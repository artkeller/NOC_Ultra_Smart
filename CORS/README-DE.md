# CORS (Cross-Origin Resource Sharing) erklärt

[![Language](https://img.shields.io/badge/Sprache-🇩🇪%20Deutsch-informational)](./LANGUAGE-DE.md)

## 1. Das Kernkonzept: Warum gibt es CORS?

- Standardmäßig erzwingen **Browser** die **Same-Origin Policy (SOP)**.

- Diese verhindert, dass **Skripte** von **Website A** (z. B. `evil-site.com`) 
ungefragt Daten von **Website B** (z. B. `mein-bank-konto.de`) abrufen, 
während Sie dort eingeloggt sind. 

- **CORS** ist die kontrollierte **Ausnahme** von dieser **Regel**. 

- Es erlaubt einem **Server**, explizit zu sagen: „Ich vertraue Anfragen 
von `domain-a.com` und erlaube den Zugriff auf meine Daten“. 

## 2. Was ist eine „Origin“?

Zwei URLs haben dieselbe **Origin**, wenn diese drei Merkmale identisch sind: 

    Protokoll (z. B. http vs. https)
    Domain (z. B. beispiel.de vs. api.beispiel.de)
    Port (z. B. :80 vs. :443)

## 3. Wie funktioniert der Prozess?

Wenn Ihr **Browser** eine Anfrage an eine andere **Origin** stellt 
(z. B. via `fetch()` oder `XMLHttpRequest`), läuft folgender Prozess ab: 

1. **Die Anfrage:** Der **Browser** fügt automatisch den Header 
`Origin: https://deine-seite.com` hinzu.
2. **Die Prüfung (Preflight):** Bei „komplexen“ Anfragen (z. B. mit 
`PUT`, `DELETE` oder speziellen JSON-Headern) sendet der **Browser** vorab 
eine `OPTIONS`-Anfrage. Er fragt den Server: „Darf ich diese Anfrage 
mit diesen Methoden stellen?“.
3. **Die Antwort:** Der Server antwortet mit **CORS**-Headern. 
Der wichtigste ist: `Access-Control-Allow-Origin: https://deine-seite.com` 
(oder * für alle).
4. **Die Entscheidung:** Stimmt der Header des Servers mit der **Origin** 
der Website überein, lässt der Browser den Zugriff zu. Falls nicht, 
blockiert der **Browser** die Antwort und zeigt einen **CORS**-Fehler 
in der Konsole an. 

## 4. Wichtige Fakten für Entwickler

- **Browser-Sache:** **CORS** wird vom **Browser** erzwungen, nicht vom **Server**. 
Tools wie `Postman` oder `curl` ignorieren **CORS**-Regeln komplett.

- **Kein Ersatz für Authentifizierung:** **CORS** schützt den Nutzer davor, dass fremde Seiten in seinem Namen agieren. Es ersetzt jedoch keine **API-Keys** oder **Logins** auf dem Server.

- **Wildcards:** `Access-Control-Allow-Origin: *` erlaubt jeder Seite den Zugriff. Das ist für öffentliche APIs (z. B. Google Fonts) okay, aber für private Daten gefährlich. 

