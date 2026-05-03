### Mida uurin?
On levinud rahvalik pärimus, et jaanipäeval (23.juuni) sajab. Tekib küsimus, kas jaanipäev on lihtsalt üks sajustest päevadest või sajutõenäosuse poolest eristuv päev?
Eesmärk on ajaloolisi sademete andmeid kasutades:
- määrata  baastase ehk üldine saju tõenäosus, kui valida suvaline juunipäev, arvestamata konkreetset kuupäeva. 
- hinnata, kui tõenäoline on sadu jaanipäeval ning kuidas see erineb baastasemest.
- uurida, kuidas juuni kuupäevade sajutõenäosused baastaseme suhtes jaotuvad ning kas mõni kuupäev (nt jaanipäev) eristub kõrgema sajutõenäosusega.

### Andmed
Keskkonnaagentuuri Ilmateenistus:
https://www.ilmateenistus.ee/kliima/ajaloolised-ilmaandmed/
Algandmed: Tallinn-Harku 2004-2025.Tunnipõhised vaatlused (Excel).
Edasiseks kasutamiseks salvestan CSV formaati ning koondan tunnipõhised vaatlused ööpäevasteks summadeks.

### Metoodika
Andmete ettevalmistamisel kontrollin veerunimed, andmetüübid ja puuduvad väärtused. Ühendan tabelid, eraldan sademete andmed ning loon edasiseks analüüsiks ühtse CSV-faili. 
Seejärel filtreerin välja ainult juuni andmed ja koondan tunnipõhisteks.

Esmase ülevaate saamiseks vaatan 23. juuni sademete hulka aastate lõikes. Selgub, et varieeruvus on suur: enamikul aastatel on sademeid vähe või üldse mitte, kuid üksikutel aastatel on sadu väga tugev, mis mõjutab keskmist. See aitab otsustada sadu defineerivad lävendid: >0 mm (sademeid üldse) ; >5 mm (mõõdukas sadu); >10 mm (tugev sadu).

Tõenäosused arvutan sagedusena ehk osakaaluna kõikidest vaatlustest. Kokku on 22 aasta ööpäevased vaatlused. See tähendab, et baastase arvutatakse 660 vaatluse põhjal ning iga konkreetse kuupäeva tõenäosus 22 aasta vaatluse põhjal. Tulemused visualiseerin graafikutel.

### Tulemused
Jaanipäeval on saju tõenäosus kõigi lävendite korral veidi suurem kui juunikuu üldine baastase. 
Suurim  erinevus on tugeva saju korral (>10 mm). Jaanipäev kuulub sel juhul pigem kõrgema sajutõenäosusega päevade hulka, kuid ei eristu selles grupis teistest päevadest.

### Kuida notebooki kasutada
