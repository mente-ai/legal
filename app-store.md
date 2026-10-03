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
| Usage Data | Product Interaction | Aantal aanroepen en tekst per dag, voor de daglimiet; reacties op nieuwsverhalen (meer, minder, geopend) om de briefing te laten passen |
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

- **Leeftijdsclassificatie**: eerder schatte ik 17+ op grond van
  "Unrestricted Web Access". Bij nakijken zit er geen ingebouwde browser in de
  app: er is geen WKWebView en links openen in Safari. Dat vakje mag dus op nee
  staan, zoals het nu staat. Wat wel aan staat is gebruikersgegenereerde
  inhoud, en dat is juist: wat het model antwoordt is niet vooraf te
  overzien. De uitkomst van de vragenlijst is daarmee lager dan ik eerst zei;
  loop hem zelf na en beslis of je de moderatievragen anders beantwoordt.
- **Export compliance**: `ITSAppUsesNonExemptEncryption` staat al op `false` in
  `project.yml`. Alleen standaard-HTTPS.
- **Sign in with Apple**: verplicht om ook andere aanmeldwijzen aan te bieden is
  hier niet van toepassing, want Apple is de enige.
- **Schermafbeeldingen**: geüpload, vijf stuks van 1320x2868 uit de simulator
  van een iPhone 17 Pro Max, onder het formaat APP_IPHONE_67.
- **Beschrijving en trefwoorden**: hieronder.

## Naam, ondertitel en beschrijving

**Naam** (30 tekens): `Mente`

**Ondertitel** (30 tekens): `De assistent die je kent`

**Promotietekst** (170 tekens, kan zonder nieuwe versie veranderen):

> Nieuw: Mente onthoudt wat je normaal in huis haalt en vult aan wat ontbreekt.
> Vraag om een recept en hij legt de boodschappen erbij in je mandje.

**Beschrijving:**

> Mente onthoudt wat je vertelt.
>
> De meeste assistenten beginnen elk gesprek opnieuw. Mente niet. Wat je vertelt
> blijft hangen — je werk, je voorkeuren, waar je mee bezig bent — zodat je het
> niet elke keer opnieuw hoeft uit te leggen.
>
> WAT HIJ DOET
>
> • Antwoord geven, met het model dat bij je vraag past
> • Zoeken op het web wanneer het antwoord van actuele feiten afhangt
> • Plaatsen opzoeken en op de kaart laten zien
> • Je boodschappen in je mandje leggen bij Picnic
> • Elke ochtend het belangrijkste tech-nieuws, met de bronnen erbij
> • Praten in plaats van typen, als dat beter uitkomt
>
> WAT HIJ ONTHOUDT
>
> Je hoeft niets op te slaan. Wat over weken nog waar is blijft vanzelf hangen:
> hoe je heet, waar je aan werkt, dat je liever kort antwoord krijgt. Ook wat je
> normaal in huis haalt. Vraag om een recept en Mente weet welke ingrediënten je
> al hebt.
>
> JOUW GEHEUGEN, JOUW KEUZE
>
> Typ /geheugen om te zien wat Mente over je weet, en /vergeet om er iets uit te
> halen. Je account verwijderen kan in de app; dat wist alles, meteen.
>
> IN EUROPA
>
> Alle vragen lopen via een Europese doorgang en Mente kiest bij voorkeur
> modellen die binnen de EU draaien. Wil je zeker weten dat je gegevens Europa
> niet verlaten, dan kun je alleen-EU afdwingen. De spraakmodus is de enige
> uitzondering; dat staat in de privacyverklaring.
>
> WAT HET KOST
>
> Niets. Er geldt een royale daglimiet zodat de kosten beheersbaar blijven; wat
> je vandaag gebruikt zie je in de app.
>
> Mente geeft antwoorden van een taalmodel. Die kunnen fout zijn. Gebruik ze niet
> als vervanging van professioneel advies.

**Trefwoorden** (100 tekens, komma's zonder spaties):

```
assistent,geheugen,boodschappen,picnic,recepten,plannen,zoeken,spraak,privacy,eu
```

Dat is 80 tekens. Bewust géén merknamen van modellen erin: Apple wijst
trefwoorden af die het handelsmerk van een ander gebruiken. "Mente" hoeft er
niet in, de naam telt al mee.

**Primaire taal**: Nederlands. De app is volledig Nederlandstalig; een Engelse
listing zou beloven wat de app niet doet.

**Categorie**: Productiviteit, met Hulpprogramma's als tweede.
