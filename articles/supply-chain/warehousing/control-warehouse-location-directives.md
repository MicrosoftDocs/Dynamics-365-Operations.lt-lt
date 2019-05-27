---
title: Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus
description: Šioje temoje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje atliekamas darbas.
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e7c36fb912f35252d6e40d17477ac2962cbc23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558810"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje atliekamas darbas.

Instrukcijos, kurias sandėlio darbuotojai gauna mobiliajame įrenginyje, yra nustatomos pagal darbo šablonus, nustatytus „Microsoft Dynamics 365 for Finance and Operations“ siekiant apibrėžti įvairius sandėlio procesus ir užduotis. Darbo šablonai nurodo, kaip darbas atliekamas kiekvieno sandėlio proceso metu. Vietos nurodymą susiedami su darbo šablonais galite užtikrinti, kad darbas bus vykdomas konkrečiose faktinėse sandėlių vietose.

## <a name="work-templates"></a>Darbo šablonai
Puslapyje **Darbo šablonai** galima apibrėžti darbo operacijas, kurį reikia atlikti sandėlyje. Paprastai sandėlio darbo operacijas sudaro du veiksmai: sandėlio darbuotojas paima turimas atsargas vienoje vietoje ir tada padeda paimtas atsargas kitoje vietoje. 

Darbo šablonus sudaro antraštė ir susietos eilutės. Kiekvienas darbo šablonas yra skirtas konkrečiam *darbo užsakymo tipui*. Daugelis darbo užsakymų tipų yra susieti su šaltinio dokumentais, pvz., pirkimo arba pardavimo užsakymais. Tačiau kiti darbo užsakymų tipai nurodo atskirus sandėlio procesus, pavyzdžiui, ciklo skaičiavimą. *Darbo telkinio ID* leidžia skirstyti darbą į grupes. 

Darbo antraštės aprašo parametrus galima naudoti norint nustatyti, kada turi būti sukurtas naujas darbas. Pavyzdžiui, galite nustatyti didžiausią paėmimo eilučių skaičių ir didžiausią numatomą paėmimo laiką. Tada, jei pardavimo užsakymo išrinkimo proceso darbas viršija vieną iš šių reikšmių, tas darbas yra padalijamas į du darbus. 

Darbo eilutės nurodo faktines užduotis, kurių reikia norint vykdyti darbą. Pvz., viena siuntimo sandėlio proceso darbo eilutė gali būti skirta prekes paimti sandėlyje, o kita eilutė – tas prekes padėti į išdėstymo sritį. Taip pat gali būti papildoma eilutė prekėms iš išdėstymo srities paimti ir dar viena eilutė prekėms į sunkvežimį pakrauti (tai yra krovimo proceso dalis). *Krypties kodas* gali būti nustatytas darbo šablono eilutėse. Krypties kodas yra susietas su vietos nurodymu ir todėl padeda užtikrinti, kad sandėlio darbas yra vykdomas tinkamoje sandėlio vietoje. 

Galite nustatyti užklausą, norėdami kontroliuoti, kada konkretus darbo šablonas naudojamas. Pavyzdžiui, galite nustatyti apribojimą, kad konkretus šablonas būtų naudojamas tik atliekant darbą konkrečiame sandėlyje. Taip pat galite nustatyti kelis šablonus, kurie būtų naudojami siuntimo pardavimo užsakymo apdorojimo darbui kurti, atsižvelgiant į pardavimo šaltinį. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų darbo šablonų vertinimo tvarką. Todėl, jei turite labai konkrečią užklausą dėl konkretaus darbo šablono, turėtumėte jai priskirti žemą sekos numerį. Tada ta užklausa bus vertinama anksčiau nei kitos, bendresnės užklausos. 

Norėdami darbo procesą sustabdyti arba pristabdyti, galite naudoti darbo eilutės parametrą **Stabdyti darbą**. Tokiu atveju darbą atliekančio darbuotojo nebus prašoma atlikti kitą darbo eilutės veiksmą. Norėdamas pereiti prie kito veiksmo, tas arba kitas darbuotojas turi pasirinkti darbą dar kartą. Taip pat galite atskirti darbo užduotis, darbo šablono eilutėse naudodami kitą *darbo klasės ID*.

## <a name="location-directives"></a>Vietos nurodymai
Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas. Pvz., pardavimo užsakymo operacijoje vietos nurodymas nustato, kur prekės bus paimtos ir kur bus padėtos. Vietos nurodymus sudaro antraštė ir susietos eilutės, o jie kuriami puslapyje **Vietos nurodymai**. 

Kiekvienas antraštės vietos nurodymas turi būti susietas su *darbo užsakymo tipu*, nurodančiu, kuriam atsargų operacijos tipui nurodymas bus skirtas, pvz., pardavimo užsakymas, papildymas arba žaliavų paėmimas. *Darbo tipas* nurodo, ar vietos nurodymas bus skirtas išrinkimo darbui, padėjimo darbui, ar kažkuriam kitam sandėlio procesui, pvz., skaičiavimui arba atsargų būsenos keitimams. Taip pat turi būti nurodyta *teritorija* ir *sandėlis*. Antraštėje nurodytas *krypties kodas* gali būti naudojamas vietos nurodymui su vienu ar daugiau darbo šablonų susieti. 

Kalbant apie darbo šablonus, nustatydami užklausą galite nurodyti, kada naudojamas konkretus vietos nurodymas. Pavyzdžiui, galite nurodyti, kad kai pardavimo užsakymo šaltinis yra e. prekyba, atsargas reikia paimti iš paskirtos sandėlio vietos. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų vietos nurodymų vertinimo tvarką. 

Vietos nurodymo eilutės nustato papildomus vietos ieškos taisyklių taikymo apribojimus. Galite nurodyti mažiausią ir didžiausią kiekius, kuriems nurodymas būtų taikomas, taip pat galite nurodyti, kad nurodymas yra skirtas konkrečiam atsargų vienetui. Pavyzdžiui, jei matavimo vienetas yra padėklai, padėklų prekes galima padėti konkrečioje vietoje. Taip pat galite nurodyti, ar kiekis gali būti suskaidytas keliose vietose. Kaip ir vietos nurodymo antraštė, kiekviena vietos nurodymo eilutė turi sekos numerį, pagal kurį nustatoma eilučių vertinimo tvarka. 

Vietos nurodymams priskiriamas vienas papildomas informacijos lygis: *vietos nurodymo veiksmai*. Galite nurodyti kelis kiekvienos eilutės vietos nurodymo veiksmus. Primename, kad sekos numeris yra naudojamas veiksmų vertinimo tvarkai nustatyti. Šiame lygyje galite nustatyti užklausą, norėdami nurodyti, kaip rasti geriausią vietą sandėlyje. Taip pat galite naudoti iš anksto nustatytus **strategijos** parametrus optimaliausiai vietai rasti.

## <a name="location-directives-configuration-details"></a>Vietos nurodymų konfigūracijos informacija 

 ### <a name="sequence-number"></a>Eilės numeris
 
Šis numeris nurodo seką, kuria apdorojamas pasirinkto užsakymo tipo vietos nurodymas. Jį galima pakeisti naudojantis meniu mygtukais **Perkelti aukštyn** ir **Perkelti žemyn**.
 
 ### <a name="work-type"></a>Darbo tipas
 
Tai norimo atlikti darbo tipas. Galimas naudoti darbo tipas yra pagrįstas lauke **Darbo užsakymo tipas** pasirinktu atsargų operacijos tipu.
-   **Padėti** – Kai darbo tipas lygus **Padėti**, tai reiškia, kad vietos nurodymas suras labiausiai tinkamą vietą, kurioje būtų galima padėti į sistemą atkeliaujančias atsargas (gaunamas, pagamintas arba atsiradusias pakoregavus atsargas). Jį taip pat galima panaudoti norint nustatyti etapo vietos padėtį arba galutinę įlankos durų siuntimo vietą.
-   **Paimti** – Kai darbo tipas lygus **Paimti**, tai reiškia, kad sandėlis suras labiausiai tinkamą vietą, iš kurios būtų galima fiziškai rezervuoti atsargas (kurti darbą). Paėmimą galima atlikti (paėmimo darbo eilutę galima uždaryti) net ir tada, kai darbas nebaigtas. Vartotojas gali atlikti faktinį paėmimą, o tai yra paėmimo veiksmas. Tada vartotojas gali atšaukti naudodamasis mobiliuoju įrenginiu ir atlikti darbą vėliau. Tačiau atlikus galutinį padėjimą darbo antraštė uždaroma. 
-   **Skaičiavimas, koregavimai, pasirinkimas, atsargų būsenos keitimas, numerio lentelės kūrimas, spausdinimas, būsenos keitimas, pakavimas su įdėtosiomis numerių lentelėmis** – šie veiksmai nenaudojami jokioje vietos nurodymo sąrankoje. Tai išvardijimas, todėl su darbo užsakymo tipu nesiejamas joks filtravimas. 

### <a name="directive-code"></a>Krypties kodas

Pasirinkite nurodymo kodą, sietiną su darbo šablonu arba papildymo šablonu. Formoje **Nurodymo kodas** galite sukurti naujų kodų, kurie gali būti naudojami sujungiant darbo šablono papildymo šabloną su vietos nurodymu. Tai taip pat galima panaudoti norint sukurti bet kurios darbo šablono eilutės ryšį su vietos nurodymu (pvz., „baydoor“ arba etapo vieta).

Atkreipkite dėmesį į tai, kad jei nustatytas kodas, kol generuojamas darbas, sistema neieškos vietos nurodymo pagal seką, paieška bus atliekama pagal nurodymo kodą. Tai reiškia, kad galite tiksliau nurodyti, koks vietos šablonas naudojamas konkrečiam darbo šablono veiksmui, pvz., išdėstant medžiagas etapais. 

### <a name="site"></a>Svetainė

Vieta yra privalomas laukas, nes vietos nurodymas turi turėti vietą ir sandėlį, kuriam jis tinkamas. 

### <a name="warehouse"></a>Sandėlis

Sandėlis yra privalomas laukas, nes vietos nurodymas turi turėti vietą ir sandėlį, kuriam jis tinkamas.

### <a name="multiple-sku"></a>Keli SKU

Tokiu būdu vienoje vietoje, pvz., „baydoor“ gali būti keli sandėliavimo vienetai (SKU). Jei pasirinksite **Keli SKU**, padėjimo vieta bus nurodyta darbe (kurį tikimasi atlikti), bet bus galima apdoroti kelių prekių padėjimą (jei darbas apima skirtingus paimamus ir padedamus SKU, o ne vieną SKU padėjimą). Jei parinkties **Keli SKU** nepasirinksite, padėjimo vieta bus nurodoma tik tuo atveju, jei padėjimui naudojamas vienas SKU. Norint naudoti abu veiksmus, reikia nurodyti dvi eilutes: vieną, kurioje įjungti keli SKU, ir vieną, kurioje keli SKU išjungti. Jos turi būti tos pačios struktūros ir joms turi būti naudojama ta pati sąranka. Atlikdami padėjimo operacijas turite turėti identiškų vietos nurodymų, net jei darbo ID neskiriate vieno ir kelių SKU. Paėmimą taip pat turite nustatyti turėdami daugiau negu vienos prekės užsakymą.

### <a name="sequence-number"></a>Eilės numeris

Įveskite seką, kuria apdorojama pasirinkto darbo tipo vietos nurodymo eilutė. Prireikus taip pat galite keisti seką, naudodamiesi mygtukais **Perkelti aukštyn** ir **Perkelti žemyn**.

### <a name="fromto-quantity"></a>Kiekis nuo / iki

Tai suteikia galimybę nurodyti kiekio intervalą, kai turėtų būti pasirinkta tinklelio vidurio seka. Intervalą Nuo / iki galite nurodyti atitinkamais vienetais srityje Kiekis.

### <a name="unit"></a>Vienetas

Galite nurodyti mažiausią ir didžiausią kiekius, kuriems nurodymas būtų taikomas, taip pat galite nurodyti, kad nurodymas yra skirtas konkrečiam atsargų vienetui. Eilutės vieneto laukas naudojamas tik kiekio įvertinimui.

Tikrinant, ar vietos nurodymo eilutė taikoma, tai bus pagrįsta atitinkamu vietos nurodymo eilutėje nurodytu vienetu pateiktu kiekiu. Kiekvieną kartą pasiekusi vietos nurodymo eilutę sistema bandys konvertuoti poreikio vienetą į eilutėje nurodytą vienetą. Jei MV konvertavimo nėra, ji pereis prie kitos eilutės. 

### <a name="locate-quantity"></a>Sandėliavimo kiekis

Ši pasirinktis naudojama tik norint padėti kiekį į sandėlį / nustatyti kieko vietą sandėlyje. Ji naudojama tik padėjimo tipo darbams. Tinkamos vertės yra:

-   **Numerio lentelės kiekis** – Vertindami, ar kiekis patenka į kiekių intervalus „Nuo“ ir „Iki“, naudokite ant gaunamos numerio lentelės nurodytą kiekį.
-   **Vienetais išskirstytas kiekis** – Vertindami, ar kiekis patenka į kiekių intervalus „Nuo“ ir „Iki“, naudokite atliekant konkrečią operaciją vienetais skirstomą kiekį.
-   **Likęs kiekis** – Vertindami, ar kiekis patenka į kiekių intervalus „Nuo“ ir „Iki“, naudokite šiuo metu registruojamoje pirkimo užsakymo eilutėje likusį gauti kiekį.
-   **Tikėtinas kiekis** – Vertindami, ar kiekis patenka į kiekių intervalus „Nuo“ ir „Iki“, naudokite bendrą pirkimo užsakymo eilutės kiekį, nepriklausomai nuo to, kas jau gauta.

### <a name="restrict-by-unit"></a>Riboti pagal vienetą

Tokiu būdu vietos nurodymo eilutė gali būti pritaikyta konkrečiam matavimo vienetui ar keliems matavimo vienetams. Rezervuodami kiekį, jei norite rezervuoti tik iš tam tikro vietų rinkinio gautus padėklus, tada tinklelio vidurio seka apribotų tą konkrečią seką iki „PL“, kad bet koks už padėkle esantį kiekį mažesnis kiekis sekos nesirinktų. Pasirinkite **Riboti pagal vienetą** ir nustatykite vienetus. Taip pat galite apriboti, kad eilutėje būtų rodomas daugiau negu vienas vienetas. Tai taikoma tik dirbant su paėmimo tipo vietos nurodymais. 

### <a name="round-up-to-unit"></a>Apvalinti iki vieneto

Šis laukas naudojamas kartu su lauku **Riboti pagal vienetą**. Jei nustatyta vietos nurodymo eilutės **Riboti pagal vienetą** parinktis „laukelis“, pasirenkant **Apvalinti iki vieneto** nurodoma, kad vykdant nurodymą paimti žaliavas sukurtas darbas turėtų būti apvalinamas iki kelių veno sandėliavimo vieneto (nurodyto srityje **Riboti pagal vienetą**) vienetų. Atkreipkite dėmesį į tai, kad tai taikoma tik paimant žaliavas ir tik dirbant su paėmimo tipo vietos nurodymais.

### <a name="locate-packing-qty"></a>Pakavimo kiekio vietos nustatymas

Jei pakavimo kiekis nurodytas pardavimo užsakyme, perkėlimo užsakyme arba gamybos užsakyme, sistemai taikomas apribojimas, kad ji galėtų pasirinkti tik tas vietas, kuriose nurodytas pakavimo kiekis. Tai taikoma tik dirbant su paėmimo tipo vietos nurodymais.

### <a name="allow-split"></a>Leisti skaidyti

Tokiu būdu nurodoma, ar vietos nurodymui leidžiama skaidyti gaunamą kiekį arba keliose sandėlio vietose rezervuojamą kiekį, taip pat ar visas kiekis turi būti randamas vienoje vietoje, ar rezervuojamas iš vienos vietos, kad būtų galima sukurti darbą. 

### <a name="sequence-number"></a>Eilės numeris

Šis numeris yra seka, kuria apdorojamas pasirinkto darbo tipo vietos nurodymas. Seką, jei reikia, galite modifikuoti. Tačiau naudodami sekos numerius būkite atsargūs, kadangi apdorojimas visada vykdomas iš eilės. 

### <a name="name"></a>Pavadinimas / vardas ir (arba) pavardė

Įveskite vietos nurodymo veiksmo pavadinimą. Būtinai nurodykite tikslų pavadinimą.

### <a name="fixed-location-usage"></a>Fiksuotos vietos naudojimas 

-   **Fiksuotos ir nefiksuotos vietos** – Vietos nurodymas vertina visas vietas.
-   **Tik fiksuotos produkto vietos** – Vietos nurodymas vertina tik fiksuotas produktų vietas.
-   **Tik fiksuotos produkto varianto vietos** – Vietos nurodymas vertina tik fiksuotas produktų variantų vietas.

### <a name="allow-negative-inventory"></a>Leisti neigiamas atsargas

Pasirinkę šią parinktį leisite neigiamas atsargas nurodytoje vietos nurodymų sandėlio vietoje. 

### <a name="batch-enabled"></a>Paketas įjungtas 

Pažymėkite norėdami paketų strategijas naudoti prekėms, kurioms įgalinti paketai. Jei eilutė pasiekiama ten, kur parinktis **Paketas įjungtas** nustatyta nurodant ne paketo prekę, procesas tęsiamas iki kitos veiksmo eilutės. 

### <a name="strategy"></a>Strategija

-   **Konsoliduoti** – Ši strategija naudojama norint konsoliduoti konkrečios vietos prekes, kai jau yra panašių prekių. Tai taikoma tik vietos nurodymo paėmimo tipui. Dažniausiai padėjimas nustatomas taip, kad būtų konsoliduojama pirmoje veiksmo eilutėje, o paskui antroje eilutėje pabandoma padėti nekonsoliduojant. Konsoliduojant prekes vėliau jų paėmimas vyksta sparčiau.
-   **Pakavimo kiekio atitikimas** – Ši strategija naudojama norint patikrinti, ar paėmimo vietoje yra konkretus pakavimo kiekis. Tai taikoma tik paėmimo tipo vietos nurodymui. 
-   **FEFO paketo rezervavimas** – Ši strategija naudojama, kai atsargos surandamos naudojant paketo galiojimo datą ir priskiriamos paketo rezervavimui. Šią strategiją galima naudoti tik prekėms, kurioms įgalinti paketai. Tai taikoma tik paėmimo darbo tipo vietos nurodymui. 
-   **Apvalinti iki viso LP** – Ši strategija naudojama norint suapvalinti atsargų kiekį, kad atitiktų paimamoms prekėms priskirtą numerio lentelės (LP) kiekį. Šią strategiją galite naudoti tik paėmimo tipo vietos nurodymo papildymo tipui. 
-   **Tuščia vieta, kurioje negaunama darbo** – Ši strategija naudojama tuščioms vietoms rasti. Vieta laikoma tuščia, jei joje nėra fizinių atsargų ir jokio planuojamo darbo. Ši strategija naudojama tik vietos nurodymo padėjimo tipui. 

### <a name="example-of-the-use-of-location-directives"></a>Vietos nurodymų naudojimo pavyzdys

Šiame pavyzdyje svarstomas pirkimo užsakymo procesas, kai vietos nurodymas turi sandėlyje rasti laisvos vietos atsargų prekėms, kurios buvo ką tik užregistruotos gavimo rampoje. Pirmiausia reikia sandėlyje rasti laisvos vietos, konsoliduojant esamas atsargas. Jei konsoliduoti negalima, tada reikia rasti tuščią vietą. 

Pagal šį scenarijų turite nustatyti du vietos nurodymo veiksmus. Pirmasis sekos veiksmas turi naudoti strategiją **Konsoliduoti**, o antrasis – strategiją **Tuščia vieta, kurioje negaunama darbo**. Jei nenustatysite trečio veiksmo, skirto perpildos scenarijui tvarkyti, kai sandėlyje nėra vietos, galimi du rezultatai: darbą galima kurti net jei nėra nurodytų vietų arba darbo kūrimo procesas gali nepavykti. Rezultatas nustatomas pagal sąranką puslapyje **Vietos nurodymo klaidos**, kuriame galite nuspręsti, ar norite kiekvienam darbo užsakymų tipui nustatyti parinktį **Stabdyti darbą esant vietos nurodymo klaidai**.
