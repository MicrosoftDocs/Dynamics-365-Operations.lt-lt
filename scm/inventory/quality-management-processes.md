---
title: "Kokybės valdymo procesai"
description: "Šiame straipsnyje pateikta informacija apie neatitinkančių produktų kokybės valdymo procesą. Aprašyta, kaip galite naudoti kokybės kontrolės funkciją, kaip nustatyti ir prižiūrėti neatitikimus ir kaip tvarkyti taisymus."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-10-30 12 - 53 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 2deec6d262e87daf4704ce21ce64546f9c9d638b
ms.lasthandoff: 03/30/2017


---

# <a name="quality-management-processes"></a>Kokybės valdymo procesai

Šiame straipsnyje pateikta informacija apie neatitinkančių produktų kokybės valdymo procesą. Aprašyta, kaip galite naudoti kokybės kontrolės funkciją, kaip nustatyti ir prižiūrėti neatitikimus ir kaip tvarkyti taisymus.

Kokybės užtikrinimas apima produktų bandymą ir neatitinkančių medžiagų valdymą. Kokybės valdymo procesai padeda užtikrinti aukštą produktų kokybę jūsų tiekimo grandinėje. Šie procesai taip pat padeda optimizuoti tiekimo grandinės procesus ir padidinti klientų pasitenkinimą. Kokybės valdymas gali padėti valdyti apgręžimo laiką, kai dirbate su neatitinkančiais produktais, neatsižvelgiant į jų kilmę. Diagnostikos rezultatus galite susieti su koregavimo užduotimis. Sistema gali planuoti užduotis turi išspręsti problemas, todėl padės išvengti šios problemos pasikartojimo ateityje. Kokybės valdymo taip pat leidžia jums sekti problemas (įskaitant vidaus problemų) iš problemos tipą, ir leidžia jums rasti sprendimus kaip trumpalaikiai arba ilgalaikiai. Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnes neatitikimo problemas ir sprendimus, kurie buvo taikomi joms taisyti. Galite naudoti praeities duomenis, kad būtų lengviau peržiūrėti anksčiau naudotų kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.

## <a name="controlling-the-quality-management-process"></a>Kokybės valdymo proceso kontroliavimas
Toliau pateikti keletas būdų, kaip galite kontroliuoti kokybės valdymo procesą.

-   Kurti kokybės užsakymus, paremtus aktyvinimo taškais, pvz., „gaunant produktus‟ (gavimo operacijomis) arba „paimant produktus‟ (siuntimo operacijoms).
-   Dokumentuoti bandymų rezultatus ir nustatyti, ar rezultatai atitinka nustatytus bandymų kriterijus ir priimtiną kokybės lygį.
-   Teikiant ataskaitas, tikrinimo proceso metu naudoti dokumentų valdymą, skirtą išsamioms produkto specifikacijoms ir konkrečių naudotojų pastaboms.
-   Prižiūrėti neatitinkančius produktus ir juos koreliuoti su papildoma neatitikimo informacija, kad būtų galima atsekti pradinę problemos priežastį.
-   Dokumentuoti neatitikimo valdymo išlaidas. Išlaidos gali būt prekės (pvz., atsarginės dalys), papildomos išlaidos ir tabelio valandos, kurių reikia norint ištaisyti neatitikimą.
-   Naudojant taisymų apdorojimą, kuris yra susijęs su kokybės užsakymais, planuoti klaidų taisymo procesus.

[![Kokybės valdymo proceso](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Produktų bandymai ir kokybės užsakymai
Produktų bandymai paprastai vadinami kokybės kontrole ir naudoja kokybės užsakymus. Naudodami kokybės kontrolės funkcijas, galite atlikti toliau nurodytus veiksmus.

-   Apibrėžti turimus atlikti medžiagos bandymus. Šie bandymai apima kokybės specifikacijas, naudojamą bandymo prietaisą, bandymą aprašančius dokumentus, pavyzdžių ėmimo planą ir priimtiną kokybės lygį (AQL).
-   Sukurti kokybės užsakymą, identifikuojantį bandymus, kurie turi būti atliekami tam tikram užsakymui, pvz., pirkimo arba gamybos užsakymui arba atsargų kiekiui. Kokybės užsakymą galite sukurti rankiniu būdu arba jį generuoti automatiškai, remiantis kokybės rekomendacijomis.
-   Apibrėžti kokybės rekomendacijas, kiekviename verslo procese susijusias su pirkimu, sulaikymu, gamyba arba pardavimo užsakymais, kad kokybės užsakymą, identifikuojantį bandymų reikalavimus gaunamoms arba išsiunčiamoms medžiagoms, būtų galima generuoti automatiškai.
-   Įrašyti bandymų rezultatus kokybės užsakyme, tikrinti bandymų rezultatus AQL atžvilgiu ir išspausdinti analizės sertifikatą, rodantį bandymų rezultatus.

## <a name="nonconformance"></a>Neatitikimas
A veiksmai neatitikties reikalavimams atveju aprašomas elementą, kuris turi kokybės problem.* * ** veiksmai neatitikties reikalavimams atveju procesas leidžia sukurti veiksmai neatitikties reikalavimams atveju užsakymas, nusakantis kiekis, netinkamų medžiagų, problemų šaltinis, problemos tipas ir aiškinamosios pastabos. Galima apibrėžti problemų tipų klasifikaciją, siekiant palengvinti neatitinkančios medžiagos analizę. Norėdami kreipti neatitinkančios medžiagos perdavimą, taip pat galite spausdinti neatitikimo žymę ir neatitikimo ataskaitą. Pavyzdžiui, žymė ir ataskaita gali nurodyti **Netinkamo naudoti** arba **Apriboto naudojimo** būklę. Toliau pateiktoje lentelėje išvardyti šeši numatytieji neatitikimo tipai ir aprašoma kiekvieno tipo informacija, kurią reikia įrašyti.

| Neatitikties tipas   | Šaltinio informacija                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Klientas              | Kliento sąskaitos numeris, pardavimo užsakymo numeris arba pardavimo užsakymo operacijos partijos numeris. Pavyzdžiui, neatitikimas gali būti susijęs su konkrečia pardavimo užsakymo siunta arba kliento grįžtamuoju ryšiu apie produkto kokybę.       |
| Aptarnavimo užklausa       | Kliento sąskaitos numeris, pardavimo užsakymo numeris arba pardavimo užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su konkrečia pardavimo užsakymo siunta arba su kliento nusiskundimu dėl prekės kokybės.     |
| Tiekėjas                | Tiekėjo sąskaitos numeris, pirkimo užsakymo numeris arba pirkimo užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su pirkimo užsakymo gavimu arba tiekėjo rūpesčiu dėl dalies, kurią jis tiekia. |
| Gamyba            | Gamybos užsakymo numeris arba gamybos užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su konkrečiu pagamintu paketu.                                                                      |
| Vidinis              | Kokybės užsakymo numeris arba kokybės užsakymo operacijos partijos numeris. Pvz., neatitikimas gali būti susijęs su bandymais, kurie atliekami kaip kokybės užsakymo dalis arba su darbuotojo rūpesčiu dėl produkto kokybės.     |
| Sudėtinio produkto gamyba | Sudėtinio produkto gamybos užsakymo neatitikimas, susijęs su paketinės gamybos užsakymais.                                                                                                                                                    |

Neatitikimai susieti su problemos tipu. Problemų tipai apibrėžiami puslapyje **Problemų tipai**, kuriame nurodote, kuriuos problemų tipus galima susieti su kiekvienu neatitikimo tipu. Pvz., problemų tipai dėl neatitikties, į **aptarnavimo užklausą** tipo gali atspindėti klientų skundus, klasifikaciją, kadangi problema tipus neatitikties, kad ** vidaus ** tipas gali kelti defektas kodų klasifikatorių. 

Kuriant naują neatitikimą, pasirenkamas neatitikimo tipas ir problemos tipas. Pradinė patvirtinimo būsena yra **Naujas**, kuri nurodo užklausą veikti. Kitas veiksmas yra patvirtinimo būseną pakeisti į **Patvirtinta** arba **Atsisakyta**, kad nurodytumėte, jog dėl neatitikimo veiksmų imsitės arba ne. Neatitikimą taip pat galite uždaryti (pasirinkdami atskirą žymės langelį), taip nurodydami, kad veiksmus su juo baigėte, arba neatitikimą galite atidaryti iš naujo, kad parodytumėte, jog jį reikia labiau apsvarstyti. 

Įvesti neatitikimo komentarus galite pridėdami dokumentą. Naudinga naudojant **Dokumento tipo** puslapį apibrėžti unikalų neatitiktimų dokumento tipą. Tada galite naudoti puslapį **Ataskaitos sąranka** ir apibrėžti, ar neatitikimo ataskaitoje ir neatitikimo žymėje turėtų būti spausdinami šio dokumento tipo komentarai. Atitikimo ataskaita ir neatitikimo žymė gali padėti atlikti medžiagų perdavimą. Pagal pasirinkimo kriterijus, kurie susieti su neatitikimu, galite selektyviai generuoti ataskaitas ir žymes. Šie kriterijai apima neatitikimo numerį, prekę, klientą, tiekėją ir būseną. 

Neatitikimo ataskaitoje rodomas neatitikimo numeris, prekė ir problemos tipas. Atsižvelgiant į jūsų ataskaitos sąrankos strategiją, ataskaitoje taip pat gali būti rodomos susijusios pastabos apie neatitikimą. Neatitikimo žymėje rodoma panaši informacija, ir ji taip pat apima sulaikymo zoną bei tipą (pvz., **Apriboto naudojimo** ar **Netinkamo naudoti**), kurį priskyrėte neatitikimui norėdami palengvinti brokuotų medžiagų perdavimą.

## <a name="approved-nonconformance"></a>Patvirtintas neatitikimas
Patvirtintai neatitikčiai galite pasirinktinai nurodyti vieną ar daugiau susijusių operacijų. Susijusi operacija apibūdina darbą, kurį turėtų atlikti, ir yra jūsų nustatytų kokybės operacijų sąrašą ir aprašomasis tekstas apie darbą priežastis. Neprivaloma: apibrėžę operaciją galite apibrėžti papildomas išlaidas, prekes ir tabelio darbo valandas, kurių reikia norint atlikti darbą. Rodomos apskaičiuotos susijusios operacijos išlaidos ir bendroji neatitikties išlaidų suma. Apskaičiuotos išlaidos ir pridėta išsami informacija (apie prekes, darbo valandas ir papildomas išlaidas) pateikiama kaip nuorodos informacija, ir jos naudojamos tik su kokybės valdymo funkcija. Neprivaloma: galite sukurti kokybės užsakymą pagal neatitikimą – pirmiausia atlikite kokybės užsakymų užklausą ir tada sukurkite naują kokybės užsakymą. Pvz., kokybės užsakyme gali būti identifikuotas poreikis bandyti (arba iš naujo bandyti) brokuotą medžiagą. Naujai sukurtame kokybės užsakyme rodomas saitas su pradiniu neatitikimu. Neprivaloma: galite susieti vieną neatitikimą su kitu ir sukurti naują neatitikimą iš esamo. Pvz., saitas gali atspindėti kokybės problemų tarpusavio ryšį.

## <a name="correction-handling"></a>Taisymų apdorojimas
**Taisymų** puslapyje galima sukurti neatitikimų, kuriuos reikia ištaisyti, sąrašą. Kiekvienas taisymo elementas yra susietas su diagnostikos tipu, dėl kurio aptikta problema. Į **pataisos** puslapyje taip pat yra informacijos apie tai, kas turi atlikti korekcinių veiksmų, ir kada. Jūs galite apibūdinti problemą ir taikytas korekcines priemones, reikalingas pridedant dokumentą prie pataisos detales. Neatitikimą apsvarsčius ar ištaisius, taisymo elementas „uždaromas‟ pasirenkant parinktį **Baigta**. Taip pat galite nurodyti, kad sprendimas buvo trumpalaikis. Naudinga naudojant **Dokumento tipo** puslapį apibrėžti unikalų taisymų dokumento tipą. Tada galite naudoti puslapį **Ataskaitos sąranka** ir apibrėžti, ar taisymo ataskaitoje spausdinami šio dokumento tipo komentarai. Išspausdintoje taisymo ataskaitoje rodoma informacija apie neatitikimą ir susijusios neatitikimo pastabos. Ataskaitoje taip pat pateikiama taisymo informacija, pvz., diagnostikos tipas ir susijusios taisymo pastabos.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kokybės valdymo įgalinimas](enable-quality-management.md)

[Neatitikimo valdymo įgalinimas](enable-nonconformance-management.md)

[Inventory blocking](inventory-blocking.md)

[Quarantine orders](quarantine-orders.md)

[Nustatyti kokybės užsakymų (darbo vadovas)](http://ax.help.dynamics.com/en/wiki/set-up-quality-orders/)

[Tikrinti kokybės prekių (darbo vadovas)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)


