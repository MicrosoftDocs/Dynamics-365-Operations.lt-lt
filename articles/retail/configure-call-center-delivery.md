---
title: "Skambučių centro pristatymo būdų ir mokesčių konfigūravimas"
description: "Šioje temoje aprašoma, kaip nustatyti skambučių centro užsakymo pristatymo būdus ir su juo susijusius mokesčius „Microsoft Dynamics 365 for Retail“."
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: ebc8ee52da7d10ca18147684a0190e52a495ad5a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="configure-call-center-delivery-modes-and-charges"></a>Skambučių centro pristatymo būdų ir mokesčių konfigūravimas

[!INCLUDE [banner](includes/banner.md)]

Kai „Microsoft Dynamics 365 for Retail“ pateikiamas pardavimo užsakymas, priklausomai nuo to, ar asmuo, kuris įvedė pardavimo užsakymą, yra susietas su skambučių centru, ar ne, pristatymo būdui patikrinti (pristatymo būdas) ir užsakymo mokesčiams apskaičiuoti gali būti naudojamas kanalas, logika ir taisyklės.

Kai kuriate pardavimo užsakymą, pristatymo būdą galite pasirinkti pardavimo užsakymo antraštėje ir pardavimo užsakymo eilutėse. Pagal numatytuosius parametrus, antraštėje pasirinktas pristatymo būdas naudojamas visoms pardavimo užsakymo eilutėms. Tačiau atskirų pardavimų eilutėse, jei reikia, numatytąjį pristatymo būdą galite perrašyti. Pristatymo būdą taip pat galite apibrėžti kliento įraše. Tada sukūrus kliento užsakymų, apibrėžtas pristatymo būdas pagal numatytuosius parametrus naudojamas pardavimo užsakymo eilutėje.

„Retail“ pateikiama funkcijų, leidžiančių vartotojams apriboti pristatymo būdus, kuriuos galima naudoti pagal kanalą, pristatymo būdus, kuriuos galima naudoti produktui, ir pristatymo būdus, tinkamus konkrečioms siuntos paskirties vietoms. Išlaidas galima apibrėžti taip, kad į kliento užsakymą būtų įtraukti papildomi mokesčiai, priklausantys nuo pristatymo būdų, kurie pasirenkami pagal pardavimo užsakymo ir bendrą užsakymo vertę.

## <a name="define-delivery-modes"></a>Pristatymo būdų apibrėžimas

Prieš nurodydami, kokius pristatymo būdus galima naudoti skambučių centro užsakymams, ir apibrėždami susijusias taisykles bei mokesčius, turite apibrėžti pristatymo būdus. Eikite į parinktį **Pardavimas ir rinkodara \> Sąranka \> Platinimas \> Pristatymo būdai**. Pasirinkite **Naujas** ir sukurkite naują pristatymo būdą. Taip pat iš sąrašo galite pasirinkti esamą pristatymo būdą ir, pasirinkę **Redaguoti**, atlikti keitimų.

Lauke **Pristatymo būdas**, priklausomai nuo verslo reikalavimų, galite įvesti bet kokį skaitinių ir raidinių simbolių derinį. Tada galite naudoti lauką **Aprašas** ir pateikti papildomo konteksto. Laukai **Išlaidų grupė** ir **Pagreitinimas** yra pasirinktiniai ir apie juos bus išsamiau paaiškinta vėliau šioje temoje.

Į „FastTab“ skirtuką **Mažmeninės prekybos kanalai** įtraukite bet kokį mažmeninės prekybos kanalą, kuriame norite, kad būtų leista naudoti pristatymo būdą, kai sukuriama pardavimo operacijų.

„FastTab“ skirtuke **Produktai** galite nurodyti, kuriems produktams ir (arba) produktų kategorijoms pristatymo būdą galima ir kurioms negalima taikyti. Pvz., jei produkto negalima siųsti oru dėl pavojingai medžiagai (pavojinga medžiaga) taikomų apribojimų, įsitikinkite, kad produkto arba produktų kategorija neįtraukiama į visus pristatymo būdus, susijusius su oro transportu.

„FastTab“ skirtuke **Adresai** galite nurodyti, kuriose šalyse arba regionuose ar valstijose pristatymo būdą galima ir kuriose negalima taikyti. Pavyzdžiui, į Havajus arba Aliaską siunčiamų užsakymų negalima pristatyti antžeminiu transportu. Dėl šios priežasties minėtas valstijas reikia pašalinti iš pristatymo būdo, susieto su pristatymo antžeminiu transportu paslauga, bet įtraukti į pristatymo būdą, susietą su pristatymo oru paslauga.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Pristatymo būdų, skirtų užsakymams per skambučių centrą, tikrinimas

Apibrėžę pristatymo būdus, turite vykdyti paketinį vykdymą **Apdoroti pristatymo būdus**. Atliekant šią užduotį pristatymo būdai padaromi pasiekiamais, kad juos būtų galima naudoti mažmeninės prekybos kanalų pardavimo užsakymo procesuose. Norėdami pradėti vykdyti užduotį **Apdoroti pristatymo būdus**, eikite į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> Apdoroti pristatymo būdus**. Šią užduotį reikia vykdyti bet kuriuo metu, kai į mažmeninės prekybos kanalą įtraukiami nauji pristatymo būdai arba atliekami esamo pristatymo būdo / kanalo ryšių keitimai.

Pradėję vykdyti paketinę užduotį **Apdoroti pristatymo būdus** galite eiti į parinktį **Mažmeninė prekyba \> Kanalai \> Skambučių centrai \> Visi skambučių centrai**. Puslapio **Visų skambučių centrai** veiksmų srityje, skirtuke **Nustatymas** pasirinkite **Pristatymo būdai**. Puslapyje **Pristatymo būdai** bus pateikti visi pasirinktam skambučių centro kanalui tinkami pristatymo būdai. Norėdami redaguoti esamus pristatymo būdus ar įtraukti naujų, pasirinkite **Valdyti pristatymo būdus**. Atkreipkite dėmesį, kad užduotį **Apdoroti pristatymo būdus** reikia vykdyti visada, kai atliekama keitimų.

## <a name="define-charges-for-delivery-services"></a>Išlaidų už pristatymo paslaugas apibrėžimas

Klientams sukūrus pardavimo užsakymų gali būti, kad įmonė norės įtraukti išlaidas, automatiškai apskaičiuojamas pagal pasirinktus užsakymo pristatymo būdus. Šios išlaidos gali būti sukonfigūruotos taip, kad nepriklausomai nuo kliento ir pristatymo būdo būtų vienodos. Taip pat išlaidos gali skirtis priklausomai nuo kliento ir (arba) pardavimo užsakymui parinktų pristatymo būdų.

Norėdami apibrėžti išlaidas, eikite į **Mažmeninė prekyba \> Kanalo sąranka \> Išlaidos \> Automatinės išlaidos**. Pasirinkite **Naujos** ir įtraukite naujų išlaidų. Taip pat galite pasirinkite esamą įrašą, tada – **Redaguoti**.

Išlaidas galima apibrėžti taip, kad jos būtų skaičiuojamos užsakymo antraštės arba užsakymo eilučių lygiu. Pasinaudokite lauku **Lygis** ir pasirinkite pageidaujamą lygį.

Galima apibrėžti konkretaus kliento, klientų grupės arba visų klientų išlaidas. Lauke **Sąskaitos kodas** pasirinkite **Lentelė** ir apibrėžkite išlaidas, taikytinas tik konkrečiam klientui. Pasirinkite **Grupė** ir apibrėžkite konkrečiai klientų grupei taikytinas išlaidas. Pasirinkite **Visi** ir išlaidas taikykite kiekvienam klientui, pateikiančiam pardavimo užsakymą su susijusiu pristatymo būdu. Jei parinktis **Lentelė** arba **Grupė** pasirinkote lauke **Sąskaitos kodas**, lauke **Sąskaitos ryšys** pasirinkite klientą arba klientų grupę.

Išlaidas galima sukonfigūruoti taip, kad jos būtų taikomos konkrečiam pristatymo būdui, pristatymo būdo grupei ar visiems pristatymo būdams. Jei parinktį **Lentelė** pasirinkote lauke **Pristatymo kodo režimas**, lauke **Pristatymo būdo ryšys** turite pasirinkti konkretų pristatymo būdą. Jei pasirinkote **Grupė**, lauke **Pristatymo būdo ryšys** turite pasirinkti pristatymo būdų grupę. Pristatymo būdo grupes galima apibrėžti parinktyje **Mažmeninė prekyba \> Kanalo sąranka \> Išlaidos \> Pristatymo išlaidų grupė**. Tada grupes puslapyje **Pristatymo būdas** galima susieti vienu ar keliais pristatymo būdais. Jei apibrėžę išlaidas pasirinksite grupę, bet kokiam su pasirinkta pristatymo grupe susietam pristatymo būdui bus taikomos nurodytos išlaidos. Galiausiai, jei parinktį **Visi** pasirinkite lauke **Pristatymo kodo režimas**, išlaidos bus taikomos visiems pristatymo būdams. Todėl lauke **Pristatymo būdo ryšys** nepasirinkite jokios reikšmės.

Skyriuje **Eilutės**, jei reikia, vieną ar kelias išlaidų sumas galite apibrėžti pagal valiutą. Išlaidos turi būti susietos su išlaidų kodu, kuriuo apibrėžiamos su išlaidomis susiję finansų registravimo taisyklės. Laukas **Kategorija** naudojamas norint apibrėžti, kaip skaičiuojamos išlaidos. Pvz., jei klientams turi būti taikomas fiksuotas 9,95 USD išlaidų tarifas, kad užsakymą būtų galima išsiųsti taikant konkretų pristatymo būdą, naudokite kategoriją **Fiksuotas**. Jei įmonė nusprendžia apmokestinti klientus procentine dalimi nuo bendros užsakymo sumos, kad padengtų pristatymo išlaidas, naudokite kategoriją **Procentas**. Faktinės klientams tenkančios išlaidos apibrėžiamos lauke **Išlaidų vertė**.

Mažmeninės prekybos įmonės dažnai konfigūruoja pakopines išlaidas. Tokiu atveju suma, kurią, klientai sumoka už pristatymą, priklauso nuo užsakymo vertės. Norėdami sukonfigūruoti pakopines išlaidas, laukuose **Suma Nuo** ir **Suma Iki** įveskite reikšmes, o lauke **Išlaidų vertė** apibrėžkite pačią vertę. Pvz., užsakymų, kurių vertė mažesnė nei 50 USD, atveju, mažmenininkas už siuntas antžeminiu transportu taikys 5,95 USD mokestį. Užsakymų, kurių vertė lygi 50 USD arba yra didesnė, bet mažesnė nei 100 USD, atveju, mažmenininkas taikys 7,95 USD mokestį. Galiausiai, užsakymų, kurių vertė lygi 50 USD arba yra didesnė, bet mažesnė nei 100 USD, atveju, mažmenininkas netaikys siuntimo mokesčio. Toliau pateiktoje iliustracijoje pavaizduota šių išlaidų konfigūracija.

![Fiksuotų pakopinių išlaidų pavyzdys](media/fixedtieredcharges.png)

Išlaidoms, priklausomai nuo jūsų verslo poreikių, galite taikyti mišrias kategorijas. Pvz., visų užsakymų, kurių vertė mažesnė nei 100 USD, atveju, yra taikomas fiksuotas 9,95 USD mokestis už siuntimą. Tada užsakymų, kurių vertė yra lygi 100 USD arba yra didesnė, pristatymo mokesčiai apskaičiuojami taikant 5 proc. tarifą nuo užsakymo vertės. Toliau pateiktoje iliustracijoje pavaizduota šių išlaidų konfigūracija.

![Mišrių pakopinių išlaidų pavyzdys](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Pristatymo būdų taikymas atliekant užsakymą skambučių centre

Sukūrus naują pardavimo užsakymą, vertę reikia nurodyti lauke **Pristatymo būdas**, kuris pateiktas pardavimo užsakymo antraštės „FastTab“ skirtuke **Pristatymas**. Šis laukas, priklausomai nuo kliento įrašo numatytųjų reikšmių, gali būti užpildytas automatiškai.

Užsakymo antraštėje apibrėžtas pristatymo būdas automatiškai nukopijuojamas į pardavimo užsakymo eilutes, kai tik jos sukuriamos. Tačiau konkrečioje eilutėje nurodytos prekės pristatymo būdą galite pakeisti skirtuke **Pristatymas**, kuris pateiktas pardavimo užsakymo įvedimo skyriuje **Eilutės informacija**.

Jei pasirinktas produkto pristatymo būdas arba nurodytas užsakymo arba užsakymo eilutės pristatymo adresas yra netinkamas, bus parodytas klaidos pranešimas. Tada turėsite pasirinkti pristatymo būdą, apibrėžtą norint palaikyti to produkto ar adreso konfigūraciją.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Pristatymo išlaidų apskaičiavimas atliekant užsakymo įvedimą

Jei parametras **Įgalinti užsakymo baigimą** jūsų skambučių centro kanale yra įjungtas, pardavimo užsakymų siuntimo išlaidos apskaičiuojamos automatiškai, kai vartotojai pasirenka **Atlikta**. Puslapio **Pardavimo užsakymo suvestinė** viršuje pateikiamas šis pranešimas: „Pakopinės išlaidos apskaičiuotos“. Apskaičiuotos išlaidos įtraukiamos į lauke **Bendroji pardavimo suma** nurodytą reikšmę. „FastTab“ skirtuko **Suma** lauke **Išlaidos** pateikiama bendra visų išlaidų, apskaičiuotų užsakymui ir eilutėms, suma. Norėdami pamatyti išsamesnę informaciją apie paskirstymą, pasirinkite parinktį **Užsakymas**, pateikiamą puslapyje **Pardavimo užsakymo suvestinė**, tada pasirinkite parinktį **Išlaidos**, kad peržiūrėtumėte, įtrauktumėte arba redaguotumėte išlaidas. Atkreipkite dėmesį, kad pristatymo išlaidų apskaičiavimo metodas užsakymo antraštėje priklauso nuo pristatymo būdo, susieto su antrašte. Eilutės lygio išlaidos už pristatymą apskaičiuojamos atsižvelgus į pristatymo būdą, sukonfigūruotą pardavimo eilutei. Jei skirtingose eilutėse naudojama keletas pristatymo būdų, gali būti taikoma ir kartu įtraukiama keletas mokesčių. Tokiu atveju bendra suma bus nurodyta lauke **Išlaidos**, kuris pateiktas puslapyje **Pardavimo užsakymo suvestinė**.

Jei parametras **Įgalinti užsakymo baigimą** išjungtas, vartotojai turi rankiniu būdu paleisti išlaidų apskaičiavimo funkciją. Puslapio **Pardavimo užsakymas** veiksmų srities skirtuke **Pardavimas**, grupėje **Skaičiuoti** pasirinkite **Pakopinės išlaidos**. Bus rodomas pranešimas „Pakopinės išlaidos apskaičiuotos“. Tada galite pasirinkti parinktį **Išlaidos**, pateiktą skirtuke **Pardavimas**, kad peržiūrėtumėte, redaguotumėte arba panaikintumėte apskaičiuotas išlaidas.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Pagreitintojo pristatymo būdų naudojimas skambučių centro užsakymams

Pagreitinimo kodą su bet kokiu sukonfigūruotu pristatymo būdu galite susieti pasirinktinai. Šis kodas naudojamas kaip prioritetų nustatymo ir ataskaitų kūrimo įrankis. Naudojant kodą papildomi mokesčiai užsakymui šiuo metu nėra taikytini. Norėdami nustatyti pagreitinimo kodus, eikite į parinktį **Pardavimas ir rinkodara \> Sąranka \> Paskirstymas \> Pagreitinimo kodai**.

Pvz., užsakymų, kurie kitą dieną bus išsiųsti oru, atveju, paėmimą sandėlyje reikia atlikti kasdien iki 13 val. Tokiu atveju pagreitinimo kodą sukurti galima ir jis bus susietas su bet kuriuo pristatymo kitą dieną būdu, sukonfigūruotu sistemoje. Kai sandėlyje sukuriama išrinkimo banga, atitinkamą pagreitinimo kodą, nurodytą lauke **Pagreitinimas**, galima naudoti kaip filtrą, kad išrinkimas būtų vykdomas tik tiems užsakymams, kurių pristatymo būdai susieti su tuo kodu.

Be to, įvedus skambučių centro užsakymą, pagreitinimo kodą galima rankiniu būdu taikyti pardavimo užsakymo antraštei arba atskirai pardavimo užsakymo eilutei. Taip pat kodą galima naudoti rūšiavimo arba ataskaitų kūrimo tikslais. Kartais užsakymą reikia apdoroti kruopščiai dėl iškilusios klientų aptarnavimo tarnybos problemos. Tokiu atveju užsakymo antraštei arba eilutėms galima taikyti konkretų pagreitinimo kodą, kad vykdymo proceso metu užsakymas būtų greičiau identifikuotas ir greičiau nustatyti jo prioritetai.

