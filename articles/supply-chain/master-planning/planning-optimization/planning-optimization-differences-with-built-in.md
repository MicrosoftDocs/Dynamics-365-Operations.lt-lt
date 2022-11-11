---
title: Skirtumai tarp planavimo optimizavimo ir pasenusio bendrojo planavimo modulio
description: Šiame straipsnyje pateikiamos funkcijos, kurių planavimo optimizavimas dar nepalaiko ir kurių nėra planavimo optimizavimo analizės puslapyje.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745367"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Skirtumai tarp planavimo optimizavimo ir pasenusio bendrojo planavimo modulio

[!include [banner](../../includes/banner.md)]

Planavimo optimizavimo rezultatai gali skirtis nuo pasenusio bendrojo planavimo modulio rezultatų. Skirtumus gali sukelti laukimo funkcijos. Šiame straipsnyje pateikiamos funkcijos, kurių planavimo optimizavimas dar nepalaiko ir kurių nėra planavimo optimizavimo **[analizės puslapyje](planning-optimization-fit-analysis.md)**.

| Funkcija | Dabartinė „Planning Optimization“ elgsena |
|---|---|
| Esamo svorio produktai | Esamo svorio produktai laikomi įprastais produktais.|
| Extensible dimensijos | Planavimo optimizavimas nepalaiko extensible dimensijų. Naudojant planavimo optimizavimą, suplanuotuose užsakymuose extensible dimensijos yra tuščios, **·** **·** **net jei saugojimo dimensijų grupių arba sekimo dimensijų grupių puslapyje pažymėtas žymės langelis Padengimo planas pagal dimensiją.** |
| Filtruoti gamybos vykdymai | Daugiau informacijos ieškokite [Gamybos planavimas – Filtrai](production-planning.md#filters). |
| Prognozės planavimas | Prognozės planavimas nepalaikomas. Patariame naudoti bendrąjį planavimą, kai prognozės modelis priskiriamas prie bendrojo plano. |
| Suplanuotų užsakymų sekų skaičius | Suplanuotų užsakymų numeracijos nepalaikomos. Suplanuotų užsakymų numeriai generuojami aptarnavimo pusėje. Suplanuoto užsakymo numeris paprastai rodomas 10 skaitmenų, bet iš tikrųjų jį sudaro 20 simbolių, planavimo vykdymo skaičiui priskirta 10 skaitmenų ir kiti 10 suplanuotų užsakymų skaičiavimo skaitmenų. |
| Planuoti kopijavimą, naikinti planą ir plano versijos valymą | <p>Šie elementai išjungti bendrojo planavimo **bendrojo planavimo \> tvarkymo planuose \> naršymo srityje**:</p><ul><li>Plano kopija</li><li>Naikinti planą</li><li>Plano versijos valymas</li></ul> |
| Grąžinimo užsakymai | Grąžinimo užsakymų nelaikomos. |
| Susijusių funkcijų planavimas | Daugiau informacijos žr. [Planavimas, naudojant neribotą pajėgumą](infinite-capacity-planning.md#limitations). |
| Saugos atsargų pildymas | Planavimo optimizavimas visada naudoja *Šiandienos data + įsigijimo laikas* parinktį, skirtą **Įvykdyti minimalų poreikį** laukui, esančiam **Prekės padengimo** puslapyje. Tai padeda sustabdyti nenorimus suplanuotus užsakymus ir kitas problemas, nes jeigu įsigijimo laikas neįtrauktas į saugos atsargas, suplanuoti užsakymai, sukurti dabartinėms mažoms turimoms atsargos, visada bus atidėti dėl gamybos laiko. |
| Saugos atsargų iškvietimas ir grynieji poreikiai | *Saugos atsargų* reikalavimo tipas nėra įtrauktas ir nėra rodomas **Grynųjų poreikių** puslapyje. Saugos atsargos neatspindi poreikio ir neturi su juo susietos poreikio datos. Vietoj to jis nustato apribojimą, kiek atsargų visada turi būti pasiekiama. Tačiau vis dar atsižvelgiama į lauko **Mažiausia** reikšmę apskaičiuojant suplanuotus užsakymus bendrojo planavimo metu. Rekomenduojame patikrinti **Sukauptas kiekis** stulpelį, esantį **Grynųjų poreikių** puslapyje, kad pamatytumėte, jog į šią reikšmę buvo atsižvelgta. Kadangi iškvietimas skiriasi, galima pasiūlyti skirtingus veiksmus. |
| Transportavimo kalendoriai | Pristatymo būdų puslapio **Transportavimo kalendorius** stulpelio **vertė ignoruojama**. |
| Min. / maks. padengimo kodas be verčių| Naudojant pasenusią bendrojo planavimo sistemą, kai naudojate min. / maks. padengimo kodą, kuriame nustatytos minimalios ar maksimalios vertės, planavimo variklis padengimo kodą laiko reikalavimu ir kiekvienam poreikiui sukuria vieną užsakymą. Sistema sukurs vieną užsakymą per dieną planavimo optimizavimui padengti visą tos dienos sumą.  |
| Grynieji reikalavimai ir rankiniu būdu sukurti suplanuoti užsakymai | Naudojant pasenusią bendrojo planavimo sistemą, rankiniu būdu sukurti prekės tiekimo užsakymai automatiškai rodomi tarp grynųjų tos prekės poreikių. Pavyzdžiui, kuriant pirkimo užsakymą iš pardavimo užsakymo, **pirkimo užsakymas rodomas grynųjų poreikių** puslapyje nereikalaujant jokių ankstesnių veiksmų. Taip yra todėl, kad pasenusi bendrojo planavimo sistema lentelėje registruoja atsargų operacijas `inventLogTTS`**ir rodo pakeitimus dinaminių planų grynųjų** poreikių puslapyje. Tačiau planavimo optimizavimo atveju rankiniu būdu sukurti užsakymai nebus rodomi tarp grynųjų prekės poreikių, kol bus paleistas planavimo optimizavimas (naudojant planą, kuriame yra prekė) **\>** **arba** kol grynųjų poreikių puslapyje veiksmų srityje nebus įtrauktas bendrasis planavimas, kuris galėsite vykdyti prekės bendrąjį planavimą. Daugiau informacijos apie tai, kaip dirbti su grynųjų **poreikių puslapiu**, žr. grynuosius [reikalavimus ir iškvietimo informaciją](net-requirements.md). |
| Išteklių priskyrimas | Dirbant su neribotu pajėgumu, pasenusias bendrojo planavimo modulis priskiria visus suplanuotus užsakymus tam pačiam ištekliui duotoje išteklių grupėje. Planavimo optimizavimas pagerina šį procesą, pasirinkdami išteklius atsitiktine tvarka, kad skirtingi gamybos užsakymai galėtų naudoti skirtingus išteklius. Jei visiems suplanuotams užsakymams norite naudoti tą patį išteklių, turite nurodyti tą maršruto išteklių. |
| Išplėsti duomenų tipai (EDT) | Planavimo optimizavimas nepalaiko EDT tikslumo pakeitimų. Tai reiškia, kad šis procesas nėra oficialiai palaikomas ir nėra garantuoti, kad jis bus veikiamas. |
| Saugos atsargų pildymas | Planavimo optimizavimas visada naudoja **šiandienos** *datos įvykdyma + įsigijimo laikas*. Taip sistema paruošia ateityje naudoti supaprastintą planavimo nustatymą ir pateikti veiksmui bingusį rezultatą. Jei įsigijimo laikas neįtrauktas į pakankamai atsargų, suplanuoti užsakymai, sukurti turimose atsargose, visada bus atidėti dėl gamybos laiko. Tai gali sukelti daug triukšmo ir nepageidaujamų suplanuotų užsakymų. Geriausia pakeisti parametrą, kad būtų galima naudoti šiandienos *datą + įsigijimo laiką*. Atnaujinti bendruosius duomenis, kad būtų išvengta įspėjimų. |
| Kopijuoti statinį į dinaminį planą | Planavimo optimizavimas nekopijuos statinių planų į dinaminius planus, nepaisant bendrojo planavimo **parametrų puslapyje nurodytų** parametrų. Apskritai, ši operacija yra ne tokia svarbi dėl spartos ir visiško planavimo optimizavimo proceso. Jei naudojami du ar daugiau planų, turėtų būti suaktyvintas kiekvieno plano bendrasis planavimas. |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)
- [Planavimo optimizavimo nenaudojami parametrai](not-used-parameters.md)
- [Datos ir laiko parametrai, naudojami „Planning Optimization“](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
