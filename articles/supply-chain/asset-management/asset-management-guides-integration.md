---
title: „Dynamics 365 Supply Chain Management“ (Turto valdymas) integravimas su „Dynamics 365 Guides“
description: Šioje temoje paaiškinama, kaip integruoti „Microsoft Dynamics 365 Supply Chain Management“ modulį „Turto valdymas“ į „Dynamics 365 Guides“, kad kasdienėse paslaugose ir priežiūros darbo eigose būtų galima pasinaudoti mišriosios realybės vadovų teikiamomis galimybėmis.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 3793dca681e28b90e96469256f368620393704f2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344275"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>„Dynamics 365 Supply Chain Management“ (Turto valdymas) integravimas su „Dynamics 365 Guides“

„Microsoft Dynamics 365 Supply Chain Management“ modulį **Turto valdymas** galite integruoti į „Dynamics 365 Guides“, kad kasdienėse paslaugose ir priežiūros darbo eigose galėtumėte pasinaudoti mišriosios realybės vadovų teikiamomis galimybėmis. Jei vadovas yra susietas su modulio „Turto valdymas“ darbo užsakymu, darbuotojas, kuris „Supply Chain Management“ („Dynamics 365“) mobilioje programoje atidaro darbo užsakymo prižiūrimo turto kontrolinį sąrašą, mato, kad vadovas yra pasiekiamas. Tada darbuotojas gali rasti ir atidaryti vadovą „Dynamics 365 Guides HoloLens“ programoje.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami pridėti vadovus modulio „Turto valdymas“ darbo užsakymų, turite atlikti toliau nurodytas būtinas užduotis.

- [Sukonfigūruokite „Dynamics 365 Supply Chain Management“](../../fin-ops-core/fin-ops/index.md) 10.0.9 arba naujesnę versiją.
- [„Supply Chain Management“ programoms įjunkite dvigubą rašymą](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Įjunkite testuojamą variantą](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** funkcijai. (Gamybos aplinkose pirmiausia turite pateikti palaikymo bilietą, kad jūsų nuomotojas būtų įtrauktas į testuojamo varianto grupę.)
- [Įjunkite toliau nurodytus konfigūracijos raktus](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) puslapyje **Licencijos konfigūracija**:

    - Turto valdymas \> Turto valdymo mišrioji realybė
    - Mišrioji realybė \> Mišriosios realybės vadovas

- [Sukonfigūruokite „Dynamics 365 Guides“](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 arba naujesnę versiją.

## <a name="use-dynamics-365-guides-with-asset-management"></a>„Dynamics 365 Guides“ naudojimas su moduliu „Turto valdymas“

Vadovui susieti, modulyje „Turto valdymas“ naudojama prižiūrimo turto kontrolinio sąrašo eilutė. Susiejimą galite sukurti naudodami prižiūrimo turto kontrolinio sąrašo šabloną, priežiūros užduoties tipą arba darbo užsakymą, nes visuose trijuose yra prižiūrimo turto kontrolinio sąrašo eilutės. Naudodami šabloną galite sutaupyti laiko, nes šablonas gali būti susietas su visais priežiūros užduočių tipais, kuriuos jis naudoja. Pavyzdžiui, vadovas, kuris yra susietas su priežiūros užduoties tipu, automatiškai susiejamas su visais darbo užsakymais, kurie nurodo tą užduoties tipą. Kita vertus, tiesiogiai su darbo užsakymu susietas vadovas yra skirtas tik tam darbo užsakymui.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo šablonu

Norėdami susieti vadovą su prižiūrimo turto kontrolinio sąrašo šablonu, atlikite toliau nurodytus veiksmus.

1. Sukurkite vadovą naudodami „Dynamics 365 Guides“ kompiuterio ir „HoloLens“ programas. Daugiau informacijos, kaip kurti vadovą, žr. tolesnėse temose.

    - [Kompiuterio programos naudojimas vadovui kurti](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [„HoloLens“ programos naudojimas hologramoms uždėti](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. [Sukurkite prižiūrimo turto kontrolinio sąrašo šabloną](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) programoje „Supply Chain Management“.
1. Susiekite vadovą, kurį sukūrėte prižiūrimo turto kontrolinio sąrašo eilutėje, naujame prižiūrimo turto kontrolinio sąrašo šablone.

    1. „FastTab“ konteineryje **Prižiūrimo turto sąrašo eilutės** pasirinkite eilutę, su kuria norite susieti vadovą.
    1. „FastTab“ konteineryje **Susieti vadovai** pasirinkite **Įtraukti vadovą**.

        ![Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo eilute.](media/am-guides-integration-add-guide.png "Vadovo susiejimas su prižiūrimo turto kontrolinio sąrašo eilute")

    1. Lauke **Pavadinimas** pasirinkite vadovą, tada – **Įrašyti**.

        ![Lauke Pavadinimas pasirinkite vadovą.](media/am-guides-integration-select-guide.png "Lauke Pavadinimas pasirinkite vadovą")

1. Susiekite prižiūrimo turto kontrolinio sąrašo šabloną su užduoties tipu.

    1. [Sukurkite priežiūros užduoties tipą ](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) arba pasirinkite esamą priežiūros užduoties tipą.
    1. Veiksmų srityje pasirinkite **Priežiūros užduoties tipo numatytosios reikšmės**.

        ![Mygtukas Priežiūros užduočių tipų numatytosios reikšmės.](media/am-guides-integration-job-defaults.png "Mygtukas Priežiūros užduočių tipų numatytosios reikšmės")

    1. Sukurkite eilutę ir pasirinkite **Įrašyti**.

        ![Sukurkite eilutę.](media/am-guides-integration-add-line.png "Kurti eilutę")

    1. Veiksmų srityje pasirinkite **Prižiūrimo turto kontrolinis sąrašas**.

        ![Mygtukas Prižiūrimo turto kontrolinis sąrašas.](media/am-guides-integration-maintenance-checklist.png "Mygtukas Prižiūrimo turto kontrolinis sąrašas")

    1. „FastTab“ konteineryje **Prižiūrimo turto kontrolinio sąrašo eilutės** pridėkite eilutę, tada pakeiskite lauko **Tipas** reikšmę į **Šablonas**.

        ![Keisti lauko Tipas reikšmę.](media/am-guides-integration-checklist-lines.png "Keisti lauko Tipas reikšmę")

    1. „FastTab“ konteinerio **Išsami eilutės informacija** lauke **Šablonas** pasirinkite šabloną, su kuriuo susiejote vadovą, tada pasirinkite **Įrašyti**.

        ![Pasirinkti šabloną.](media/am-guides-integration-checklist-line-details.png "Pasirinkti šabloną")

1. [Sukurkite darbo užsakymą](work-orders/manually-created-workorders.md#create-work-order), tada pasirinkite priežiūros užduoties tipą, kuris naudoja prižiūrimo turto kontrolinio sąrašo šabloną, su kuriuo susiejote vadovą. Vadovas automatiškai susiejamas su darbo užsakymu.

    ![Pasirinkti priežiūros užduoties tipą.](media/am-guides-integration-create-work-order.png "Pasirinkti priežiūros užduoties tipą")

1. Norėdami peržiūrėti vadovą, susietą su darbo užsakymu ir darbuotojais, atlikite toliau aprašytus veiksmus.

    1. Norėdami pasiekti darbo užsakymą, atidarykite [Turto valdymo mobilioji darbo sritis](asset-management-mobile-workspace.md).
    1. [Atidarykite darbo užsakymo prižiūrimo turto kontrolinį sąrašą](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).
    1. Pasirinkite kontrolinio sąrašo eilutę, kad pamatytumėte susietą vadovą.

        ![Vadovas, susietas su kontrolinio sąrašo eilute.](media/am-guides-integration-show-guide.png "Vadovas, susietas su kontrolinio sąrašo eilute")

    1. Atidarykite vadovą „HoloLens“.

        ![Atidaryti vadovą „HoloLens”.](media/am-guides-integration-hololens-select.png "Atidaryti vadovą „HoloLens“")

> [!NOTE]
> Vadovą taip pat galite tiesiogiai susieti darbo užsakymo arba užduoties tipo prižiūrimo turto kontroliniame sąraše.

> [!IMPORTANT]
> Yra žinoma problema, kai susiejus prižiūrimo turto kontrolinio sąrašo šabloną su numatytuoju priežiūros užduoties tipu, su šablonu susietas vadovas nerodomas puslapio **Priežiūros užduočių tipų numatytosios reikšmės** „FastTab“ konteineryje **Susieti vadovai**. Tačiau vadovas bus rodomas po to, kai tas užduoties tipas bus pritaikytas darbo užsakymui „FastTab“ konteineryje **Susieti vadovai**.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Dvigubo rašymo apžvalga](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Išteklių valdymo apžvalga](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]