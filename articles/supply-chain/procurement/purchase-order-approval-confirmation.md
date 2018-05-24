---
title: "Pirkimo užsakymų patvirtinimas"
description: "Šiame straipsnyje aprašomos būsenos, kurios taikomos sukurtam pirkimo užsakymui (PU), paaiškinama, kas nutinka suaktyvinus PU keitimų valdymą."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 475470fa87455e187e0a93148046cb1df634da1f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="approve-and-confirm-purchase-orders"></a>Pirkimo užsakymų patvirtinimas

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Šiame straipsnyje aprašomos būsenos, kurios taikomos sukurtam pirkimo užsakymui (PU), paaiškinama, kas nutinka suaktyvinus PU keitimų valdymą.

Sukūrus pirkimo užsakymą (PU), jį gali reikėti patvirtinti. Kai tiekėjas užsakymą patvirtina, PU būsena nustatoma kaip **Patvirtinta**.

## <a name="approval-of-purchase-orders"></a>Pirkimo užsakymų patvirtinimas
PU, kuriuose nenaudojamas keitimų valdymas, būsena nustatoma kaip **Patvirtinta** iš karto juos sukūrus, o PU, kuriuose naudojamas keitimų valdymas,būsena nustatoma kaip **Juodraštis**, pirmą kartą juos sukūrus. PU, kuris buvo sukurtas patvirtinus suplanuotą užsakymą iš bendrojo planavimo, būsena visada nustatoma kaip **Patvirtinta**, nepriklausomai nuo keitimų valdymo parametrų. PU sukuria atsargų operacijas tik tada, kai jo būsena pasikeičia į **Patvirtinta**. Todėl nerodoma, kad tas atsargas galima rezervuoti arba žymėti, kol užsakymas nepatvirtintas.  

PU keitimų valdymas įjungiamas puslapyje **Įsigijimo ir šaltinio pasirinkimo parametrai** nustatant parinktį **Aktyvinti pokyčių valdymą**. Suaktyvinus keitimų valdymą, užbaigtiems PU turi būti taikoma patvirtinimo darbo eiga. „Microsoft Dynamics 365 for Finance and Operations“ teikia darbo eigos procesų rengyklę, kurioje galima nurodyti patvirtinimo proceso darbo eigą. Ši darbo eiga gali apimti automatinio patvirtinimo taisykles, taisykles, nurodančias, ką priskirti konkrečiam PU tvirtinti, ir taisyklės, skirtas darbo eigai, kuri laukia patvirtinimo ilgą laiką, perskirti. Galite suaktyvinti visų tiekėjų arba konkrečių tiekėjų keitimų valdymo procesą. Taip pat galite nustatyti procesą, kad jį būtų galima perrašyti atskiriems PU.  

Įgalinus keitimų valdymą, naudojamos šešios PU patvirtinimo būsenos, nuo **Juodraštis** iki **Baigta**. Patvirtinus užsakymą, jį modifikuoti norintys vartotojai turi naudoti veiksmą **Reikalauti keitimo**.

| Patvirtinimo būsena | Prekės/Paslaugos pavadinimas                                                                      | Veiksmas Reikalauti keitimo suaktyvintas |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Juodraštis           | PU yra juodraštis ir jis nebuvo pateiktas tvirtinti PU darbo eigoje.     | Ne                        |
| Peržiūrima       | PU buvo pateiktas tvirtinti PU darbo eigoje. Laukiama patvirtinimo.       | Ne                        |
| Atmesta        | PU buvo atmestas tvirtinimo proceso metu.                                 | Ne                        |
| Patvirtinta        | PU buvo patvirtintas.                                                             | Taip                       |
| Patvirtinta       | PU buvo patvirtintas. PU negalima patvirtinti, kol jis nepatvirtintas.        | Taip                       |
| Baigta       | PU nustatytas kaip galutinis. Dabar jis yra finansiškai uždarytas ir jo nebegalima keisti. | Ne                        |

## <a name="confirming-purchase-orders"></a>Pirkimo užsakymų patvirtinimas
Gali reikėti atlikti papildomų veiksmų, norint patvirtinti PU, kurių patvirtinimo būseną yra **Patvirtinta**. Pavyzdžiui, jums gali tekti tiekėjui pateikti pirkimo užklausą apie kainas, nuolaidas arba pristatymo datas. Šiuo atveju galite nustatyti PU būseną kaip **Išorinė peržiūra**, naudodami veiksmą **Pirkimo užklausa**.  

Tiekėjai, kuriems nustatyta galimybė naudoti tiekėjo portalą, portale gali užsakymus peržiūrėti ir patvirtinti arba atmesti. Šio peržiūros proceso metu PU būsena yra **Išorinė peržiūra**. Tiekėjų portalą galima sukonfigūruoti taip, kad, užsakymą patvirtinus tiekėjui, jis būtų automatiškai patvirtintas sprendime „Finance and Operations“. Arba jūs galite neautomatiniu būdu patvirtinti PU, kai tiekėjas jį patvirtina. Jei tiekėjas PU atmeta, apie atmetimą informuojama nurodant atmetimo priežastį ir keitimų pasiūlymus. Tokiu atveju PU būsena lieka **Išorinė peržiūra**.  

Taip pat galima generuoti išankstinį užsakymo patvirtinimą, prieš apdorojant faktinį patvirtinimą. Naudojant šią parinktį sukuriama ataskaita, kurią galite bendrinti su tiekėju. Jokia žurnalo informacija nesukuriama.  

Po to, kai tiekėjas patvirtina užsakymą, kitu veiksmu PU įrašomas kaip užfiksuotas. Šį veiksmą galite atlikti naudodami veiksmą **Patvirtinimas** arba **Patvirtinti**. Naudojant abu veiksmus užsakymo patvirtinimo būsena nustatoma kaip **Patvirtinta**. Patvirtinus įsakymą inicijuojami du papildomi procesai.

-   Sukuriamas žurnalas, skirtas tiksliai patvirtinto užsakymo kopijai sistemoje saugoti. Kartais užsakymus reikia keisti ir patvirtinus atnaujintą užsakymą sukuriami papildomi žurnalai. Šiuose žurnaluose galima peržiūrėti įvairių patvirtintų užsakymo versijų retrospektyvą.
-   Sukuriami apskaitos paskirstymai ir vykdomi užsakymo bei biudžeto tikrinimai, jei ši funkcija įjungta. Jei kuris nors patikrinimas nepavyksta, rodomas klaidos pranešimas, nurodantis, kad prieš patvirtinant PU reikia atlikti keitimų.

Tiekėjas gali prašyti kokio nors tipo garantijos, kad už pirkimą bus sumokėta. Šią garantiją suteikti naudojant mokėtinų sumų procesus galima įvairiais būdais. Pvz., veiksmu **Išankstinis mokėjimas** rezervuojamos PU lėšos ir šis išankstinis mokėjimas yra užregistruojamas PU.

## <a name="changing-purchase-orders"></a>Pirkimo užsakymų keitimas
Kai kuriais atvejais gali reikėti PU pakeisti po to, kai jo būsena buvo nustatyta kaip **Patvirtinta** arba **Patvirtinta**.  

Jei PU buvo sukurtas vykdant pakeitimų valdymo procesą, keitimus galite atlikti užsakymą atšaukdami arba, jei užsakymas jau buvo patvirtintas, naudodami veiksmą **Reikalauti keitimo**. Tokiu atveju patvirtinimo būsena vėl pakeičiama į **Juodraštis** ir tada užsakymą tada galite keisti. Atlikus keitimus, gali reikėti PU pateikti pakartotinai patvirtinti. Pakeitimų, kuriuos atlikus užsakymą reikia pakartotinai patvirtinti, tipus galite naudodami puslapio **Pirkimo užsakymų pakartotinio patvirtinimo taisyklė** veiksmą **Pirkimo strategijos**.  

Jei pristatyta užsakyto PO eilutės kiekio dalis, užsakyto kiekio keisti negalima. Tačiau eilutėje galite keisti kiekį **Pristatymo likutis**. Tada galite naudoti veiksmą **Baigti**, norėdami atšaukti eilutės ir neleisti toliau apdoroti 

Patvirtinus užsakymą jo panaikinti nebegalima. Tačiau užsakyme galite atšaukti visą kiekį ar bet kokį likusį kiekį,ji kiekis nebuvo gautas arba neišrašyta jo SF.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pirkimo užsakymo apžvalga](purchase-order-overview.md)

[Pirkimo užsakymo kūrimas](purchase-order-creation.md)

[Produkto gavimas pagal pirkimo užsakymą](product-receipt-against-purchase-orders.md)

[Tiekėjo SF apžvalga](../../financials/accounts-payable/vendor-invoices-overview.md)




