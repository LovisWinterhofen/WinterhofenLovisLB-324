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