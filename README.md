# GMGI221 prosjekt - Urbane indikatorer

*Jonas Okkenhaug Bratland*

---

## Plan

Tema: Urbane indikatorer: grønt, gatenett og befolkningstetthet i Grunerløkka og Nordstrand.

### Ideer til forskningsspørsmål
- Hvor mye grøntareal har bydelene, og hvor mange innbyggere bor nær en park?
- Hvordan skiller gatenettverket seg mellom en tett bydel og en villapreget bydel?
- Hvordan henger befolkningstetthet og vekst sammen med grøntareal?

### Datasett / kilder
- Bydelsgrenser og befolkning. Allerede tilgjengelig fra kurset.
- SSB-rutenett 250m (har allerede), og ett eldre år for å måle vekst (fra SSB/Geonorge).
- OSM-grøntareal og gatenett via osmnx (brukt i kurset).
- Eventuelt Oslos statistikkbank for å hente ut befolkningstall per bydel over tid.

### Ide til struktur
- funksjoner.py: funksjoner for å hente ut data fra OSM, SSB og Geonorge, samt funksjoner for å beregne indikatorer.
- analyse.ipynb: Jupyter-notebook for å kjøre analyser og lage visualiseringer.
- data/: mappe for å lagre nedlastede datasett.
- data/mellomresultater/: mappe for å lagre mellomresultater som ikke er endelige.
- figurer/: mappe for å lagre figurer som genereres i analysen.
- README.md: denne filen, med beskrivelse av prosjektet og hvordan man kan kjøre analysen og annet relevant informasjon.

### Forslag til indikatorer
1. Grøntareal og tilgang til grønt: andel grønt per bydel, kvadratmeter grønt per innbygger og andel innbyggere som bor innen 300 m fra en park. Her kombineres OSM og SSB-rutenett med overlay, buffer og romlig kobling, så den gir mest uttelling i vurderingen av romlig analyse.
2. Gatenett (med osmnx versjon 1.9, som i kursmiljøet): kryss per km², gatelengde per km² og hvor store kvartalene er. Nettverksanalyse teller som høyere vanskelighetsgrad.
3. Befolkningstetthet og vekst mellom to år. Den gir tallene du trenger for «grønt per innbygger», og en utvikling over tid.

### Tanker om ekstrapoeng
- Kjøre verktøyet for alle Oslos bydeler med parameterbytte og rangering.
- Eventuelt legge til flere indikatorer eller analyser om tid og kapasitet tillater det.

## Arbeidsplan med 4 hovedtrinn (f.eks. ett trinn per uke)
1. Formuler spørsmål endelig. Hent og test alle data, og sjekk CRS. Filstruktur.
2. Få indikator 1 til å virke for en bydel, og gjør om til funksjoner. Deretter muligens indikator 3.
3. Indikator 2 (osmnx). Kjør alt for begge bydeler med løkke. Lag kart med plott, grafer og interaktivt kart.
4. Diskusjon/refleksjon og ferdig README-rapport. Kjør alt fra start til slutt i rent miljø.
