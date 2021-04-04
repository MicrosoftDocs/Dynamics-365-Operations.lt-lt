---
title: Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti dvigubo rašymo pardavimo užsakymo būsenos stulpelius.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: ecf26a2a697fa4d0485c1904041692a6c10ce9c3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560414"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas

[!include [banner](../../includes/banner.md)]

Stulpeliai, nurodantys pardavimo užsakymo būseną, turi skirtingas išvardijimo vertes „Microsoft Dynamics 365 Supply Chain Management” ir „Dynamics 365 sales” programose. Būtini papildomi nustatymai, norint susieti stulpelius dvigubame rašyme.

## <a name="columns-in-supply-chain-management"></a>„Supply Chain Management“ stulpeliai

„Supply Chain Management“ dviejuose stulpeliuose nurodoma pardavimo užsakymo būsena. Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Dokumento būsena**.

**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną. Ši būsena rodoma užsakymo antraštėje.

**Būsenos** išvardijimas turi šias reikšmes:

- Atviras užsakymas
- Pristatyta
- Išrašyta SF
- Atšaukta

**Dokumento būsenos** išvardijimas nurodo vėliausią dokumentą, sugeneruotą užsakymui. Pavyzdžiui, jei užsakymas patvirtintas, šis dokumentas yra pardavimo užsakymo patvirtinimas. Jei pardavimo užsakymas yra dalinai išrašyta SF, o tada likusi eilutė patvirtinama, dokumento būsena lieka **SF**, nes vėliau vykstančiame procese SF sugeneruojama.

**Dokumento būsenos** išvardijimas turi šias reikšmes:

- Patvirtinimas
- Išrinkimo dokumentas
- Važtaraštis
- PVM sąskaita faktūra

## <a name="columns-in-sales"></a>Pardavimų stulpeliai

Pardavimuose du stulpeliai nurodo užsakymo būseną. Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Apdorojimo būsena**.

**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną. Jam būdingos šios reikšmės:

- Aktyvūs
- Pateikta
- Įvykdyta
- Išrašyta SF
- Atšaukta

**Apdorojimo būsenos** išvardijimas buvo įvestas tam, kad būseną būtų galima tiksliau susieti su „Supply Chain Management“.

Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas „Supply Chain Management“.

| Apdorojimo būsena   | Būsena „Supply Chain Management“ | Dokumento būsena „Supply Chain Management“ |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktyvūs              | Atviras užsakymas                        | None                                       |
| Pritarta           | Atviras užsakymas                        | Patvirtinimas                               |
| Paimta              | Atviras užsakymas                        | Išrinkimo dokumentas                               |
| Iš dalies pristatyta | Atviras užsakymas                        | Važtaraštis                               |
| Pristatyta           | Pristatyta                         | Važtaraštis                               |
| Iš dalies išrašyta SF  | Pristatyta                         | PVM sąskaita faktūra                                    |
| Išrašyta SF            | Išrašyta SF                          | PVM sąskaita faktūra                                    |
| Atšaukta           | Atšaukta                         | Netaikoma                             |

Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas tarp pardavimų ir „Supply Chain Management“.

| Apdorojimo būsena   | Būsena pardavimuose | Būsena „Supply Chain Management“ |
|---------------------|-----------------|-----------------------------------|
| Aktyvūs              | Aktyvūs          | Atviras užsakymas                        |
| Pritarta           | Pateikta       | Atviras užsakymas                        |
| Paimta              | Pateikta       | Atviras užsakymas                        |
| Iš dalies pristatyta | Aktyvūs          | Atviras užsakymas                        |
| Iš dalies išrašyta SF  | Aktyvūs          | Atviras užsakymas                        |
| Iš dalies išrašyta SF  | Įvykdyta       | Pristatyta                         |
| Išrašyta SF            | Išrašyta SF        | Išrašyta SF                          |
| Atšaukta           | Atšaukta       | Atšaukta                         |

## <a name="setup"></a>Sąranka

Norėdami nustatyti pardavimo užsakymo būsenos stulpelių susiejimą, turite įgalinti **IsSOPIntegrationEnabled** ir **isIntegrationUser** atributus.

Norėdami įgalinti **IsSOPIntegravimasĮjungtas** atributą, atlikite toliau pateiktus veiksmus.

1. Žiniatinklio naršyklėje eikite į `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Pakeiskite **\<test-name\>** savo įmonės saitu į pardavimus.
2. Atidarytame puslapyje suraskite **OrganizacijosID** ir atkreipkite dėmesį į vertę.

    ![Organizacijos ID radimas](media/sales-map-orgid.png)

3. Dalyje Pardavimai atsidarykite naršyklės konsolę ir vykdykite šį scenarijų. Naudokite **OrganizacijosID** vertę nuo 2 veiksmo.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![„JavaScript” kodas naršyklės konsolėje](media/sales-map-script.png)

4. Patikrinkite, ar **IsSOPIntegravimasĮjungtas** yra nustatytas kaip **teisingas**. Naudokite URL, kurį nurodėte 1 veiksme, kad patikrintumėte vertę.

    ![IsSOPIntegravimasĮjungtas yra nustatytas kaip teisingas.](media/sales-map-integration-enabled.png)

Norėdami įgalinti **isVartotojoIntegravimas** atributą, atlikite toliau pateiktus veiksmus.

1. Dalyje Pardavimai eikite į **Parametrai \> Tinkinimas \> Tinkinti sistemą**, pasirinkite **Vartotojo lentelė** ir tada atidarykite **Forma \> Vartotojas**.

    ![Vartotojo formos atidarymas](media/sales-map-user.png)

2. Laukų naršyklėje suraskite **Integravimo vartotojo režimas** ir du kartus spustelėkite jį, kad įtrauktumėte į formą. Įrašykite savo pakeitimą.

    ![Vartotojo režimo stulpelio integravimo į formą pridėjimas](media/sales-map-field-explorer.png)

3. Dalyje Pardavimai eikite į **Parametras \> Sauga \> Vartotojai** ir pakeiskite rodinį iš **Įgalinti vartotojai** į **Taikomosios programos vartotojai**.

    ![Rodinio keitimas iš „Įgalinti vartotojai” į „Taikomosios programos vartotojai”](media/sales-map-enabled-users.png)

4. Pasirinkite du **DviguboRašymo VartotojoIntegravimas** įrašus.

    ![Taikomosios programos vartotojų sąrašas](media/sales-map-user-mode.png)

5. Pakeiskite vertę į **Integravimo vartotojo režimas** stulpelį į **Taip**.

    ![Integravimo vartotojo režimo stulpelio vertės pakeitimas](media/sales-map-user-mode-yes.png)

Dabar Jūsų pardavimo užsakymai yra susieti.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]