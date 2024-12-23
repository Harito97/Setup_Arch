I use Python 3.11 for this:
```bash
yay -S python311
```

Virtual environments are created with the `venv` module in /projects/venv:
```bash
cd /projects/venv
python3.11 -m venv ai_work#311
source ai_work#311/bin/activate
python3.11 -m venv financial#311
```
