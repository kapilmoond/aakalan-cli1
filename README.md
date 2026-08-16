# Aakalan CLI

Local backend for **Aakalan Agent**, by **Aaklan Infra Consultancy**.

Website: [aakalaninfra.com](https://aakalaninfra.com)

This repository is the command-line engine that the Aakalan Agent desktop EXE
installs on a client PC. Clients should see **Aakalan**, never Hermes or Nous.

## Client-facing names

| Item | Value |
|---|---|
| Product | Aakalan Agent |
| Command | `aakalan` |
| Company | Aaklan Infra Consultancy |
| Home (Windows) | `%LOCALAPPDATA%\aakalan` |
| Checkout | `%LOCALAPPDATA%\aakalan\aakalan-cli` |
| Official GitHub | https://github.com/kapilmoond/aakalan-cli |

Internal Python modules may still use `hermes_*` names. That is engine
plumbing only.

## Desktop first-run

The Windows EXE installs **locally only**. There is no cloud / remote choice.

## Install (after this repo is on GitHub)

Windows:

```powershell
iex (irm https://raw.githubusercontent.com/kapilmoond/aakalan-cli/main/scripts/install.ps1)
```

Then run:

```bat
aakalan
```

## Push this local repo to GitHub

1. On GitHub, create an **empty** repository named `aakalan-cli` under `kapilmoond` (no README).
2. In PowerShell:

```bat
cd "C:\Users\LAPTOP PC\Desktop\3_Apps_and_Development\aakalan-cli"
git remote add origin https://github.com/kapilmoond/aakalan-cli.git
git push -u origin main
```

3. Rebuild the Aakalan Agent desktop EXE so first-launch can download `scripts/install.ps1` from this repo.
