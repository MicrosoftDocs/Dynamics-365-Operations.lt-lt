---
title: Sandėliavimo limitų vieta
description: Šiame straipsnyje aprašomos vietos sandėliavimo limitų funkcijos.
author: perlynne
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 794fe9afddfa43862aea62bf56f9b745aaf91c2c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854042"
---
# <a name="location-stocking-limits"></a>Sandėliavimo limitų vieta

[!include [banner](../includes/banner.md)]

Galite naudoti **Sandėliavimo limitų vietos** puslapį (**Sandėlio valdymas \> Nustatymai \> Sandėlis \> Sandėlio limitų vietos**) tam, kad suvaldytumėte krovinio talpą sandėlio vietose be papildomų procesų naudojimo fizinių produktų tūrio skaičiavimams.

Siandėliavimo limitų vietos tikslas yra įvertinti maksimalų kiekį, kurį vieta gali turėti. Galite nustayti funkciją bet kuriame iš trijų lygių, kurių kiekvienas turi jam skirtą skirtuką **Sandėliavimo limitų vietos** puslapis:

- Produktai
- Produkto variantai
- Konteinerių tipai

Kiekvienam lygiui galite nustatyti skirtingas laukelio vertes. Sistema tuomet įvertins konkrečios vietos talpą pagal **Kiekį** ir **Vieneto** vertes kiekvienai eilutei. Ji parinks išsamiausią atitinkantį įrašą pirma. Pavyzdžiui, eilutė turinti vertę **Vietos profilio ID** laukelis bus vertinama prieš eilutę, kuri turi tik vertę **Sandėlio** laukelyje. Likęs kiekis taip pat bus vertinamas pagal **Kiekio** vertę sandėliavimo limitų vietos įraše, kuris yra naudojamas.

Puslapio skyriuje **Produktai** galite nustatyti tolesnes laukelio vertes paieškai sandėliavimo limitų vietai:

- Sandėlis
- Vietos šablono ID
- Buvimo vieta
- Paketo dydžio kategorijos ID
- Prekės Nr.
- Vienetas

> [!NOTE]
> Neturite nustatyti **Vieneto** vertės kiekvienam sandėliavimo limitų vietos įrašui. Vietos talpos apskaičiavimai bus paremti inventoriaus vieneto kiekiais. Jei nėra vieneto pavertimo nustatyto nenaudojamai vertei, sandėliavimo limito vietos įrašas bus praleistas taip tarsi kita  **Vieneto skaičiaus** vertė jai bus nustatyta.

## <a name="example--purchase-order-receiving"></a>Pavyzdys – Pirkimo užsakymo gavimas

Šis pavyzdys paremtas švariu *USMF* demonstracinių duomenų rinkiniu, kuriame tolesnės vertės nustatytos **Produkto variantų** skirtuke **Sandėliavimo limitų vietos** puslapyje.

| Sandėlis | Vietos šablono ID | Prekės Nr. | Dydis | Kiekis | Vienetas |
|-----------|---------------------|-------------|------|----------|------|
| 24        | AUKŠTAS               | D0013       | P    | 300      | Vnt.   |
| 24        | AUKŠTAS               | D0013       | L    | 240      | Vnt.   |
| 24        | AUKŠTAS               | D0013       | Š.    | 360      | Vnt.   |

Kiti matavimo vieneto produkto variantai yra nustatyti produktams. Šie variantai yra suderinti su sandėliavimo limitų vieta trims padėklams (PL):

- **Dydis M:** 1 PL = 100 kiekvienas (Ea)
- **Dydis L:** 1 PL = 80 (Ea)
- **Dydis S:** 1 PL = 120 (Ea)

Dėl to, kiekviena vieta, kurioje **Vietos profilio ID** vertė yra nustatyta į *AUKŠTĄ* gali turėti *3* *PL* prekės skaičiaus *D0013*.

### <a name="prepare-for-the-example"></a>Parengimas pavyzdžiui

Šiuo atveju, vykdysite pirkimo užsakymo gavimo eigą dviem eilutėms. Nepaisant to, pirma turite naujinti demonstracinius duomenis tolesniu būdu siekiant užtikrinti, kad vietos leidžia turėti maišytas prekes, tik tuščios vietos *FL-002* per *FL-004* yra naudojamos ir yra atviras įvesties darbas.

1. Vietai *FL-001*, keiskite **Vietos profilio** laukelio vertę iš *AUKŠTAS* į *AUKŠTAS-05*.
1. *AUKŠTO* vietos profiliui, nustatykite **Leidžiamos maišytos prekės** parinktį į *Taip*.
1. Sukurkite prikimo užsakymą, kuris turi dvi tolesnes eilutes.

    | Sandėlis | Prekės Nr. | Dydis | Kiekis | Vienetas |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | Š.    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Apdorokite pavyzdį

Pirmiausia gausite kiekį *4* prekės *PL* dydžio *S* ir peržiūrėkite padėjimo eilutės vietas darbui, kuris yra sukuriamas. Tada gausite kiekį *4* prekės *PL* dydžio *L* ir peržiūrėkite padėjimo eilutės vietas darbui, kuris yra sukuriamas.

1. Prisijunkite prie sandėlio valdymo mobiliųjų įrenginių programėlės naudodami *24 kaip* vartotojo ID ir *1 kaip* slaptažodį.
1. Rinkitės **Įvestis** \> **Pirkimo gavimas**.
1. Gaukite *4* *PL* prekės numerio *D0013* dydžio *S*.
1. Peržiūrėkite sukurtą atidėjimo darbą. Turėtumėte matyti tolesnius rezultatus:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Gaukite *4* *PL* prekės numerio *D0013* dydžio *L*.
1. Peržiūrėkite sukurtą atidėjimo darbą. Turėtumėte matyti tolesnius rezultatus:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Atsižvelgiant į rezultatus, galite daryti išvadą, kad sistemai nepavyko priskirti tinkamų atidėjimo vietų. Kitu atveju, kodėl sistema įtraukė tik *1* *PL* dydžio *L* į vietą *FL-003* paskurtiniu žingsniu, o ne *2* *PL*? Taip yra todėl, kad nėra bendro *3* *PL* atidėjimo tai vietai?

Siekiant paaiškinti šią akivaizdžią nesėkmę, turite suprasti kriterijų sandėliavimo limitų vietos kriterijus. Sistema pasirenka išsamiausią atitikmens įrašą. Šiame pavyzdyje, išsamiausias atitikmens įrašas atitinka eilutę, kurioje **Dydis** vertė yra *L*, **Kiekio** vertė yra *240* ir **Vieneto** vertė yra *Ea*. kadangi jau atvėrėte darbą iš ankstesnio kiekio gavimo *120* *Ea* dydžio *S*, likusi talpa skaičiuoajam kaip *240* – *120* = *120* *Ea*. Dėl to, likusi talpa gali apimti tik *1* *PL* of *80* *Ea*.

> [!NOTE]
> Negalite naudoti sandėliavimo vietos limitų siekiant valdyti, pavyzdžiui, prekių papildymo, kuris turi kitus kiekius toje pačioje vietoje. Tokiu atveju, naudokite *papildymo pavyzdį*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]