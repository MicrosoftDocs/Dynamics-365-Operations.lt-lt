---
title: Įkeltų išlaidų ir transportavimo valdymo palyginimas
description: „Microsoft Dynamics 365 Supply Chain Management” siūlo du skirtingus modelius darbui su transportavimu – transportavimo valdymą (TMS) ir įkeltas išlaidas. Šioje temoje apibendrinamos abejų modulių tapačios funkcijos ir išryškinami jų skirtumai.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba745048d1d9f28300f03ed0bc98142d80aa5a26
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569822"
---
# <a name="landed-cost-vs-transportation-management"></a>Įkeltų išlaidų ir transportavimo valdymo palyginimas

[!include [banner](../../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management” siūlo du skirtingus modelius darbui su transportavimu: **Transportavimo valdymą (TMS)** ir **Įkeltas išlaidas**. Šioje temoje apibendrinamos abejų modulių tapačios funkcijos ir išryškinami jų skirtumai. Galite naudoti šią informaciją siekiant nuspręsti, kuris modulis geriausiai tinka jūsų veiklos praktikai. Galite pastebėti, jog kai kurioms veiklos praktikoms labiau tinka TMS, o kitoms geriausiai tinka Įkeltos išlaidos. Tada, atsižvelgdami į savo veiklos poreikius, galite pasirinkti naudoti tik vieną modulį arba galite sujungti šiuos du modulius.

Ši tema nėra išsami visų kurio nors modulio funkcijų apžvalga. Vietoj to, ji išryškina galimas funkcijas, nes jos susijusios su prekių transportavimu iš tiekėjo į jūsų veiklos sandėlį, kuriame jos gali būti suvartojamos.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminologijos, nuorodų duomenų ir ataskaitų skirtumai

### <a name="terminology-comparison"></a>Terminologijos palyginimas

TMS ir Įkeltos išlaidos naudoja skirtingus terminus panašioms koncepcijoms. Šioje lentelėje apibendrinami šie terminai ir jų naudojimas dvejuose moduliuose.

| TMS terminas | Įkeltų išlaidų terminas | Pastabos |
|----------|------------------|-------|
| **Krovinys**<p>*Krovinys* yra siuntų, kuriuos tuo pačiu metu transportuojamos tuo pačiu transportavimo vienetu (pavyzdžiui, sunkvežimiu arba laivu), rinkinys. Kroviniai gali būti gaunami arba siunčiami.</p> | **Reisas**<p>Įprastai, *reisas* yra viena transporto priemonė, kuri nukeliauja vieną *kelionę*. Reise gali būti keletas *siuntimo konteinerių*, taip pat jame gali būti gaunamų užsakymų iš skirtingų jūsų organizacijos juridinių subjektų. Reisai gali būti tik siunčiami.</p> | TMS taip pat naudoja terminą *reiso numeris*, kuris nurodo informacijos lauką, kuriame galite įvesti identifikatorių. Tačiau jokia funkcija nėra susieta su TMS lauku ir ji nesusijusi su *reiso* sąvoka Įkeltų išlaidų modulyje. |
| **Maršrutas**<p>*Maršrutas* yra fizinis transportavimo iš kilmės į paskirties vietą kelias.</p> | **Kelionė**<p>*Kelionė* yra fizinis transportavimo iš kilmės į paskirties vietą kelias. Kiekvienas reisas turi būti priskirtas kelionei.</p> | |
| **Maršruto segmentai**<p>Maršrutas gali turėti kelis *maršruto segmentus*, kurių kiekvienas iš jų atspindi kelionės veiksmą. Į maršrutą gali būti įtraukti keli vežėjai arba paslaugos, kurių kiekvienas iš jų laikomas maršruto segmentu.</p> | **Atkarpos**<p>Kiekviena kelionė gali turėti kelias *atkarpas*, kurių kiekviena iš jų atspindi kelionės veiksmą. Atkarpa gali būti transportavimo, muito mokesčio tvarkymo ar kitos veiklos dalis.</p> | |
| **Konteineriai**<p>*Konteineris* gali būti bet kokios rūšies pakuotė ar pakavimas, naudojamas TMS.</p> | **Gabenimo konteineriai**<p>*Gabenimo konteineris* yra tikras, fizinis gabenimo konteineris, žinomas iš konteinerių siuntimo.</p> | |
| **Prekių kodai**<p>TMS (ir kitose „Supply Chain Management” vietose) *prekių kodai* nurodo prekių tipus. Jie gali paveikti tarifus, pavojingų medžiagų tvarkymą ir panašiai.</p> | **Prekių kodai**<p>Įkeltų išlaidų modulyje *prekių kodai* yra nustatomi juridiniu subjekto lygiu. Jie daugiausia naudojami ataskaitoms.</p> | Įkeltų išlaidų modulis taip pat gali naudoti prekių kodus, kuriuos naudoja TMS ir kitos „Supply Chain Management” vietos. Tačiau Įkeltų išlaidų prekių kodus naudoja tik Įkeltų išlaidų modulis. |

### <a name="some-reference-data-isnt-shared"></a>Kai kurie nuorodos duomenys nėra bendrinami

TMS ir Įkeltos išlaidos nebendrina nuorodos duomenų apie objektus, pavyzdžiui, išlaidų nustatymą, keliones ir atkarpas. Jei naudojate abu modulius, turite iš naujo sukurti nebendrintus nuorodos duomenis.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Vidinės įmonės ataskaitos neveikia kartu su tranzito prekėmis

Toliau pateiktos ataskaitos neveikia su tranzito prekių funkcija, kurią siūlo Įkeltų išlaidų modulis:

- [Bendro vidinės įmonės tranzito prekių kiekio ataskaita](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Bendro vidinės įmonės tranzito prekių kiekio ataskaita](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Šiose ataskaitose laikoma, kad prekės įdedamos į tranzitą iš kart išdavus pardavimo važtaraštį, ir kad jos iš tranzito nuvežamos į atsargas jas gavus. Tačiau tranzito prekės apdorojamos ne taip. Todėl, jei naudojate tranzito prekių ir vidinės įmonės funkcijas kartu, abiejų ataskaitų rezultatai bus neteisingi.

## <a name="using-the-two-modules-together"></a>Abiejų modulių naudojimas kartu

TMS galima naudoti tiek gavimo, tiek siuntimo operacijoms. Įkeltos išlaidos be tų pačių pagrindinių gavimo operacijų funkcijų, kurias turi ir TMS, turi ir keletą papildomų funkcijų. Todėl galbūt norėsite naudoti TMS siuntimo operacijoms, o Įkeltas išlaidas – gavimo operacijoms.

Apskritai, nerekomenduojame naudoti abiejų modulių gavimo operacijoms. Turėtumėte naudoti modulį, geriausiai atitinkantį jūsų poreikius. Jei naudosite kartu du modulius, turite nebendrinti šaltinio dokumentų tarp jų. Pavyzdžiui, nenaudokite to paties pirkimo užsakymo tiek TMS kroviniui, tiek reisui Įkeltų išlaidų modulyje. Visų pirma, turite užtikrinti, kad nenustatysite sistemos automatiškai kurti gautiems kroviniams. Jeigu pirkimo užsakymų prekės įtraukiamos į reisą, jų negalima tvarkyti kaip krovinio dalies.

## <a name="goods-in-transit"></a>Tranzito prekės

Viena iš pagrindinių Įkeltų išlaidų funkcijų yra galimybė apdoroti tranzito prekes. Tranzitų prekių apdorojimas leidžia jums perimti finansinę atsiųstų prekių nuosavybę, prieš gaunant jas fiziškai paskirties sandėlyje. Tranzito prekių apdorojimas dažniausiai reikalingas tarptautinei prekybai.

### <a name="tms-goods-in-transit-features"></a>TMS modulio tranzito prekių funkcijos

Šiuo metu TMS nepalaiko tranzito prekių apdorojimo.

### <a name="landed-cost-goods-in-transit-features"></a>Įkeltų išlaidų modulio tranzito prekių ypatybės

Tranzito prekių apdorojimas yra pagrindinė Įkeltų išlaidų ypatybė, suteikianti šias funkcijas:

- **Tranzito prekių sandėliai** – Tranzito prekių sandėlį galima susieti su kiekvienu „Supply Chain Management” sandėliu. Prekės yra pervežamos į tranzito prekių sandėlius po to, kai išrašoma pradinio pirkimo užsakymo sąskaita faktūra. Fiziškai rezervuotai prekės čia tampa negalimos suvartoti tol, kol jos nėra gautos jų fiziniame sandėlyje. Todėl išrašę pirkimo užsakymo sąskaitą faktūrą, galite perimti prekių finansinę nuosavybę.
- **Tranzito prekių didžiosios knygos paskyra** ‑ Įkeltų išlaidų modulis prie pirkimo užsakymo registravimo profilio prideda tam tikrą didžiosios knygos registravimo paskyrą, skirtą tranzito prekių apdorojimui. Ši tranzito prekių didžiosios knygos paskyra veikia kaip „prekėms išrašyta sąskaita faktūra, jos negautos” tipo paskyra. Kai išrašoma pradinio pirkimo užsakymo sąskaita faktūra ir sukuriamas tranzito prekių užsakymas, tiesioginio pirkimo užsakymo išlaidos užregistruojamos tranzito prekių didžiosios knygos paskyroje tol, kol prekės gaunamos galutinėje faktinėje vietoje.
- **Sekimo kontrolės atnaujinimai** – Tranzito prekių užsakymai palaiko sekimo kontrolės funkciją Įkeltų išlaidų modulyje. Sekimo kontrolė leidžia atnaujinti numatomą prekių gavimo datą prekėms būnant tranzite. Tada sekimo kontrolė atnaujina reisą ir susijusias pirkimo užsakymo eilutes. Tada numatoma pristatymo data galima bendrajam planavimui ir logistikai.
- **Perviršio/trūkumo operacijų suaktyvinimas** – Jeigu atsiranda nuokrypis tarp numatomų reiso linijos prekių ir faktiškai į sandėlį gautų prekių, Įkeltos išlaidos išsprendžia šią problemą sukurdamas perviršio/trūkumo operacijas. Tada galite tvarkyti šias operacijas, atsižvelgdami į tai, kaip norite jas apdoroti – per pirkimo užsakymą ar per judėjimo žurnalą. Perviršio ir trūkumo operacijos suteikia saitą atgal į reisą, pradinį pirkimo užsakymą ir naują judėjimo žurnalą, arba pirkimo užsakymą nuokrypiui.
- **Tranzito prekių užsakymai** – Įkeltos išlaidos pristato naują šaltinio dokumentą, žinomą kaip *tranzito prekių* užsakymą. Tranzito prekių užsakymas leidžia išrašyti sąskaitą faktūrą pradiniam pirkimo užsakymui, kad perimtumėte finansinę prekių nuosavybę. Kai išrašoma pirkimo užsakymo sąskaita faktūra, kiekvienai pirkimo užsakymo eilutei sukuriamas naujas šaltinio dokumentas, kuriame yra atsargų matmenų derinys. Tada prekės yra fiziškai perkeliamos į tranzito prekių sandėlį, kuriame jos fiziškai rezervuojamos pagal tranzito prekių užsakymą, ir prekės negali būti suvartojamos, nebent gaunami tranzito prekių užsakymai.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Papildomi mokesčiai ir siuntimo išlaidos

Vienas iš svarbiausių prekių siuntimo ir jo valdymo aspektų yra su siuntomis susijusių pridėtinių išlaidų atpažinimas. Šios pridėtinės išlaidos nėra tiesioginės atsargų išlaidos, susijusios su pirkimo užsakymu ir siunta arba reisu. Vietoj to, jos yra papildomos išlaidos, įvedamos dėl prekių judėjimo iš tiekėjo į jūsų organizaciją pobūdžio. Šias išlaidas gali apimti transportavimo mokesčio išlaidos, susijusios su prekių siuntimui iš vienos faktinės vietos į kitą, arba muito mokesčio išlaidos, susijusios su prekių importu iš užsienio tiekėjo.

Įkeltų išlaidų modulis tvarko šias išlaidas sukurdamas naują išlaidų struktūros tipą, vadinamą *automatinėmis išlaidomis*. TMS tvarko šias išlaidas naudodama papildomų išlaidų funkciją.

### <a name="tms-charge-and-cost-features"></a>TMS mokesčių ir išlaidų funkcijos

TMS naudoja papildomus mokesčius tvarkyti papildomoms krovinio išlaidoms, kurios yra paskirstytos susijusio šaltinio dokumento eilutėms. Šiuos papildomus mokesčius galima nustatyti tiek pirkimo užsakymo eilutės, tiek pirkimo užsakymo antraštės lygiu.

TMS modulyje papildomi mokesčiai gali būti paskirstyti arba padalinti pagal atsargų svorį, tūrį arba kiekį. Mokesčiai gali būti padalinti į transportavimo arba papildomų paslaugų mokesčius. Bus reikalingas tolimesnis vystymasis papildomų paskirstymo metodų naudojimui TMS modulyje.

### <a name="landed-cost-charge-and-cost-features"></a>Įkeltų išlaidų modulio mokesčių ir išlaidų funkcijos

Įkeltų išlaidų modulis suteikia išlaidų funkcijų rinkinį, kuris tvarko papildomas išlaidas, susijusias su prekių siuntimu. Šios išlaidos vadinamos automatinėmis išlaidomis ir yra taikomos pradinio siuntimo sąskaitos faktūros išrašymo metu naudojant įvertintos savikainos sumą. Kiekvienas išlaidų tipas yra valdomas jį registruojant. Užregistravus faktines papildomų išlaidų sąskaitas faktūras, įvertintos išlaidos automatiškai atnaujinamos, kad atspindėtų faktines išlaidas.

Be to, papildomoms išlaidoms, susijusioms su prekių siuntimui, gali būti išrašomos sąskaitos faktūros reiso iš kilmės uosto metu arba bet kuriuo metu gavus prekes. Ši galimybė suteikia daugiau lankstumo prekių suvartojimui.

Šiame sąraše apibrėžtos kai kurios Įkeltų išlaidų modulio mokesčių ir išlaidų funkcijų sąvokos:

- **Išlaidų sritis** – Išlaidos ir mokesčiai gali būti priskirti skirtingiems lygiams, arba *išlaidų sritims*, reise. Išlaidos gali būti taikomos reiso lygiu ir išskaidytos iki kiekvienos reiso prekės. Be to, išlaidos gali būti taikomos konteinerio, pirkimo užsakymo, prekės arba perkėlimo užsakymo lygiu. Kiekvieną išlaidų mokestį galima valdyti atskirai įvairiose srityse ir jis išskaidytas iki išlaidų vienai prekei.
- **Paskirstymo metodai** – Įkeltų išlaidų modulyje galimi keli paskirstymo metodai. Išlaidų mokesčius galima paskirstyti pagal kiekį, dolerių sumą, vertę, svorį, tūrį, matavimo vienetą arba vartotojo nustatytą tūrio matavimą.
- **Tarpusavio/nuokrypio kontrolė** – Išlaidų mokesčiai nustatyti kaip tam tikras išlaidų kodo tipas Įkeltų išlaidų modulyje. Kiekvienas išlaidų kodo tipas leidžia jums apibrėžti tarpuskaitos sąskaitą įvertintoms išlaidoms bei taip pat kaupimo ir pirkimo kainų nuokrypio sąskaitas, skirtas palyginti nuokrypiams tarp įvertintų ir faktinių išlaidų. Užregistravus įvertintas išlaidas į tarpuskaitos sąskaitą pervedamas kreditas. Užregistravus faktines sąskaitas faktūras, užregistruojamos faktinės išlaidos, o įvertintos išlaidos yra nurašomas iš tarpuskaitos sąskaitos.

## <a name="matching-freight-bills-and-invoices"></a>Transportavimo sąskaitų ir sąskaitų faktūrų gretinimas

### <a name="tms-bill-and-invoice-matching-features"></a>TMS sąskaitos ir sąskaitos faktūros gretinimo ypatybės

TMS gali sugretinti numatytas išlaidas apimančias transportavimo sąskaitas su sąskaitomis faktūromis, atspindinčiomis faktines transportavimo išlaidas. Sąskaitas faktūras galima gauti tiek elektroniniu būdu, tiek išspausdintas ant popieriaus. Įvertintų ir faktinių išlaidų gretinimo nuokrypis neturi įtakos atsargų vertinimui.

Daugiau informacijos rasite [Transportavimo mokesčių derinimas transportavimo valdyme](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Įkeltų išlaidų sąskaitos ir sąskaitos faktūros gretinimo ypatybės

Įkeltos išlaidos gali sugretinti transportavimo sąskaitas su įvertintų išlaidų mokesčiais ir gali išrašyti faktinių išlaidų mokesčių sąskaitą faktūrą įvertintoms išlaidoms. Sąskaitos faktūros išrašymo metu transportavimo mokesčiai yra sąskaitos faktūros žurnale, o įvertintos išlaidos išvalomos iš tarpuskaitos sąskaitos. Be to, faktinių išlaidų mokesčiai registruojami pagal parduotų prekių savikaina vienai prekei, kartu su nuokrypiais tarp įvertintų ir faktinių mokesčių. Dėl to sąskaitos faktūros išrašymo procesas yra lankstus.

## <a name="tracking"></a>Sekimas

Svarbi tiek TMS, tiek Įkeltų išlaidų ypatybė yra galimybė sekti prekes ir nustatyti, kur jos yra kelionės metu nuo pat kilmės vietos iki galutinio paskirties sandėlio. Sekimas leidžia sekti ir atnaujinti prekių buvimo vietą, bei kada jas tikimasi pristatyti į sandėlį suvartojimui. Papildomai prie prekių būsenos kelionės metu, Įkeltos išlaidos pateikia ir kiekvieno kelionės etapo numatytas ir faktines datas.

### <a name="tms-tracking-features"></a>TMS sekimo ypatybės

TMS modulis suteikia ribotas gaunamų krovinių sekimo funkcijas. Jis rodo datas ir leidžia kurti integravimą tikslių pozicijų suradimui (pavyzdžiui, **Transportavimo būsenos** puslapyje).

Kiekvienam maršruto segmentui galite įvesti numatomus grafikus ir pristatymo laikus.

### <a name="landed-cost-tracking-features"></a>Įkeltų išlaidų sekimo ypatybės

Įkeltos išlaidos siūlo sekimo kontrolę kiekvienam reisui nuo kilmės uosto iki galutinės paskirties vietos. Sekimo kontrolė nustato reiso būseną. Būsena nurodo, ar reisas keliauja, ar yra muitinėje patikrinimui, ar vietiniame pristatyme, kelyje į galutinį sandėlį. Būsena gali būti nustatyta pirkimo užsakymo eilutės, konteinerio ir reiso antraštės lygiais. Todėl jūs turite išsamesnę kontrolę.

Be to, nurodytais gamybos laikais pagrįsta data yra su susieta su kiekvienu kelionės etapu. Patvirtintos ir numatomos pristatymo datos yra pridėtos prie pirkimo užsakymo eilutės ir tranzito prekių užsakymų, ir gali būti naudojamos bendrajam planavimui ir logistikai. Be numatytų datų, galima atnaujinti faktines datas. Tolesni kelionės etapai tada bus taip pat atitinkamai atnaujinti.

## <a name="multi-leg-journeys"></a>Kelių atkarpų kelionės

Kelionės koncepcija nustato, kurioje proceso vietoje yra prekės, ir kontroliuoja prekių būseną tranzito metu. Prekės gali pereiti per kelias kelionės atkarpas ir galite susieti įvairias išlaidas su konkrečia atkarpa. Pavyzdžiai apima transportavimo išlaidas plaukiant laivu ir vietinio transporto išlaidas prekių transportavimui iš uosto į paskirties vietą.

### <a name="tms-multi-leg-journey-features"></a>TMS kelių atkarpų kelionės ypatybės

TMS modulyje maršrutai gali būti išskaidyti į maršruto segmentus kelių atkarpų kelionių atvaizdavimui. TMS gali paskirstyti vietos tarifus ir papildomų paslaugų mokesčius atskiriems maršruto segmentams.

Daugiau informacijos rasite [Planuokite transportavimo maršrutų su keliais sustojimais mokesčius](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Įkeltos savikainos kelių atkarpų kelionės ypatybės

Įkeltos išlaidos suteikia sistemą, leidžiančią perkelti prekes iš kilmės į paskirties vietą per daug atkarpų, kurios vadinasi sustojimais arba etapais kelionėje. Atkarpos yra sujungiamos žurnalų šablonų kūrimui, kurie apibrėžia, kaip prekės perkeliamos iš tiekėjo į jūsų organizaciją.

Kiekvienoje kelionės atkarpoje galite toliau nurodyti kiekvienos pirkimo užsakymo eilutės būseną ir su ja susijusius gamybos laikus. Bendras visų atkarpų gamybos laikas naudojamas numatytai pristatymo datai nustatyti. Tačiau kelių atkarpų kelionėse reikalaujama taikyti tranzito prekių apdorojimą. Prekių kelionė reise valdoma tik Įkeltų išlaidų moduliui būdingai lentelei.

## <a name="receiving-by-container"></a>Gavimas konteineriu

Gali būti svarbu valdyti, kaip prekės skaidomos ir saugomos transporto priemonėje. Transporto priemonėse prekes galima laikyti viename arba keliuose konteineriuose. Prekės yra gaunamos konteineriuose, o skirtingi to pačio reiso konteineriai gali būti gauti skirtingu laiku arba skirtingomis datomis.

Tiek TMS, tiek Įkeltos išlaidos suteikia funkcijas, skirtas tvarkyti prekių gavimą konteineriu. TMS naudoja krovinių koncepciją valdyti su gabenimo konteineriu susietoms prekėms, pirkimo ir perkėlimo užsakymams. TMS palaiko gavimą pagal pakavimo struktūrą, kuri gaunama pagal išankstinį siuntimo pranešimą (ASN). Įkeltos išlaidos naudoja gabenimo konteinerių koncepciją apdoroti pirkimo užsakymams ir valdyti pridėtinėms išlaidoms, susietoms su transporto priemonės konteineriu.

### <a name="tms-receiving-by-container-features"></a>TMS gavimo konteineriu ypatybės

TMS palaiko gaunamus ASN, visus gavimo per sandėlio valdymo mobiliųjų įrenginių programėlę variantus bei visus gavimo per „Supply Chain Management” klientą metodus.

### <a name="landed-cost-receiving-by-container-features"></a>Įkeltų išlaidų gavimo konteineriu ypatybės

Gavimo konteineriu palaikymui Įkeltos išlaidos sukuria gabenimo konteinerių įrašus ir susieja pirkimo užsakymus su konkrečiu gabenimo konteineriu naudojant to konteinerio ID. Pridėtinės išlaidos tada gali būti pritaikytos tam siuntimo konteineriui ir išskaidytos taip, kad jos būtų susietos su atitinkamais pirkimo užsakymais.

Konteinerius Įkeltose išlaidose galima gauti per naują gavimo tipą, vadinamą *tranzito prekių gavimu*, per pristatymo žurnalus arba per mobilųjį įrenginį. Naudojant gavimo žurnalus kiekiai gali būti inicijuoti iš tranzito prekių užsakymo arba pradinio pirkimo užsakymo eilučių konteineryje. Įkeltos išlaidos pateikia du darbo tipus, skirtus gavimui per sandėlio valdymo mobiliųjų įrenginių programėlę.

Įkeltų išlaidų modulyje nėra ASN, skirto elektroniniam prekių gavimo kvitui. Be to, jis nepalaiko sandėlio valdymo mobiliųjų įrenginių programėlė srautų, apdorojančių krovinio, numerio lentelės arba mišrios numerio lentelės gavimą.

## <a name="rate-shopping-by-vendor"></a>Tarifo analizė pagal tiekėją

Tarifo analizė įgalina įmonę pasirinkti transportavimo tiekėją pagal mažiausią kainą, greičiausią maršrutą arba abiejų aplinkybių derinį.

### <a name="tms-rate-shopping-features"></a>TMS tarifo analizės ypatybės

TMS leidžia nustatyti gaunamų ir siunčiamų užsakymų tiekėjo ir maršruto sprendimus. Pavyzdžiui, galite identifikuoti greičiausią maršrutą arba mažiausią siuntos kainą.

TMS suteikia pilną tarifo analizę ir transportavimo optimizavimą per tarifo maršruto darbo sritį, lanksčius tarifo pasirinkimus per tarifų mechanizmą, tarifų mechanizmo API integravimui su išorinėmis šalimis ir tūrinio svorio palaikymą.

Daugiau informacijos rasite [Transportavimo valdymo mechanizmai](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Įkeltų išlaidų tarifo analizės ypatybės

Įkeltos išlaidos teikia tik ribotą tarifo analizės pagal tiekėją palaikymą. Nors ir galite įvesti krovinių ekspeditorių reikšmes, Įkeltos išlaidos nepalygina jų tarp kelių tiekėjų.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Vairuotojo įregistravimas/išregistravimas su paskyrimo planavimu

Vairuotojo įsiregistravimo/išsiregistravimo funkcijos įgalina sistemą stebėti atvykimus ir išvengti grūsčių krovimo rampose.

### <a name="tms-driver-check-incheck-out-features"></a>TMS vairuotojo įsiregistravimo/išregistravimo funkcijos

TMS jums leidžia kurti *paskyrimus*. Paskyrimas reiškia įvykius, kurie įvyksta rampoje gaunant pirkimo užsakymą, siunčiant pardavimo užsakymą arba apdorojant gaunamą arba siunčiamą krovinį konkrečia data ir konkrečiu laiku. Paskyrimai užtikrina, kad rampos būtų laisvos norimu pakrovimo ir iškrovimo laiku, taip pat jos padeda išvengti situacijų, kai į vieną vietą tuo pačiu metu atvyksta keli vežėjai.

Sistema palaiko vairuotojų įsiregistravimo konkrečiose rampos duryse galimybę.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Įkeltų išlaidų vairuotojo įsiregistravimo/išregistravimo funkcijos

Įkeltos išlaidos gali saugoti numatomą konteinerio pristatymo datą ir laiką.

## <a name="transfer-orders-and-additional-costs"></a>Perkėlimo užsakymai ir papildomos išlaidos

Dažnai įmonės privalo turėti galimybę perkelti prekes tarp sandėlių. Kai įvyksta tokio tipo perkėlimas, reikalingos išlaidos ir jūs galbūt norėsite pažinti šias išlaidas. Įkeltų išlaidų modulyje perkėlimo užsakymai gali būti pridėti prie reiso ar transporto priemonės, kad būtų sekamas prekių judėjimas iš vieno sandėlio ar vienos jo vietos į kitą, įvertinamas pristatymo laikas ir numatyta pristatymo data bei įtrauktos prekių perkėlimo pridėtinės išlaidos.

### <a name="tms-transfer-order-cost-features"></a>TMS perkėlimo užsakymo išlaidų ypatybės

TMS palaiko su perkėlimais susijusių transportavimo mokesčių kūrimą. Nors šiuos mokesčius galima peržiūrėti perkėlimo užsakyme, įkeltos išlaidos nėra pridedamos prie prekės išlaidų. Transportavimo derinimas yra palaikomas kuriant transportavimo sąskaitą pagal šias išlaidas. Tada ši transportavimo sąskaita bus sugretinta su tiekėjo transportavimo sąskaita faktūra.

### <a name="landed-cost-transfer-order-cost-features"></a>Įkeltų išlaidų perkėlimo užsakymo išlaidų ypatybės

Įkeltos išlaidos leidžia jums įtraukti perkėlimo užsakymus į transporto priemonę arba reisą. Tokiu būdu perkėlimo užsakymo gavimo metu galite įtraukti siuntos išlaidas į reisą kaip atsargų sudengimus. Pridėtinėms išlaidoms gali būti išrašoma sąskaita faktūra faktinėms išlaidoms ir susekamos iki reiso atnaujinti parduotų prekių savikainai. Nors perkėlimo užsakymuose nenaudojamas tranzito prekių apdorojimas standartiniame leidime, jas taip pat galima įtraukti į reisus. Įkeltos išlaidos pridedamos prie bendrų kiekvienos prekės išlaidų.