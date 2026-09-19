# LB 324

## Aufgabe 2
Erklären Sie hier, wie man `pre-commit` installiert.

## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.

## Pre-commit

Für die lokalen Automatisierungen müssen zuerst die Projektabhängigkeiten und
pre-commit installiert werden:

```bash
python -m pip install -r requirements.txt
python -m pip install pre-commit pytest