---
title: Pardavimo užsakymų trikčių šalinimas
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo užsakymais.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 8f4a28b0cf47ec1c2534fc97c4dee6790fa6c51637bddf64caa7147e9ce6d6db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746117"
---
# <a name="troubleshoot-sales-orders"></a>Pardavimo užsakymų trikčių šalinimas

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo užsakymais.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Mokesčių informacija nėra atnaujinama, jei pakeisiu vietą pardavimo užsakymo antraštėje.

### <a name="issue-description"></a>Problemos aprašas

Jei vieta, sandėlis arba pristatymo adresas pakeistas pardavimo užsakymo antraštėje arba eilutės lygiu, šiuo atveju mokesčių informacija nėra automatiškai atnaujinama eilutėse.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Problema kyla dėl to, kad pristatymo adresas, vieta ir sandėlis taip pat nėra automatiškai keičiami eilutės lygiu. Turite juos atnaujinti rankiniu būdu.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Jei tam pačiam laikotarpiui ar persidengiantiems laikotarpiams yra dvi prekybos sutartys, visada pasirenkama ta pati sutarties eilutė.

### <a name="issue-description"></a>Problemos aprašas

Jei tam pačiam laikotarpiui ar persidengiantiems laikotarpiams yra nustatytos dvi prekybos sutartys, atrodo, kad ta pati prekybos sutartis pasirenkama kiekvieną kartą, kai sukuriate pardavimo užsakymo eilutes, kuriose yra tos prekės.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jei nurodytą datą yra daugiau nei viena prekybos sutartis, visada pasirenkama prekybos sutartis, turinti žemiausią kainą. Norėdami gauti daugiau informacijos, atsisiųskite šią techninę dokumentaciją: [Prekybos sutartys „Microsoft Dynamics AX” 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Ar galiu susieti pirkimo užsakymą su pardavimo užsakymu, siekiant įvykdyti paklausą?

Galite sukurti pirkimo užsakymą naudojant pardavimo užsakymą. Norėdami gauti daugiau informacijos, žr. [Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Negaliu atšaukti arba panaikinti grąžinimo užsakymą arba pardavimo užsakymą.

Galite atšaukti tik pardavimo užsakymus ir grąžinimo užsakymus, kurie yra būsenoje *Sukurta*. Norėdami gauti daugiau informacijos, žr. [Grąžinimo užsakymo atšaukimas](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Bandant atšaukti pardavimo užsakymą, gaunu „Rezervacijų šalinti negalima, nes sukurtas šiomis rezervacijomis grindžiamas darbas” klaidos pranešimą.

Klaidos kodas: WAX4661

Jei darbas susietas su pardavimo užsakymu, negalite atšaukti pardavimo užsakymo, kol darbas nebus atšauktas. Šis reikalavimas taikomas, net jei darbas, susietas su pardavimo užsakymu, yra uždarytas.

Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.

1. Atšaukite darbą ir grąžinkite atsargas į norimą vietą. Eikite prie atitinkamo pardavimo užsakymo krovinio ir pasirinkite arba **Sumažinti paimtą kiekį** krovinio eilutėje, arba **Atšaukti darbą** veiksmų srityje.

    Dabar darbo būsena yra *Atšaukta*, o naujas atsargų perkėlimo darbas automatiškai sukuriamas ir apdorojamas, siekiant sugrąžinti atsargas į vietą, kuri buvo aprašyta atšaukimo metu.

2. Panaikinkite krovinį. Siunta taip pat panaikinama.
3. Dabar turėtumėte galėti nueiti į pardavimo užsakymą ir jį atšaukti.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Negaliu atšaukti vidinės įmonės pirkimo užsakymo, susieto su pardavimo užsakymu.

### <a name="issue-description"></a>Problemos aprašas

Jei mėginsite atšaukti vidinės įmonės pirkimo užsakymą, susietą su pardavimo užsakymu, galite gauti tokį klaidos pranešimą: „Kiekio sumažinti negalima, nes pasikeis likusio atnaujinto kiekio ženklas.”

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši problema buvo išspręsta „Microsoft Dynamics 365 Supply Chain Management” versijoje 10.0.13. Šioje versijoje ir vėlesnėse versijose dabar galite atšaukti vidinės įmonės pirkimo užsakymą, kuris yra susijęs su pardavimo užsakymu.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Ar galiu atkurti panaikintą pardavimo užsakymą, kurio SF jau išrašyta?

### <a name="issue-description"></a>Problemos aprašas

Pardavimo užsakymas, kurio SF jau išrašyta, buvo panaikintas per klaidą ir Jūs norite jį atkurti arba peržiūrėti jo informaciją.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jeigu panaikintam pardavimo užsakymui jau išrašyta SF, eikite į **Kliento sąskaita \> Operacijos \> Originalus dokumentas \> Rodinio informacija**. Suraskite ieškomą SF ir pasirinkite ją, kad peržiūrėtumėte išsamią informaciją. Ši informacija apima pardavimo užsakymo nuorodą. Taip pat turėtumėte turėti prieigą prie pardavimo užsakymo informacijos tame puslapyje.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Pardavimo užsakymo antraštės galutinis terminas nerastas „SalesOrderHeaderV2Entity” duomenų objekte.

*SalesOrderHeaderV2Entity* objektui galutinio termino lauko nėra.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Privalau panaikinti pavienius pardavimo užsakymų įrašus.

Norėdami išvalyti pavienius pardavimo užsakymų įrašus, vykdykite *Pardavimo užsakymo panaikinimas* periodinę užduotį, apsilankę vienoje iš šių vietų:

- Pardavimas ir rinkodara \> Periodinės užduotys \> Valymas \> Naikinti pardavimo užsakymus
- Mažmeninė prekyba ir prekyba \> IT mažmeninė prekyba ir prekyba \> Valymas \> Naikinti pardavimo užsakymus

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Ar yra būdas apskaičiuoti jau užregistruotų SF komisinius?

„Supply Chain Management“ šiuo metu nepalaiko užregistruotų SF komisinių skaičiavimo.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Vidinės įmonės procese nepalaikomas paketo elementas.

Paketo elementas negalimas pirkimo užsakyme, nes, jei patikrinsite paketo elemento pardavimo užsakymo eilutes, pastebėsite, kad kiekis yra *0* (nulis), o būsena *Atšaukta*. Toks veikimo būdas yra numatytas. Pardavimo užsakymas perka tik paketo elemento komponentus. Jis neperka pačio paketo elemento.

Jei privalote įsigyti paketą, apsvarstykite, ar reikės jį pažymėti kaip paketo elementą, nes šis funkcionalumas yra skirtas pelno atpažinimo scenarijams. Daugiau informacijos apie paketo elementus žr. [Paketai](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]