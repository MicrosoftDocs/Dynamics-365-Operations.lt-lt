---
title: Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms
description: Šioje temoje aprašomos mažmeninės prekybos kanalo užsakymų papildomos automatinių išlaidų skaičiavimo ir taikymo galimybės naudojant automatinių išlaidų funkciją.
author: hhaines
manager: annbe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 07eea8fd7af4da611b4bd0c9340923f8894fab2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1526020"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma funkcija, kurią naudojant antraštės lygio automatinės išlaidos grupuojamos ir proporcingai paskirstomos į mažmeninės prekybos pardavimo eilutes. Ši funkcija yra skirta operacijoms, kurios sukurtos elektroniniame kasos aparate (EKA) naudojant „Microsoft Dynamics 365 for Retail“ 10.0.1 versiją ir pardavimo operacijoms, kurios sukurtos skambučių centre naudojant „Microsoft Dynamics 365 for Retail“ 10.0.2 versiją.

Šią funkciją galima naudoti tik jei funkcija [Išplėstinės automatinės išlaidos](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) įjungta naudojant parinktį puslapyje **Mažmeninės prekybos parametrai**. Be to, patobulintą automatinių išlaidų skaičiavimo metodą galima taikyti tik mažmeninės prekybos pardavimo užsakymams, kurie sukurti mažmeninės prekybos kanaluose (EKA, skambučių centre ir „Dynamics e-Commerce“ platformoje).

Ši nauja funkcija suteikia organizacijoms daugiau lankstumo skaičiuojant antraštės lygio automatines išlaidas ir taikant jas mažmeninės prekybos pardavimo operacijoms.

Ankstesnėse nei 10.0.1 „Microsoft Dynamics 365 for Retail“ versijose antraštės lygio automatinės išlaidos, kurioms priskirtas konkretus pristatymo būdo ryšys, skaičiuojamos tik nustačius atitikimą su pardavimo užsakymo antraštėje nurodytu pristatymo būdu.

Pavyzdžiui, antraštės lygio automatinės išlaidos nustatomos ir priskiriamos pristatymo būdui **99** ir pristatymo būdui **11**. Sukuriamas pardavimo užsakymas ir užsakymo antraštėje nustatomas pristatymo būdas **99**. Tačiau kai kurios pardavimo eilutės nustatomos taip, kad jos siunčiamos naudojant pristatymo būdą **11**. Šiuo atveju tik antraštės lygio išlaidos, susietos su pristatymo būdu **99**, yra apdorojamos ir taikomos pardavimo užsakymui.

„Dynamics 365 for Retail“ antraštės lygio išlaidoms priskirta papildoma funkcija, kuri suteikia galimybę nustatyti [pakopinių išlaidų konfigūraciją](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery), pagrįstą užsakymo verte. Pavyzdžiui, jei užsakymo vertė yra tarp 50,00 USD ir 200,00 USD, galbūt organizacija norės taikyti 5,00 USD transportavimo išlaidų mokestį. Tačiau, jei užsakymo vertė yra tarp 200,01 ir 500,00 USD, transportavimo mokestis gali būti 4,00 USD.

Kai kurios organizacijos nori pakopinių išlaidų skaičiavimo išmokų, pateiktų antraštės lygio išlaidose. Tačiau scenarijuose, kurie susiję su pristatymo būdais, jos taip pat nori įsitikinti, kad skaičiuojamos išlaidos yra pagrįstos kiekvienoje pardavimo eilutėje nurodyto pristatymo būdo atitikimu.

Dabar galite konfigūruoti antraštės lygio automatines išlaidas, kad visi užsakymo pristatymo būdai būtų apdorojami, kai skaičiuojamos išlaidos. Norint naudoti šią funkciją reikalinga sudėtingesnį skaičiavimo logika, pagal kurią skaičiuojamos antraštės lygio išlaidos. Logika kartu sugrupuoja visas prekes, kurios siunčiamos naudojant tą patį pristatymo būdą, ir laiko tą grupę prekių skaičiavimo grupe, kai skaičiuoja automatines antraštės lygio išlaidas. Jei prekėms priskirtas toks pat pristatymo būdas, automatinės išlaidos skaičiuojamos remiantis bendra prekių pardavimo verte. Tokiu būdu nustatoma atitinkama automatinių išlaidų pakopa.

Gavus pardavimo eilučių, kurios siunčiamos naudojant tokį patį pristatymo būdą, atitinkamas antraštės lygio išlaidas, apskaičiuotos išlaidos yra proporcingai paskirstomos pardavimo eilutės lygiu. Kadangi šios išlaidos yra eilutės lygio ir nėra saugomos antraštės lygiu, sukuriamas konkretesnis saitas tarp prekės jos apskaičiuotos išlaidų vertės. Tai gali būti naudinga dalinio gražinimo scenarijuose, kai grąžinama tik dalis prekių ir organizacija nori grąžinti tik dalį išlaidų, o ne visas išlaidas.

## <a name="scenarios"></a>Scenarijai

Tolesniuose dviejuose scenarijuose aprašoma, kaip šios išlaidos skaičiuojamos, kai nauja funkcija naudojama ir kai ji nenaudojama.

### <a name="scenario-1"></a>1 scenarijus

Šiame scenarijuje aprašoma, kas nutinka automatinių išlaidų sąrankoje nustačius parinkties **Proporcingai paskirstyti atitinkančioms pardavimo eilutėms** reikšmė **Ne**. (Ši elgsena atitinka antraštės lygio išlaidų elgseną mažmeninės prekybos versijose, kurios yra ankstesnės nei 10.0.1 versija).

Tokiu atveju organizacija nustatė antraštės lygio išlaidų pristatymo būdo ryšį **99** ir pristatymo būdo ryšį **11**. Pristatymo būdo **21** automatinės išlaidos nekonfigūruojamos.

![Pristatymo būdo 99 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra išjungtas](media/99_disabled.png)

![Pristatymo būdo 11 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra išjungtas](media/11_disabled.png)

Skambučių centre sukuriamas pardavimo užsakymo ir nustatomas pristatymo būdas **99**. Šiame užsakyme yra penkios prekės. Dvi užsakymo eilutės sukonfigūruotos naudoti pristatymo būdą **99**, dvi eilutės sukonfigūruotos naudoti pristatymo būdą **11**, o viena eilutė sukonfigūruota naudoti pristatymo būdą **21**, kaip parodyta tolesnėje lentelėje.

| Produktas  | Eilutės kiekis | Pristatymo režimas | Vieneto kaina |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 USD            |
| 81332 | 1             | 99            | 50 $            |
| 81333 | 2             | 11            | 30 USD            |
| 81334 | 3             | 99            | 10 USD            |
| 81334 | 3             | 21            | 5 USD             |

Tokiu atveju visas užsakymas vertinamas pagal pristatymo būdo **99** automatinių išlaidų lentelę. Bendra visų pardavimo eilučių suma naudojama nustatant atitinkamą pakopą automatinių išlaidų konfigūracijoje, o šis mokestis taikomas užsakymo antraštės lygiu. Šiame pavyzdyje užsakymo suma yra 165,00 USD, o 15,00 USD transportavimo mokestis taikomas užsakymo antraštei. Sukonfigūruotos pristatymo būdo **11** automatinės išlaidos niekada nenurodomos ir taikomos.

Tokiu atveju, jei klientas grąžina kai kurias užsakymo prekes ir jei [išlaidų kodas buvo sukonfigūruotas taip, kad pinigai būtų grąžinti](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), visos antraštės lygio išlaidos yra sistemiškai taikomas grąžinimui, net jei grąžinamos tik kai kurios prekės.

### <a name="scenario-2"></a>2 scenarijus

Tokiu atveju nustatyti antraštės lygio išlaidų pristatymo būdo ryšys **99** ir pristatymo būdo ryšys **11**. Tačiau šių automatinių išlaidų lentelėse nustatoma parinkties **Proporcingai paskirstyti atitinkančioms pardavimo eilutėms** reikšmę **Taip**.

![Pristatymo būdo 99 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra įjungtas](media/99_enabled.png)

![Pristatymo būdo 11 automatinės išlaidos, kai atitikimo eilutės proporcingas paskirstymas yra įjungtas](media/11_enabled.png)

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

    - Bendra mažmeninės prekybos produkto vertė = 70 USD
    - **Išlaidų vertė = 7 USD**

    **Pristatymo būdas 99**

    - Bendra mažmeninės prekybos produkto vertė = 80 USD
    - **Išlaidų vertė = 15 USD**

    **Pristatymo būdas 21**

    - Bendra mažmeninės prekybos produkto vertė = 15 USD
    - **Išlaidų vertė = 0 USD** (Šio kliento ir pristatymo būdo derinio automatinės išlaidos nesukonfigūruotos.)

    ![Pristatymo būdo 11 išlaidos patenka į paryškintą pakopą](media/step2mode11.png)

    ![Pristatymo būdo 99 išlaidos patenka į paryškintą pakopą](media/step2mode99.png)

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

![81334 prekės pardavimo eilutės proporcingai paskirstytos išlaidos](media/proratedlinecharge.png)

Kai šis skaičiavimo metodas naudojamas dalinio grąžinimo scenarijuje, jei išlaidų kodas yra grąžinamas, tik dalis išlaidų, paskirstytų tai eilutei, bus grąžinta grąžinus prekę.
