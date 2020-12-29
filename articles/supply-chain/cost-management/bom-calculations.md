---
title: BOM skaičiavimai
description: Išlaidų susumavimas ir pardavimo kainos apskaičiavimas vadinamas komplektavimo specifikacijų (KS) skaičiavimais, kuriuos galite inicijuoti skaičiavimų puslapyje. Šioje temoje pateikiama informacija apie KS skaičiavimus.
author: AndersGirke
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: a718a2e825630ccfaa54ff9dece1d3d19d59018c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433797"
---
# <a name="bom-calculations"></a>BOM skaičiavimai

[!include [banner](../includes/banner.md)]

Išlaidų susumavimas ir pardavimo kainos apskaičiavimas vadinamas komplektavimo specifikacijų (KS) skaičiavimais, kuriuos galite inicijuoti skaičiavimų puslapyje. Šioje temoje pateikiama informacija apie KS skaičiavimus.

Išlaidų susumavimas ir pardavimo kainos apskaičiavimas vadinamas komplektavimo specifikacijų (KS) skaičiavimais, kuriuos galite inicijuoti puslapyje **Skaičiavimai**. Naudodami puslapį **Skaičiavimai** atlikite šias užduotis:

-   Apskaičiuokite pagamintos prekės išlaidas ir sugeneruokite susietos prekės išlaidų įrašą įkainojimo versijoje.
-   Apskaičiuokite pagamintos prekės pardavimo kainą ir sugeneruokite susietos prekės pardavimo kainos įrašą įkainojimo versijoje.

Puslapio **Skaičiavimai** naudojimo būdas gali skirtis ir priklauso nuo to, kaip inicijuojami KS skaičiavimai. Puslapio **Skaičiavimai** naudojimo būdas taip pat priklauso nuo to, ar KS skaičiavimai apima standartinių išlaidų arba planuojamų išlaidų įkainojimo versiją ir nuo kelių strategijų, nustatytų įkainojimo versijoje, kuri naudojama KS skaičiavimams. **Pastaba.** Puslapio **Skaičiavimai** nuokrypis naudojamas pardavimo užsakymo, pardavimo pasiūlymo arba aptarnavimo užsakymo eilutės elemento kontekste. Šie skaičiavimai vadinami specialaus užsakymo KS skaičiavimais. Specialaus užsakymo KS skaičiavimo metu įkainojimo versijoje nesugeneruojamas prekės išlaidų įrašas. Tokiu atveju generuojamas skaičiavimo įrašas, rodomas puslapyje **KS skaičiavimo informacija**. Skaičiavimo įraše yra apskaičiuotos išlaidos ir apskaičiuota pardavimo kaina. Puslapį **Skaičiavimai** galima inicijuoti vienai pagamintai prekei arba įkainojimo versijai:

-   Norėdami apskaičiuoti vienos pagamintos prekės išlaidas puslapyje **Prekės kaina** inicijuokite KS skaičiavimus. Perimamas puslapio **Skaičiavimai** prekės identifikatorius. Būtina nurodyti įkainojimo versiją, KS versiją, maršruto versiją, skaičiavimo kiekį, skaičiavimo datą ir teritoriją.
    -   Pagal numatytuosius nustatymus KS versijoje ir maršruto versijoje nustatomos aktyvios prekės, teritorijos, datos ir skaičiavimo kiekio versijos. Tačiau numatytųjų verčių galite nepaisyti, jei naudojate patvirtintas versijas.
    -   Pagal numatytuosius nustatymus skaičiavimo kiekis nustatomas kaip prekės standartinis užsakymo kiekis. Tačiau numatytosios vertės galite nepaisyti.
    -   Skaičiavimo datą ar teritoriją gali nustatyti įkainojimo versija arba galima nustatyti vartotojo nurodytas vertes, kai data arba teritorija nėra nustatytos įkainojimo versijoje. Skaičiavimo data ateityje nustato, kaip naudojami laukiamų išlaidų įrašai. KS skaičiavimams naudojamas laukiamų išlaidų įrašas su artimiausia pradžios data nuo ar prieš skaičiavimo datą.
-   Norėdami apskaičiuoti visų pagamintų prekių ar pasirinktų prekių išlaidas arba atnaujinti prekes pagal tai, kur naudota, puslapyje **Įkainojimo versijos nustatymas** arba **Įkainojimo versijos priežiūra** inicijuokite KS skaičiavimus. Perimama puslapio **Skaičiavimai** įkainojimo versija.
    -   Skaičiuojant laikoma, kad naudojama aktyvi pagamintos prekės (ir susijusios teritorijos, datos bei kiekio) KS versija ir maršruto versija, nebent pagamintas komponentas turi nurodytą subKS ar submaršrutą.
    -   Skaičiuojant laikoma, kad naudojamas pagamintų prekių standartinis užsakymo kiekis. Standartinis užsakymo kiekis yra komponentų kiekių skaičiavimo pagrindas nustatant tinkamas KS versijas ir maršrutų versijas (kai naudojate nuo kiekio priklausomas KS ir maršrutus) ir amortizuojant pastovias išlaidas. Tačiau, kai pagamintas komponentas turi KS eilutės tipą **Gamyba** arba **Tiekėjas**, arba kai KS skaičiavimams naudojate išskleidimo režimą paruošti užsakyti, ši prielaida netaikoma, nes kiekiai atspindi nurodytą apskaičiavimo kiekį.
    -   Skaičiavimo datą ar teritoriją gali nustatyti įkainojimo versija arba galima nustatyti vartotojo nurodytas vertes, kai data arba teritorija nėra nustatytos įkainojimo versijoje.

Kitos KS skaičiavimų variacijos atspindi įkainojimo tipą ir įkainojimo versijos apribojimus:

-   KS skaičiavimai, kurie naudoja standartines išlaidas, turi būti apriboti pagal įkainojimo versijos strategijas, nes apribojimai padeda užtikrinti, kad naudojami standartiniai įkainojimo principai. Standartiniai įkainojimo principai reikalauja apribojimų vykdymo dėl standartinių išlaidų naudojimo įsigytoms prekėms, vieno lygio išskleidimo režimo ir papildomų išlaidų įtraukimo į vieneto savikainą.
-   Atliekant KS skaičiavimus, kurie naudoja planuotas išlaidas, nebūtina laikytis standartinių įkainojimo principų. Šiems KS skaičiavimams galima naudoti įvairius išskleidimo režimus, alternatyvius įsigytų prekių išlaidų duomenų šaltinius ir įkainojimo versijoje nebūtina vykdyti apribojimų.

### <a name="bom-calculations-that-use-standard-costs"></a>KS skaičiavimai, kurie naudoja standartines išlaidas

Įkainojimo versijos strategijos (standartinių išlaidų) gali nustatyti penkių KS skaičiavimo strategijų vykdymą. Parinktis **Įrašymo apribojimas** įkainojimo versijoje nustato vieną iš šių strategijų, kur papildomos išlaidos turi būti įtrauktos į vieneto kainą. Papildomas įsigytų prekių išlaidas galima įvesti rankiniu būdu, tuo tarpu papildomos pagamintų prekių išlaidos atspindi apskaičiuotą pastovių išlaidų amortizaciją. Parinktis **Skaičiavimo apribojimas** įkainojimo versijoje nustato kitas keturias KS skaičiavimo strategijas:

-   Įsigytų prekių išlaidų įnašų šaltinis turi būti pagrįstas standartinėmis išlaidomis. Kitaip tariant, KS skaičiavimuose turi būti naudojami prekės išlaidų įrašai iš nurodytos įkainojimo versijos arba iš atsarginės versijos, kurioje yra standartinės išlaidos.
-   Išskleidimo režimas turi būti vieno lygio siekiant užtikrinti tikslų ir nuoseklų standartinių išlaidų apskaičiavimą.
-   Siekiant užtikrinti, kad skaičiuojant prekių pardavimo kainą būtų pasiekti nuoseklūs rezultatai, turi būti nustatytas pelno parametras. Naudoti pelno parametrą ir generuoti prekių pardavimo kainos įrašus galima tik tada, jei įkainojimo versija leidžia taikyti pardavimo kainų turinį.
-   Turi būti nustatyta atsarginė strategija. Galima nustatyti, kai strategijos **Nėra**, kai **Aktyvu** (aktyviems išlaidų įrašams) arba **Įkainojimo versija** (nurodytai įkainojimo versijai).

### <a name="bom-calculations-that-use-planned-costs"></a>KS skaičiavimai, kurie naudoja planuotas išlaidas

Įkainojimo versijos strategijos (planuotų išlaidų) gali pasirinktinai nustatyti penkių KS skaičiavimo strategijų vykdymą. Taip pat strategijos gali tik pateikti numatytąsias vertes. Parinktis **Įrašymo apribojimas** įkainojimo versijoje nustato, ar papildomų išlaidų KS skaičiavimo strategija bus nustatyta arba veiks kaip numatytoji vertė. Papildomas išlaidas galima pasirinktinai įtraukti į vieneto kainą. Parinktis **Skaičiavimo apribojimas** įkainojimo versijoje nustato, ar kitos keturios KS skaičiavimo strategijos bus nustatytos arba veiks kaip numatytosios vertės:

-   Įsigytos prekės išlaidų įnašų šaltinis gali būti prekės išlaidų įrašai įkainojimo versijoje. Taip pat šaltinis gali būti nustatytas pagal prekei priskirtą KS skaičiavimo grupę. Pavyzdžiui, KS skaičiavimo grupė gali nustatyti pirkimo kainos prekybos sutartis kaip išlaidų įnašo duomenų šaltinį.
-   Išskleidimo režimas gali būti vieno lygio, kelių lygių, gamybos pagal užsakymą arba pagrįstas KS prekės eilute. KS eilutės tipo išskleidimo režimas pakartoja gamybos užsakymo įvertinimo išlaidų skaičiavimo logiką.
-   Gali būti nustatytas pelno parametras arba tai gali būti numatytoji vertė. Naudoti pelno parametrą ir generuoti prekių pardavimo kainos įrašus galima tik tada, jei įkainojimo versija leidžia taikyti pardavimo kainų turinį.
-   Gali būti nustatytas atsarginis principas arba tai gali būti numatytoji vertė. Atsarginė strategija gali būti nustatyta, kai strategijos **Nėra**, kai **Aktyvu** (aktyviems išlaidų įrašams) arba **Įkainojimo versija** (nurodytai įkainojimo versijai).

KS skaičiavimai generuoja perspėjimo pranešimus ir kitų tipų pranešimus. Kelios KS skaičiavimo strategijos apibrėžia pranešimų tipus. Perspėjimo sąlygos nurodomos prekėms priskirtoje KS skaičiavimų grupėje. Tačiau pradėdami KS skaičiavimą šių perspėjimo sąlygų galite nepaisyti. Naudojant atsarginę strategiją naudinga atsarginę informaciją rodyti kaip informacinį pranešimą. Bandant atnaujinti apskaičiuotas išlaidas prekėms su trūkstamais išlaidų įrašais taip pat naudinga informaciniu pranešimu nustatyti prekes, kurios nebuvo atnaujintos.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>KS skaičiavimai, kurie naudoja atsarginį principą
Tokiose situacijose iliustruojami du atsarginio principo naudojimo būdus:

-   **Dviejų versijų būdo standartinių išlaidų atnaujinimai** − įkainojimo versijoje gali būti standartinių išlaidų pakeitimų didėjančia tvarka, tokių kaip laukiančių išlaidų įrašų, kurie nurodo naujas prekes arba išlaidų pokyčius. Šioje situacijoje atsarginis principas gali identifikuoti aktyvių standartinių išlaidų naudojimą, kuris yra kitose įkainojimo versijose.
-   **Išlaidų pokyčio poveikio modeliavimas naudojant suplanuotas išlaidas** – suplanuotų išlaidų įkainojimo versijoje modeliavimo tikslu gali būti pasikeitimų didėjančia tvarka. Į šią įkainojimo versiją bus įtraukti laukiančių išlaidų įrašai, kurie nurodo modeliuotų prekių išlaidų pakeitimus, išlaidų kategorijas ir netiesioginių išlaidų skaičiavimo formules. Šioje situacijoje atsarginis principas gali identifikuoti aktyvių standartinių išlaidų naudojimą, kuris yra kitose įkainojimo versijose.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Pasiūlytos pardavimo kainos KS skaičiavimas
Naudojant pagrįstų išlaidų antkainio metodą, apskaičiuota prekės pardavimo kaina atspindi pelno parametrų procentų rinkinį, kuris nurodomas KS skaičiavimui ir išlaidoms, susijusioms su savo komponentų prekėmis, maršruto operacijomis ir taikomais papildomais gamybos duomenimis. Antkainis atspindi pelno parametrų procentines dalis, kurios priskiriamos prie išlaidų grupių ir išlaidų grupių, kurios priskiriamos prekėms, maršruto operacijų išlaidų kategorijoms ir papildomų gamybos duomenų netiesioginių išlaidų skaičiavimo formulėms. Pelno parametrų procentų rinkiniai pažymėti kaip **Standartinis**, **1 pelnas**, **2 pelnas** ir **3 pelnas**. 1 pelno rinkinyje, pavyzdžiui, 50 proc. pelno parametrų gali būti nurodomi išlaidų grupei, kuri priskiriama įsigytoms medžiagoms, o 80 proc. pelno parametrų gali būti nurodomi išlaidų grupei, kuri priskiriama prie maršruto operacijų išlaidų kategorijoms. KS skaičiavimo kontekstas nurodo, kaip apdorojami suskaičiuotų pardavimo kainų rezultatai:

-   **Prekės ir nurodytos įkainojimo versijos KS skaičiavimas** – KS skaičiavimas įkainojimo versijoje generuoja laukiančios pardavimo kainos įrašą. Šis pardavimo kainos įrašas padeda peržiūrėti išsamią skaičiavimo informaciją (pavyzdžiui, puslapyje **Skaičiuoti prekės išlaidas**). Pardavimo kainos įrašas dažniausiai veikia kaip nuorodos informacija, tačiau jis nenaudojamas kaip pardavimo kainos ir pardavimo užsakymo pagrindas.
-   **Specialaus užsakymo KS skaičiavimas** – **KS** skaičiavimo puslapio nuokrypis naudojamas pardavimo užsakymo, pardavimo pasiūlymo arba aptarnavimo užsakymo eilutės elemento kontekste. Specialaus užsakymo KS skaičiavimo metu įkainojimo versijoje nesugeneruojamas įrašas. Tokiu atveju generuojamas skaičiavimo įrašas, rodomas puslapyje **KS skaičiavimo rezultatai**. Šis skaičiavimo įrašas padeda peržiūrėti išsamią skaičiavimo informaciją (pavyzdžiui, puslapyje **Skaičiuoti prekės išlaidas**). Informaciją apie pasirinktą skaičiavimo įrašą galima perkelti į pradinį eilutės elementą. Pavyzdžiui, apskaičiuotą pardavimo kainą galima perkelti į pardavimo užsakymo eilutės elementą.

## <a name="order-specific-bom-calculations"></a>Specialaus užsakymo KS skaičiavimai
Specialaus užsakymo KS skaičiavimas pristato KS skaičiavimo nuokrypį, reikalingą prekei pagaminti. Specialaus užsakymo KS skaičiavimas vykdomas pardavimo užsakymo, pardavimo pasiūlymo ar aptarnavimo užsakymo eilutės elemento kontekste. Specialaus užsakymo KS skaičiavimas generuoja skaičiavimo įrašą, rodomą puslapyje **KS skaičiavimo rezultatai**. Į skaičiavimo įrašą įtraukiamas apskaičiuotas svoris, pagal aktyvių išlaidų įrašus apskaičiuotas išlaidas ir apskaičiuotą pardavimo kainą. Kiekvienos prekės specialaus užsakymo KS skaičiavimas generuoja skaičiavimo įrašą puslapyje **KS skaičiavimo rezultatai** unikaliai nurodytu skaičiavimo numeriu. Skaičiavimo įrašo rezultatai gali būti pasirinktinai perkelti į kuriamos eilutės elementą. Specialaus užsakymo KS skaičiavimas skiriasi nuo KS skaičiavimo, reikalingo prekei pagaminti, todėl skaičiavimai atliekami dviem būdais:

-   Specialaus užsakymo KS skaičiavimo metu įkainojimo versijoje nesugeneruojamas prekės išlaidų įrašas. Todėl KS skaičiavimo strategijos netaikomos tada, kai sukuriamas arba perrašomas prekės išlaidų įrašas.
-   Specialaus užsakymo KS skaičiavimas visada naudoja aktyvių išlaidų įrašus, skirtus komponentų, išlaidų kategorijų ir netiesioginių išlaidų skaičiavimo formulėms.





