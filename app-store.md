# Wat er in App Store Connect ingevuld moet worden

Afgeleid uit wat de code werkelijk doet, niet uit wat gebruikelijk is. Verandert
er iets aan wat er bewaard wordt, dan verandert dit mee.

## URL's

| Veld | Waarde |
|---|---|
| Privacy Policy URL | `https://mente-ai.github.io/legal/privacy.html` |
| Support URL | `https://mente-ai.github.io/legal/support.html` |
| Marketing URL | leeg laten, of de index |

## App Privacy: wat we verzamelen

Voor elk gegeven hieronder geldt: **gekoppeld aan de gebruiker**, gebruikt voor
**App Functionality**, en **niet** voor tracking, advertenties of
personalisatie van advertenties. Op de vraag "Do you or your third-party
partners use data for tracking?" is het antwoord **nee**.

| Categorie | Type | Waarom |
|---|---|---|
| Contact Info | Email Address | Alleen als de gebruiker het bij Sign in with Apple deelt; mag Apple's doorstuuradres zijn |
| Identifiers | User ID | De Apple-identificatie en ons eigen account-id |
| User Content | Other User Content | De gesprekken, en het profiel dat eruit volgt |
| User Content | Photos or Videos | Foto's die iemand meestuurt in een gesprek |
| Usage Data | Product Interaction | Aantal aanroepen en tekst per dag, voor de daglimiet |
| Diagnostics | Other Diagnostic Data | Technische logs op de server: tijdstippen, fouten, IP-adres van het verzoek |

Niet verzamelen, dus overal **nee**: Location, Contacts, Health & Fitness,
Financial Info, Browsing History, Search History, Sensitive Info, Advertising
Data, Purchases.

Let op bij het invullen: Apple vraagt per type apart of het **gekoppeld** is aan
identiteit en of het voor **tracking** wordt gebruikt. Alles hierboven is
gekoppeld (het hangt aan een account) en niets is tracking.

## Account verwijderen

Apple controleert hierop sinds 2022. De knop staat in de app: lade linksboven,
onderin **Verwijder account**. De pagina
`https://mente-ai.github.io/legal/account-verwijderen.html` beschrijft de stappen
en wat er weggaat. Zet die URL in het reviewbriefje.

## Reviewbriefje (App Review Information → Notes)

Zoiets:

> Mente is een Nederlandstalige persoonlijke assistent. Aanmelden gaat met Sign
> in with Apple; er is geen ander account nodig en er is niets te kopen.
>
> Account verwijderen: open de lade linksboven, scrol naar onderen, tik op
> "Verwijder account". Dat wist onmiddellijk alle gegevens.
>
> De antwoorden komen van taalmodellen via Opper (EU). De spraakmodus gebruikt
> een realtime-model dat in de VS draait; dat staat in de privacyverklaring.
>
> Connectors zoals Picnic zijn optioneel en vragen om de eigen inloggegevens van
> de gebruiker bij die dienst. Ze zijn niet nodig om de app te beoordelen.

## Overig

- **Leeftijdsclassificatie**: de app geeft door een taalmodel gegenereerde
  antwoorden en kan het web doorzoeken. Dat is in Apple's vragenlijst
  "Unrestricted Web Access" en gebruikersgegenereerde inhoud; reken op 17+,
  tenzij je de webtoegang in de vragenlijst anders kunt verantwoorden.
- **Export compliance**: `ITSAppUsesNonExemptEncryption` staat al op `false` in
  `project.yml`. Alleen standaard-HTTPS.
- **Sign in with Apple**: verplicht om ook andere aanmeldwijzen aan te bieden is
  hier niet van toepassing, want Apple is de enige.
- **Schermafbeeldingen**: nog te maken. Nodig voor ten minste 6,7 inch; de
  simulator van een iPhone 17 Pro levert de juiste maat.
- **Beschrijving en trefwoorden**: nog te schrijven.
