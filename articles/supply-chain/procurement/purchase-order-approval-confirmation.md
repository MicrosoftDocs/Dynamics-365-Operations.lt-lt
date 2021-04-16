---
title: Pirkimo užsakymų tvirtinimas
description: Šioje temoje aprašomos būsenos, kurios taikomos sukurtam pirkimo užsakymui, paaiškinama, kas nutinka suaktyvinus PU keitimų valdymą.
author: kamaybac
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f1f6971e645a0aae8679c94a4bbd4cba946dc3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825427"
---
# <a name="approve-and-confirm-purchase-orders"></a>Pirkimo užsakymų tvirtinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos būsenos, kurios taikomos sukurtam pirkimo užsakymui (PU), paaiškinama, kas nutinka suaktyvinus PU keitimų valdymą.

Sukūrus pirkimo užsakymą (PU), jį gali reikėti patvirtinti. Kai tiekėjas užsakymą patvirtina, PU būsena nustatoma kaip **Patvirtinta**.

## <a name="approval-of-purchase-orders"></a>Pirkimo užsakymų patvirtinimas
Iš karto sukūrus, PU, kuriuose nenaudojamas keitimų valdymas, būsena yra **Patvirtinta**, o PU, kuriuose naudojamas keitimų valdymas, pirmą kartą sukūrus, būsena yra **Juodraštis**. PU, kuris buvo sukurtas patvirtinus suplanuotą užsakymą iš bendrojo planavimo, būsena visada nustatoma kaip **Patvirtinta**, nepriklausomai nuo keitimų valdymo parametrų. PU sukuria atsargų operacijas tik tada, kai jo būsena pasikeičia į **Patvirtinta**. Todėl nerodoma, kad atsargas galima rezervuoti arba žymėti, kol užsakymas nepatvirtintas.

PU keitimų valdymas įjungiamas puslapyje **Įsigijimo ir šaltinio pasirinkimo parametrai** nustatant parinktį **Aktyvinti pokyčių valdymą**. Suaktyvinus keitimų valdymą, užbaigtiems PU turi būti taikoma patvirtinimo darbo eiga. Tiekimo grandinės valdyme teikiama eigos proceso rengyklė, kurioje galima nurodyti patvirtinimo proceso darbo eigą. Ši darbo eiga gali apimti automatinio patvirtinimo taisykles, taisykles, nurodančias, ką priskirti konkrečiam PU tvirtinti, ir taisyklės, skirtas darbo eigai, kuri laukia patvirtinimo ilgą laiką, perskirti. Galite suaktyvinti visų tiekėjų arba konkrečių tiekėjų keitimų valdymo procesą. Taip pat galite nustatyti procesą, kad jį būtų galima perrašyti atskiriems PU.

Įgalinus keitimų valdymą, naudojamos šešios PU patvirtinimo būsenos, nuo **Juodraštis** iki **Baigta**. Patvirtinus užsakymą, jį modifikuoti norintys vartotojai turi naudoti veiksmą **Reikalauti keitimo**.

| Patvirtinimo būsena | Aprašymas                                                                      | Veiksmas Reikalauti keitimo yra suaktyvintas |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Juodraštis           | PU yra juodraštis, kuris nebuvo pateiktas tvirtinti PU darbo eigoje.     | Ne                        |
| Peržiūrima       | PU buvo pateiktas tvirtinti PU darbo eigoje. Laukiama patvirtinimo.       | Ne                        |
| Atmesta        | PU buvo atmestas tvirtinimo proceso metu.                                 | Ne                        |
| Patvirtinta        | PU buvo patvirtintas.                                                             | Taip                       |
| Pritarta       | PU buvo patvirtintas. PU negalima patvirtinti, kol jis nepatvirtintas.        | Taip                       |
| Baigta       | PU nustatytas kaip galutinis. Dabar jis yra finansiškai uždarytas ir jo nebegalima keisti. | Ne                        |

## <a name="confirming-purchase-orders"></a>Pirkimo užsakymų patvirtinimas
Gali reikėti atlikti papildomų veiksmų, norint patvirtinti PU, kurių patvirtinimo būseną yra **Patvirtinta**. Pavyzdžiui, jums gali tekti tiekėjui pateikti pirkimo užklausą apie kainas, nuolaidas arba pristatymo datas. Šiuo atveju galite nustatyti PU būseną kaip **Išorinė peržiūra**, naudodami veiksmą **Pirkimo užklausa**.

Tiekėjai, kuriems nustatyta galimybė naudoti tiekėjo portalą, portale gali užsakymus peržiūrėti ir patvirtinti arba atmesti. Šio peržiūros proceso metu PU būsena yra **Išorinė peržiūra**. Tiekėjų portalą galima sukonfigūruoti taip, kad, užsakymą patvirtinus tiekėjui, jis būtų automatiškai patvirtintas Tiekimo grandinės valdyme. Arba jūs galite neautomatiniu būdu patvirtinti PU, kai tiekėjas jį patvirtina. Jei tiekėjas PU atmeta, apie atmetimą informuojama nurodant atmetimo priežastį ir keitimų pasiūlymus. Tokiu atveju PU būsena lieka **Išorinė peržiūra**.

Taip pat galima generuoti išankstinį užsakymo patvirtinimą, prieš apdorojant faktinį patvirtinimą. Naudojant šią parinktį sukuriama ataskaita, kurią galite bendrinti su tiekėju. Jokia žurnalo informacija nesukuriama.

Po to, kai tiekėjas patvirtina užsakymą, kitu veiksmu PU įrašomas kaip užfiksuotas. Šį veiksmą galite atlikti naudodami veiksmą **Patvirtinimas** arba **Patvirtinti**. Naudojant abu veiksmus užsakymo patvirtinimo būsena nustatoma kaip **Patvirtinta**. Patvirtinus įsakymą inicijuojami du papildomi procesai.

-   Sukuriamas žurnalas, skirtas tiksliai patvirtinto užsakymo kopijai sistemoje saugoti. Kartais užsakymus reikia keisti ir patvirtinus atnaujintą užsakymą sukuriami papildomi žurnalai. Šiuose žurnaluose galima peržiūrėti įvairių patvirtintų užsakymo versijų retrospektyvą.
-   Sukuriami apskaitos paskirstymai ir vykdomi užsakymo bei biudžeto tikrinimai, jei ši funkcija įjungta. Jei kuris nors patikrinimas nepavyksta, rodomas klaidos pranešimas, nurodantis, kad prieš patvirtinant PU reikia atlikti keitimų.

Tiekėjas gali prašyti kokio nors tipo garantijos, kad už pirkimą bus sumokėta. Šią garantiją suteikti naudojant mokėtinų sumų procesus galima įvairiais būdais. Pvz., veiksmu **Išankstinis mokėjimas** rezervuojamos PU lėšos ir šis išankstinis mokėjimas yra užregistruojamas PU.

## <a name="changing-purchase-orders"></a>Pirkimo užsakymų keitimas
Kai kuriais atvejais gali reikėti PU pakeisti po to, kai jo būsena buvo nustatyta kaip **Patvirtinta** arba **Patvirtinta**.

Jei PU buvo sukurtas vykdant pakeitimų valdymo procesą, keitimus galite atlikti užsakymą atšaukdami arba, jei užsakymas jau buvo patvirtintas, naudodami veiksmą **Reikalauti keitimo**. Tokiu atveju patvirtinimo būsena vėl pakeičiama į **Juodraštis** ir tada užsakymą tada galite keisti. Atlikus keitimus, PU gali reikėti pateikti pakartotinai patvirtinti. Pakeitimų, kuriuos atlikus užsakymą reikia pakartotinai patvirtinti, tipus galite naudodami puslapio **Pirkimo užsakymų pakartotinio patvirtinimo taisyklė** veiksmą **Pirkimo strategijos**.

Jei pristatyta užsakyto PO eilutės kiekio dalis, užsakyto kiekio keisti negalima, kai pirkimo užsakymo būsena yra **Juodraštis**. Tačiau pirkimo užsakymo, kurio būsena yra **Juodraštis**, eilutėje galite keisti kiekį **Pristatymo likutis**.

Patvirtinus užsakymą jo panaikinti nebegalima. Tačiau užsakyme galite atšaukti visą kiekį ar bet kokį likusį kiekį, jei kiekis nebuvo gautas arba neišrašyta jo SF. Tada galite naudoti veiksmą **Baigti**, norėdami neleisti toliau apdoroti. 


## <a name="canceling-purchase-orders"></a>Pirkimo užsakymų atšaukimas

PU galima atšaukti naudojant antraštės veiksmą **Atšaukti**.

Jei kiekis buvo iš dalies užregistruotas, gautas arba buvo išrašyta SF, galite atšaukti tik likusį kiekį, kuris nebuvo užregistruotas, gautas arba kuriam nebuvo išrašyta SF. Užsakymo kiekis atitinkamai sumažinamas. Atnaujinus eilutėje nurodytą kiekį, taip pat atnaujinama eilutės būsena. Pavyzdžiui, pradinis kiekis eilutėje yra 5, o gaunamas kiekis – 3. Šiuo atveju galima atšaukti tik du vienetus. Eilutė atnaujinama, kad būtų rodoma būsena **Gauta**.

Jei pristatymo likutis įtraukiamas į užsakymo eilutę ir viršija kiekį užsakymo eilutėje, veiksmas **Atšaukti** neanuliuoja perteklinio kiekio. Vietoj to, eilutės būsena išlieka **Atviras užsakymas**, nes joje yra likęs kiekis. Pavyzdžiui, pradinis kiekis eilutėje yra 5, o pristatymo likutis – 7. Jei užsakymas atšaukiamas, penki vienetai bus atšaukti, o 2 vienetų kiekis išliks, kaip galima matyti atsargų operacijose.

Norėdami PU eilutėje atšaukti visą kiekį, eilutėje turite atšaukti pristatymo likučio kiekį. Eilutės būsena bus atnaujinta į **Atšaukta**.

Vykdant PU pakeitimų valdymą, bet koks pasikeitimas, pvz., užsakymo arba pristatymo likučio atšaukimas, turi būti pateiktas darbo eigos sistemai ir patvirtintas prieš tai, kai procesas gali būti baigtas, o atsargų operacijų būsena gali būti atnaujinta į atšauktą.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pirkimo užsakymų apžvalga](purchase-order-overview.md)

[Pirkimo užsakymų kūrimas](purchase-order-creation.md)

[Produkto gavimas pagal pirkimo užsakymą](product-receipt-against-purchase-orders.md)

[Tiekėjų sąskaitų faktūrų apžvalga](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]