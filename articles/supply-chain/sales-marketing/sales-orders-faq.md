---
title: Dažnai užduodami klausimai apie pardavimo užsakymus
description: Šiame puslapyje adresai dažnai užduodami klausimai, kurie ateina dirbant su pardavimo „Dynamics 365 Supply Chain Management“ užsakymais.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477083"
---
# <a name="sales-order-faqs"></a>Pardavimo užsakymo DUK

Šiame puslapyje adresai dažnai užduodami klausimai, kurie ateina dirbant su pardavimo „Dynamics 365 Supply Chain Management“ užsakymais.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Ar galiu susieti pirkimo užsakymą su pardavimo užsakymu, siekiant įvykdyti paklausą?

Galite sukurti pirkimo užsakymą naudojant pardavimo užsakymą. Norėdami gauti daugiau informacijos, žr. [Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Ar galiu atšaukti ar panaikinti prekybos užsakymą ar grąžinimo užsakymą?

Galite atšaukti tik pardavimo užsakymus ir grąžinimo užsakymus, kurie yra būsenoje *Sukurta*. Norėdami gauti daugiau informacijos, žr. [Grąžinimo užsakymo atšaukimas](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Ar galiu atkurti panaikintą pardavimo užsakymą, kurio SF jau išrašyta?

Jei pardavimo užsakymas, kurio SF jau išrašyta, buvo panaikintas per klaidą ir Jūs norite jį atkurti arba peržiūrėti jo informaciją.

Eikite į **kliento sąskaitos \>operacijų \> pradinio dokumento \> peržiūros informaciją**. Suraskite ieškomą SF ir pasirinkite ją, kad peržiūrėtumėte išsamią informaciją. Ši informacija apima pardavimo užsakymo nuorodą. Taip pat turėtumėte turėti prieigą prie pardavimo užsakymo informacijos tame puslapyje.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Kaip man panaikinti pavienius pardavimo užsakymų įrašus?

Norėdami išvalyti pavienius pardavimo užsakymų įrašus, vykdykite *Pardavimo užsakymo panaikinimas* periodinę užduotį, apsilankę vienoje iš šių vietų:

- Pardavimas ir rinkodara \> Periodinės užduotys \> Valymas \> Naikinti pardavimo užsakymus
- Mažmeninė prekyba ir prekyba \> IT mažmeninė prekyba ir prekyba \> Valymas \> Naikinti pardavimo užsakymus

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Ar yra būdas apskaičiuoti jau užregistruotų SF komisinius?

„Supply Chain Management“ šiuo metu nepalaiko užregistruotų SF komisinių skaičiavimo.
