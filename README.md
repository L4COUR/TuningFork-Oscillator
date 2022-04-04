# Masters Thesis: Tonewheel
This repo is documenting my artistic research practice for my masters thesis in Audiodesign. This is a media archaeological examination of the tuningfork oscillator used by Poul la Cour in late 1800 for telegraphy and his experiments with "Tonehjulet" (patented 1878).

## Tonestrømsapparat
![](./media/LaCourStemmegaffelaparat.png)
![](./media/Stemmegaffel-elektromagnetisk.jpg)
Et *Tonestrømsapparat* består af en stemmegaffel monteret med en spændeskrue ved dets base. Modsat stemmegaflens grene er placeret en elektromagnet med form som en hestesko. Ved indersiden af en af stemmegaffel-grenene er placeret en kontakt i let berøring.

### Generering af en Tonestrøm
![](./media/LaCourTonestrømme.png)
Det Poul la Cour kalder en *tonestrøm* kan i vore dage anses for et audio/analog signal.

Stemmegaflens base er forbundet til GND, den ene af elektromagnetens pins er forbundet til V++, og den anden af elektromagnetens pins er forbundet til en kontakt sat i let berøring ved indersiden af en stemmegaffel-gren.
 
Følgende er beskrevet hvordan en tonestrøm skabes af et tonestrøms-apparat.

1. Stemmegaflen er i dets naturlige position hvor det ved at berøre kontakten lukker et kredsløb med dets elektromagnet
2. Den nu aktive elektromagnet tiltrækker den ene af stemmegafflens grene der således fjernes fra kontakten og afbryder kredsløbet med elektromagneten
3. idet elektromagneten taber sin magnetisme vender stemmegaflen tilbage til dens naturlige position og således etableres en cyklus fra step 1. igen.

Denne Cyklus hastighed er determineret af den pågældende stemmegaffels naturlige frekvens

Frekvens(Hz), hvor mange gange i sekundet stemmegaffelgrenene går mellem naturlig og udspilet position. 

1 Hz = 1 cyklus pr. sekund

Den mekaniske vibration frembragt af ovenstående cyklus er ofte hørbar.

Denne cyklus er kontinuerlig indtil strømmen slukkes, eller der er dannet så meget sod ved kontakt/stemmegaffel at berøringsfladen ikke længere er god.

## Re-(enactment)construction of "Tonestrømsapparat"
For at kunne udfører nogen form for re-enactment af tonestrømsapparattet kræver det konstruktionen af et apparat.

I min konstruktion har jeg anvendt en 440 Hz stemmegaffel med en 5v elektromagnet. Stemmegaflen er monteret i en 3D printet holder der er fastspændt på en træbundplade. Monteret med en skrue gennem træbundpladet er elektromagneten placeret så den uden at berøre stemmegaflen vil kunne tiltrække gaflens gren med sin magnetiske kraft. Over elektromagneten er monteret en holder ligeledes gennem træbundpladen hvorpå kontakten der kun let berør indersiden af stemmegaflens gren.

På stemmegaflens bund er et krokkodillenæbs monteret der fobinder stemmegaflen til GND. Den anden del af kredsløbet V++ er forbundet til elektromagneten, der videre er i forbindelse med kontakten.

I det originale tonestrømsapparat er der anvendt en hesteskoesmagnet, hvoraf jeg har valgt at anvende en tilsvarende helt almindre 5V stangelektromagnet. Pouls argument for at anvende en hesteskosmagnet er at den grundet sin form kan afgive en stærkere magnetisk påvirkning. Den 5V elektromagnet jeg har valgt at anvende har en kraft der kan løfte op til 5kg, hvilket er rigeligt for at kunne tiltrække stemmegaffel-grenen.

### Fejlkilder
- Kontakten
	- Stivhed
	- gnist sod
	- ekstremt følsom
- Træbundpladen
	- ujævnhed resulterer i pitch ændringer
- 3D-printet stemmegaffel holder
	- tolerancen gør at gaflen kan skubbes igennem og således komme for tæt på elektromagneten
- Krokkodillenæb ledninger, sidder løse, har dårlig kontakt til kredsløbet

### Udfordringer: Kontakt & unipolar vs. bipolar
Den første udfordring var at vælge den korrekte form for kontakt. **Graden af stivhed** er vigtig, hvis den er for elastisk giver metallet for meget efter og kommer ud af facon, hvis det er for stift er der ingen vibration mulig. **Bredden på kontakten**, hvis kontakt-fladen er for bred da har gaflen svært ved at bevare vibrationer, gennem forskellige empiriske undersøgelser fandt jeg at en stiv, spids, tøjnål var den umiddelbart bedste kontakt.

Den anden udfordring var at finde ud af hvordan jeg kunne aflæse stemmegaflens signal. Først anvendte jeg sonic arechaeology metoden hvor de elektromagnetiske signaler opfanges som lyd. Lyden jeg opfangede var elektromagneten der blev slukket og tændt med 440 Hz. Dette signal er bestemt brugbart som et clock-signal idet signalet var unipolart.

![](./media/LaCourTonestrømme.png)
Poul la Cour beskriver hvordan alle bølgerne i (Fig 2) kan siges at være tonestrømme. I min re-enactment har jeg valgt at fokusere på bølgerne *a,b og c* hvoraf *a og b* begge er unipolare bølger, hvorimod *c* er en bipolar bølge.