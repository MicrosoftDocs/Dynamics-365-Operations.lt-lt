---
title: Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms
description: Šiame straipsnyje aprašomos papildomos automatinio apmokestinimo skaičiavimo ir taikymo "Commerce" kanalų užsakymams galimybės naudojant išplėstinę automatinio mokesčio funkciją.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6b41aa7b012b161626a98fc4aa2d37134552a57a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886937"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms


[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomos automatinio antraštės lygio mokesčių grupavimo ir jų skelbimo komercijos pardavimo eilutėms funkcijos. Ši funkcija yra skirta operacijoms, kurios sukurtos elektroniniame kasos aparate (EKA) naudojant „Retail“ 10.0.1 versiją ir pardavimo operacijoms, kurios sukurtos skambučių centre naudojant „Retail“ 10.0.2 versiją.

Ši funkcija galima tik tuo atveju, jei įjungta funkcija [Išplėstinės automatinės išlaidos](/dynamics365/unified-operations/retail/omni-auto-charges) ir naudojama puslapyje **Prekybos parametrai** esanti parinktis. Be to, patobulintas automatinis apskaičiavimo metodas gali būti taikomas tik pardavimo užsakymams, kurie sukuriami per „Commerce“ kanalus (EKA, skambučių centrą ir „e-Commerce“ platformą „Dynamics“).

Ši nauja funkcija suteikia organizacijoms daugiau lankstumo apskaičiuojant automatinį apmokestinimą antraščių lygiu ir jį taikant pardavimo sandoriams.

Ankstesnėse nei 10.0.1 programos versijose antraštės lygio automatinės išlaidos, kurioms priskirtas konkretus pristatymo būdo ryšys, skaičiuojamos tik nustačius atitikimą su pardavimo užsakymo antraštėje nurodytu pristatymo būdu.

Pavyzdžiui, antraštės lygio automatinės išlaidos nustatomos ir priskiriamos pristatymo būdui **99** ir pristatymo būdui **11**. Sukuriamas pardavimo užsakymas ir užsakymo antraštėje nustatomas pristatymo būdas **99**. Tačiau kai kurios pardavimo eilutės nustatomos taip, kad jos siunčiamos naudojant pristatymo būdą **11**. Šiuo atveju tik antraštės lygio išlaidos, susietos su pristatymo būdu **99**, yra apdorojamos ir taikomos pardavimo užsakymui.

„Commerce“ antraštės lygio išlaidos turi papildomą funkciją, leidžiančią apibrėžti [pakopinę išlaidų konfigūraciją](/dynamics365/unified-operations/retail/configure-call-center-delivery), kuri pagrįsta užsakymo verte. Pavyzdžiui, jei užsakymo vertė yra tarp 50,00 USD ir 200,00 USD, galbūt organizacija norės taikyti 5,00 USD transportavimo išlaidų mokestį. Tačiau, jei užsakymo vertė yra tarp 200,01 ir 500,00 USD, transportavimo mokestis gali būti 4,00 USD.

Kai kurios organizacijos nori pakopinių išlaidų skaičiavimo išmokų, pateiktų antraštės lygio išlaidose. Tačiau scenarijuose, kurie susiję su pristatymo būdais, jos taip pat nori įsitikinti, kad skaičiuojamos išlaidos yra pagrįstos kiekvienoje pardavimo eilutėje nurodyto pristatymo būdo atitikimu.

Dabar galite konfigūruoti antraštės lygio automatines išlaidas, kad visi užsakymo pristatymo būdai būtų apdorojami, kai skaičiuojamos išlaidos. Norint naudoti šią funkciją reikalinga sudėtingesnį skaičiavimo logika, pagal kurią skaičiuojamos antraštės lygio išlaidos. Logika kartu sugrupuoja visas prekes, kurios siunčiamos naudojant tą patį pristatymo būdą, ir laiko tą grupę prekių skaičiavimo grupe, kai skaičiuoja automatines antraštės lygio išlaidas. Jei prekėms priskirtas toks pat pristatymo būdas, automatinės išlaidos skaičiuojamos remiantis bendra prekių pardavimo verte. Tokiu būdu nustatoma atitinkama automatinių išlaidų pakopa.

Gavus pardavimo eilučių, kurios siunčiamos naudojant tokį patį pristatymo būdą, atitinkamas antraštės lygio išlaidas, apskaičiuotos išlaidos yra proporcingai paskirstomos pardavimo eilutės lygiu. Kadangi šios išlaidos yra eilutės lygio ir nėra saugomos antraštės lygiu, sukuriamas konkretesnis saitas tarp prekės jos apskaičiuotos išlaidų vertės. Tai gali būti naudinga dalinio gražinimo scenarijuose, kai grąžinama tik dalis prekių ir organizacija nori grąžinti tik dalį išlaidų, o ne visas išlaidas.

## <a name="scenarios"></a>Scenarijai

Tolesniuose dviejuose scenarijuose aprašoma, kaip šios išlaidos skaičiuojamos, kai nauja funkcija naudojama ir kai ji nenaudojama.

### <a name="scenario-1"></a>1 scenarijus

Šiame scenarijuje aprašoma, kas nutinka automatinių išlaidų sąrankoje nustačius parinkties **Proporcingai paskirstyti atitinkančioms pardavimo eilutėms** reikšmė **Ne**. (Šis veiksmas atitinka antraštės lygio išlaidų funkciją tokiose programų versijose, kurios yra senesnės nei 10.0.1 versija.)

Tokiu atveju organizacija nustatė antraštės lygio išlaidų pristatymo būdo ryšį **99** ir pristatymo būdo ryšį **11**. Pristatymo būdo **21** automatinės išlaidos nekonfigūruojamos.

![Pristatymo būdo 99 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra išjungtas.](media/99_disabled.png)

![Pristatymo būdo 11 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra išjungtas.](media/11_disabled.png)

Skambučių centre sukuriamas pardavimo užsakymo ir nustatomas pristatymo būdas **99**. Šiame užsakyme yra penkios prekės. Dvi užsakymo eilutės sukonfigūruotos naudoti pristatymo būdą **99**, dvi eilutės sukonfigūruotos naudoti pristatymo būdą **11**, o viena eilutė sukonfigūruota naudoti pristatymo būdą **21**, kaip parodyta tolesnėje lentelėje.

| Produktas  | Eilutės kiekis | Pristatymo režimas | Vieneto kaina |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 USD            |
| 81332 | 1             | 99            | 50 $            |
| 81333 | 2             | 11            | 30 USD            |
| 81334 | 3             | 99            | 10 USD            |
| 81334 | 3             | 21            | 5 USD             |

Tokiu atveju visas užsakymas vertinamas pagal pristatymo būdo **99** automatinių išlaidų lentelę. Bendra visų pardavimo eilučių suma naudojama nustatant atitinkamą pakopą automatinių išlaidų konfigūracijoje, o šis mokestis taikomas užsakymo antraštės lygiu. Šiame pavyzdyje užsakymo suma yra 165,00 USD, o 15,00 USD transportavimo mokestis taikomas užsakymo antraštei. Sukonfigūruotos pristatymo būdo **11** automatinės išlaidos niekada nenurodomos ir taikomos.

Tokiu atveju, jei klientas grąžina kai kurias užsakymo prekes ir jei [išlaidų kodas buvo sukonfigūruotas taip, kad pinigai būtų grąžinti](/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), visos antraštės lygio išlaidos yra sistemiškai taikomas grąžinimui, net jei grąžinamos tik kai kurios prekės.

### <a name="scenario-2"></a>2 scenarijus

Tokiu atveju nustatyti antraštės lygio išlaidų pristatymo būdo ryšys **99** ir pristatymo būdo ryšys **11**. Tačiau šių automatinių išlaidų lentelėse nustatoma parinkties **Proporcingai paskirstyti atitinkančioms pardavimo eilutėms** reikšmę **Taip**.

![Pristatymo būdo 99 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra įjungtas.](media/99_enabled.png)

![Pristatymo būdo 11 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra įjungtas.](media/11_enabled.png)

Šiame scenarijuje naudojamas tas pats pardavimo užsakymas, kuriame yra penkios eilutės. Nustatytas užsakymo antraštės pristatymo būdas **99**, bet kiekvienos pardavimo užsakymo prekės pristatymo būdas sukonfigūruojamas, kaip parodyta toliau pateiktoje lentelėje.

| Produktas  | Eilutės kiekis | Pristatymo režimas | Vieneto kaina |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 USD            |
| 81332 | 1             | 99            | 50 $            |
| 81333 | 2             | 11            | 30 USD            |
| 81334 | 3             | 99            | 10 USD            |
| 81334 | 3             | 21            | 5 USD             |

Kadangi automatinių išlaidų konfigūracija nustatyta proporcingai paskirstyti atitinkančioms pardavimo eilutėms, sistema atlieka toliau nurodytus skaičiavimo veiksmus.

1. Visos prekės, kurių pristatymo būdas yra toks pats, yra sugrupuojamos kartu ir sistema apskaičiuoja bendrą grupės prekių produktų vertę.

    **Pristatymo būdas 11**

    - Prekė 81331, kiekis 1 = 10 USD
    - Prekė 81333, kiekis 2 = 60 USD grynoji suma (30 USD už vienetą)
    - **Bendra pristatymo būdo 11 produkto vertė = 70 USD**

    **Pristatymo būdas 99**

    - Prekė 81332, kiekis 1 = 50 USD
    - Prekė 81334, kiekis 3 = 30 USD grynoji suma
    - **Bendra pristatymo būdo 99 produkto vertė = 80 USD**

    **Pristatymo būdas 21**

    - Prekė 81334, kiekis 3 = 15 USD grynoji suma
    - **Bendra pristatymo būdo 21 produkto vertė = 15 USD**

2. Sistema ieško antraštės lygio automatinių išlaidų konfigūracijos, kuri atitinka kiekvienos prekių grupės kliento ir pristatymo parametrus. Jei konfigūracija randama, sistema pakopinėje konfigūracijoje ieško išlaidų, kurios turėtų būti taikomos, pagal bendrą pristatymo būdo grupės prekių produktų vertę.

    **Pristatymo būdas 11**

    - Bendra produkto vertė = 70 USD
    - **Išlaidų vertė = 7 USD**

    **Pristatymo būdas 99**

    - Bendra produkto vertė = 80 USD
    - **Išlaidų vertė = 15 USD**

    **Pristatymo būdas 21**

    - Bendra produkto vertė = 15 USD
    - **Išlaidų vertė = 0 USD** (Šio kliento ir pristatymo būdo derinio automatinės išlaidos nesukonfigūruotos.)

    ![Pristatymo būdo 11 išlaidos patenka į paryškintą pakopą.](media/step2mode11.png)

    ![Pristatymo būdo 99 išlaidos patenka į paryškintą pakopą.](media/step2mode99.png)

3. Sistema apskaičiuoja išlaidų vertė, kuri turi būti taikoma kiekvienai eilutei, pagal proporcingo paskirstymo logiką, kuri proporcingą eilutės vertę nuskaito palygindama ją su bendra grupės produktų verte.

    **Pristatymo būdas 11**

    - Išlaidų vertė = 7 USD
    - Grupės produktų grupė vertė = 70 USD
    - 1 eilutės vertė = 10 USD (= 14,2857 procento grupės vertės)
    - 3 eilutės vertė = 60 USD (= 85,7143 procento grupės vertės)
    - **1 eilutės išlaidos = 1 USD**
    - **3 eilutės išlaidos = 6 USD**

    **Pristatymo būdas 99**

    - Išlaidų vertė = 15 USD
    - Grupės produktų grupė vertė = 80 USD
    - 2 eilutės vertė = 50 USD (= 62,5 procento grupės vertės)
    - 4 eilutės vertė = 30 USD (= 37,5 procento grupės vertės)
    - **2 eilutės išlaidos = 9.38 USD**
    - **4 eilutės išlaidos = 5,62 USD**

    **Pristatymo būdas 21**

    - Išlaidų vertė = 0 USD
    - Grupės produktų grupė vertė = 15 USD
    - 5 eilutės vertė = 15 USD (= 100 procento grupės vertės)
    - **5 eilutės išlaidos = 0 USD**

Todėl šiame pavyzdyje 81334 prekei bus priskirtas 5,62 transportavimo mokestis. Šias išlaidas galite peržiūrėti pardavimo eilutės puslapyje **Išlaidų tvarkymas**. Tolesnėje iliustracijoje rodoma, kaip rodomas šis 81334 prekės puslapis.

![81334 prekės pardavimo eilutės proporcingai paskirstytos išlaidos.](media/proratedlinecharge.png)

Kai šis skaičiavimo metodas naudojamas dalinio grąžinimo scenarijuje, jei išlaidų kodas yra grąžinamas, tik dalis išlaidų, paskirstytų tai eilutei, bus grąžinta grąžinus prekę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Integruoto kanalo išplėstinės automatinės išlaidos](omni-auto-charges.md)

[Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]