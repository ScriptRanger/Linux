# WSL Ubuntu Neuinstallation & Bereinigung

## Schritt 1: Ubuntu aus WSL entfernen
wsl --unregister Ubuntu

## Schritt 2: Ubuntu aus den installierten Apps entfernen
# Öffne die Windows-Einstellungen (Win + I).
# Gehe zu "Apps > Installierte Apps" (Windows 11) oder "Apps & Features" (Windows 10).
# Suche nach "Ubuntu", klicke darauf und wähle "Deinstallieren".
# Bestätige die Deinstallation.

## Schritt 3: Überprüfung, ob noch WSL-Überreste vorhanden sind
wsl --list --verbose

## Schritt 4: WSL komplett zurücksetzen (optional)
# Falls WSL komplett auf Werkseinstellungen zurückgesetzt werden soll:
wsl --shutdown

# Falls Docker Desktop aus WSL entfernt werden soll:
wsl --unregister docker-desktop

# Falls WSL selbst deinstalliert werden soll:
wsl --uninstall

## Schritt 5: WSL neu installieren
wsl --install

## Schritt 6: Installation prüfen
wsl --list --verbose

## Schritt 7: Ubuntu starten und einrichten
wsl

# Falls ein neuer Benutzer erstellt werden soll, folge den Anweisungen.

# System aktualisieren
sudo apt update && sudo apt upgrade -y

## Falls Docker vorhanden war und neu installiert werden muss:
sudo apt install docker.io -y
