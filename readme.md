## Pre-commit

Für die lokalen Automatisierungen müssen zuerst die Projektabhängigkeiten und pre-commit installiert werden:

```bash
python -m pip install -r requirements.txt
python -m pip install pre-commit pytest
```

Danach müssen die Hooks installiert werden:

```bash
pre-commit install
pre-commit install --hook-type pre-push
```

Beim Commit wird der Python-Code automatisch mit Black formatiert.

Beim Push werden automatisch die Tests mit pytest ausgeführt.

## Deployment

Die Applikation ist auf Render verfügbar:

https://winterhofen-lb324.onrender.com

Die Auslieferung erfolgt auf Render als mit der Lehrperson abgesprochene Alternative zu Azure.

Das lokale Passwort aus der `.env`-Datei wird nicht im Repository gespeichert.

Auf Render wurde unter Environment Variables die Variable `PASSWORD` angelegt.
Als Wert wird gemäss Aufgabenstellung der GitHub-Benutzername verwendet.

Für die automatische Auslieferung wurde auf Render ein Deploy Hook erstellt.
Die Deploy-Hook-URL wird auf GitHub als Repository Secret
`RENDER_DEPLOY_HOOK_URL` gespeichert.

Bei einem erfolgreichen Merge in den `main`-Branch startet die GitHub Action
`.github/workflows/deploy.yml` automatisch eine neue Auslieferung auf Render.