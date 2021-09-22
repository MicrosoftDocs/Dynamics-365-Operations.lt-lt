---
title: Įgalinti svečių išregistrų užsakymo peržvalgą
description: Šioje temoje aprašoma, kaip įgalinti svečių registracijos užsakymų „Microsoft Dynamics 365 Commerce“ peržvalgą.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0368f567898210f122047a9f298bcb28b7540de1
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472650"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Įgalinti svečių išregistrų užsakymo peržvalgą

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašoma, kaip įgalinti svečių registracijos užsakymų „Microsoft Dynamics 365 Commerce“ peržvalgą.

Svečių tikrinimo priemonės užsakymo peržvalga leidžia klientams, kurie perka kaip svečio vartotojus, peržiūrėti savo užsakymus. Užsakymo peržvalgos galimybė naudinga, kai klientai nori atlikti tokius veiksmus, kaip produktų įvykdymo būsenos tikrinimas užsakyme, adreso, kuriuo buvo pristatytas užsakymas, patikrinimas, produkto užsakymas ar parduotuvės patvirtinimas, iš kurio bus paimtas užsakymas.

Klientai, kurie užsakymus laiko registruotais vartotojais, prisiregistravę gali matyti savo užsakymų informaciją, bet klientai, kurie užsakymus išregistruoja kaip svečią, negali to padaryti. Tačiau, kai užsakymų peržvalga svečių čekių funkcija yra įgalinta, joje pateikiama forma, kurią klientai gali naudoti norėdami ieškoti užsakymų, kuriuos jie pateikia kaip svečius. Šioje formoje klientai įveda užsakymo patvirtinimo ID ir (pasirinktinai) el. pašto adresą, kurį nurodė išregistravimas.

Be to, saitas arba mygtukas, kuris atsiunčia klientą tiesiai į jo užsakymo informacijos puslapį, gali būti įtrauktas į visus su užsakymu susijusius operacijų el. laiškus. Šis saitas arba mygtukas veiks užsakymams, kuriuos pateikti ir registruotieji vartotojai, ir svečių vartotojai.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Įjungti būtinas „Commerce Headquarters" funkcijas

Norėdami įgalinti svečių tikrinimo užsakymų peržvalgą, turite įjungti šias **Darbo sritys \> Funkcijų valdymas** „Commerce“ štabe.

| Funkcija | Paskirtis |
|---------|---------|
| „Retail“ anoniminio vartotojo paieškos užsakymo informacijos pasirinkimo funkcija | Ši funkcija parodo vartotojo sąsają „Commerce" parametruose, kurie leidžia įgalinti užsakymo peržvalgos API neautentifikuotiems vartotojams ir konfigūruoti asmeninių duomenų rodymą. |
| Įgalinti stipresnio kanalo nuorodos ID generavimą | Ši funkcija sugeneruoja saugesnį 12 simbolių kanalo nuorodos ID (užsakymo patvirtinimo ID), kurį galima perduoti užklausos eilutėje, kai peržvalga. |
| Generuoti nuoseklų kanalo nuorodos ID formatą visuose kanaluose | Ši funkcija sugeneruoja saugų kanalo nuorodos ID užsakymams, kurie pateikiami per el. komercijos svetainę, mažmeninės prekybos elektroninį kasos punktą (EKA) arba skambučių centrą. Prieš įjungdami šią funkciją, turite įjungti **funkciją Įgalinti didesnį kanalo nuorodos ID** generavimą. |

Įjungus **mažmeninės prekybos anoniminio vartotojo ieškos užsakymo informacijos pasirinkimo funkcijos** funkciją, „Commerce Headquarters" reikia įgalinti API, palaikančią neautentifikuotą užsakymų peržvalgą. Eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> Kliento užsakymai**. Puslapyje **Kliento užsakymų** „FastTab“ **užsakymų ieškos** nustatykite pasirinktį **Įgalinti neautentifikuotą užsakymo peržvalgą** kaip **Taip**, kaip parodyta toliau pateiktame pavyzdyje.

## <a name="manage-the-display-of-personal-data"></a>Asmeninių duomenų rodymo valdymas

„FastTab“ **Užsakymo iešką** „FastTab“ **Kliento užsakymai** puslapyje „Commerce headquarters“ apima **asmeninių duomenų į svečių užsakymų peržvalgos** lauką, kuris leidžia kontroliuoti, ar klientams rodoma asmeninė informacija. Ši asmeninė informacija apima kliento siuntimo adresą ir paskutinius keturis kliento kredito kortelės numerio skaitmenis. Pagal numatytuosius nustatymus asmeninė informacija klientams nerodoma, kai įgalinta neautentifikuota užsakymų peržvalga. Šioje lentelėje aprašytos prieinamos parinktys.

| Parinktis | Rezultatas |
|--------|--------|
| Niekada | Numatytoji vertė. Užsakymų peržvalgoje asmeninė informacija nerodoma. Kai registruoti vartotojai, kurie prisiregistravo peržiūrėdami užsakymą, kurį jie sukūrė, kol prisiregistruoja, jie galės matyti savo asmeninę informaciją. |
| Tik svečių užsakymai | Užsakymų, kuriuos klientai sukūrė kaip svečius, peržvalgoje rodoma asmeninė informacija. Jei užsakymą sukūrė registruotasis vartotojas, jis turi prisiregistruoti, kad pamatytų savo asmeninę informaciją. |
| Visi užsakymai | Užsakymų peržvalgoje visa asmeninė informacija nerodoma. |

> [!NOTE]
> Šios pasirinktys nurodo, kada anoniminiams svečiui rodomi asmeniniai duomenys, pvz., kliento adresas ir keturi paskutiniai kliento kredito kortelės numerio skaitmenys. Siekiant apsaugoti užregistruotų klientų privatumą, rekomenduojame pasirinkti tik **pasirinktį Svečio užsakymai**. Tačiau saugiausia pasirinktis yra **Niekada**.

Pakeiskite "Commerce Headquarters" užduotį **Įtraukti asmeninius duomenis į svečių užsakymo** peržvalgos lauką turite vykdyti 1070 (**Kanalo konfigūravimą**) ir tada nueiti į **Mažmeninė prekyba ir komercija \> Mažmeninė prekyba ir komercijos IT \> Paskirstymo grafikas**.

## <a name="configure-the-order-lookup-module"></a>Konfigūruoti užsakymo peržvalgos modulį

Užsakymų peržvalgos modulis „Commerce" modulių bibliotekoje naudojamas formai, kurią vartotojai naudoja užsakymams ieškoti, atvaizduoti. Užsakymo peržvalgos modulį galima įtraukti į bet kurio puslapio, prie kurio nereikia prisijungti kliento, kūno atminties atminties atminties lauką. Informacijos apie modulio konfigūravimą ieškokite [užsakymo peržvalgos modulyje](order-lookup-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Užsakymo peržvalgos modulis](order-lookup-module.md)

[El. paštu siunčiamo pranešimo šablono nustatymas](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
