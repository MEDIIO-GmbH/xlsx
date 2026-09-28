# xlsx

Unveränderter Spiegel des Pakets `xlsx` von [SheetJS](https://sheetjs.com),
Version 0.20.3, verteilt über GitHub.

| Feld | Wert |
| --- | --- |
| Codename | MEDIIO 2.0 |
| Use Case | SheetJS `xlsx` ohne Zugriff auf `cdn.sheetjs.com` installieren |
| Produkte | Werkzeug |
| Tech-Stack | JavaScript |
| Ansprechpartner | [@oskarherz](https://github.com/oskarherz) |
| Status | Spiegel, eingefroren auf v0.20.3 |
| Default-Branch | `main` |
| Läuft auf | nirgends, wird per Tarball installiert |
| Agenten-Leitfaden | keiner |

Der Spiegel existiert, weil CI und die Claude-Code-Sandbox nur über Proxys mit
Host-Allowlist ins Netz gehen und `cdn.sheetjs.com` nicht erreichen; GitHub
liefert dasselbe Paket, und das Lockfile pinnt den Tarball auf den Commit des
Tags. Ihn konsumieren `apps/data-bridge` und `packages/tasks` in
[`mediio-app-platform`](https://github.com/MEDIIO-GmbH/mediio-app-platform)
über den Specifier `github:MEDIIO-GmbH/xlsx#v0.20.3`. Ein Update spiegelt ein
neues Tag über den Workflow `.github/workflows/sync-upstream.yml` (manuell
startbar; den wöchentlichen Lauf hat GitHub nach dem letzten Lauf am 2026-06-15
wegen Inaktivität abgeschaltet), hebt danach den Specifier in beiden
`package.json` an und löst das Lockfile mit `pnpm install` neu auf.

> **Spiegel, kein Fork.** Hier wird kein Quellcode geändert. Entwicklung,
> Fehler und Wünsche gehören zu SheetJS.

## Aktuelle Version

`v0.20.3`, gespiegelt von
<https://cdn.sheetjs.com/xlsx-0.20.3/xlsx-0.20.3.tgz>

## Verwendung

In der `package.json`:

```jsonc
{
  "dependencies": {
    "xlsx": "github:MEDIIO-GmbH/xlsx#v0.20.3"
  }
}
```

Zuletzt geprüft: 2026-09-28
