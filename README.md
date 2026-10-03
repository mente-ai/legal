# Mente: juridisch en ondersteuning

De pagina's waar de App Store en de app naar verwijzen. Statisch, geen build:
pushen naar `main` is uitrollen via GitHub Pages.

Dit is de enige publieke repo van Mente. De api en de app zijn privé.

| Bestand | Waarvoor |
|---|---|
| `privacy.html` | Privacyverklaring — verplicht veld in App Store Connect |
| `voorwaarden.html` | Gebruiksvoorwaarden |
| `support.html` | Ondersteuning — verplicht veld in App Store Connect |
| `account-verwijderen.html` | Hoe je je account wist; de URL staat in het reviewbriefje |
| `index.html` | Verzamelpagina met links naar het bovenstaande |
| `stijl.css` | Eén stylesheet voor alle pagina's |
| `app-store.md` | Het invulblad voor App Store Connect |

Live:

```
https://mente-ai.github.io/legal/privacy.html
https://mente-ai.github.io/legal/support.html
https://mente-ai.github.io/legal/account-verwijderen.html
```

## De regel

De teksten beschrijven wat de code werkelijk doet, niet wat gebruikelijk is.
Verandert er iets aan wat er bewaard wordt of waar het heen gaat, dan verandert
`privacy.html` mee en de datum bovenaan ook. `app-store.md` hoort hetzelfde te
blijven zeggen als de pagina's.

Twee dingen die makkelijk uit de pas gaan lopen:

- **De spraakmodus loopt via een US-hosted realtime-model.** Dat is het enige
  deel buiten de EU en het staat met opzet expliciet in de privacyverklaring.
- **Account verwijderen moet kloppen met de app.** De knop staat in de lade
  linksboven, onderin. Verhuist die, dan verhuist de beschrijving mee.
