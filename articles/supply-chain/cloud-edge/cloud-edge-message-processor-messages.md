---
title: Pranešimų procesoriaus pranešimai
description: Šiame straipsnyje pateikiama informacija apie pranešimų procesoriaus pranešimų funkciją, siekiant nustatyti skalės vieneto darbo krūvius.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a5f8d48ba697df389150f70ac159e690156de33b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893619"
---
# <a name="message-processor-messages"></a>Pranešimų procesoriaus pranešimai

[!include [banner](../includes/banner.md)]

Pranešimų procesoriaus pranešimai naudojami, kai paleisti debesies ir kraštų [skalės vienetai, skirti gamybos darbo krūviui](cloud-edge-workload-manufacturing.md) ir [sandėlio valdymo darbo](cloud-edge-workload-warehousing.md) krūviui.

Centro ir skalės vieneto diegimo aplinkos keičiasi dideliu duomenų kiekiu, kad išliktų sinchronizuoti. Kai kurie duomenų mainai suaktyvins papildomą pranešimų procesoriaus *logiką*. Galite peržiūrėti pranešimus, kuriuos apdorojo pranešimų procesorius, **nueię į sistemos administravimą > procesorių ir > procesoriaus pranešimus**.

## <a name="message-grid-columns-and-filters"></a>Pranešimų tinklelio stulpeliai ir filtrai

Galite naudoti laukus pranešimų procesoriaus pranešimų puslapio viršuje, norėdami **padėti** rasti visus konkrečius jūsų ieškomus pranešimus. Dauguma šių filtrų atitinka pranešimų tinklelio stulpelių antraštes. Galimi šie filtrai ir stulpelių antraštės:

- **Pranešimo** tipas – nurodo pranešimo tipą.
- **Pranešimų eilė** – nurodo eilės, kurioje bus apdorojamas pranešimas, pavadinimą. Pateiktos šios eilės:
  - *Skalės vienetas koncentratoriui*
  - *Iš telkinio į sandėlį vykdymo skalės vienetas*
  - *Telkinys, skirtas gamybos vykdymo skalės vienetui*
- **Pranešimo** būsena – nurodo pranešimo būseną. Yra tokios būsenos:
  - *Eilėje* – pranešimą gali apdoroti pranešimų procesorius.
  - *Apdorotos* – pranešimas buvo sėkmingai apdorotas pranešimo tvarkytojo.
  - *Atšaukta –* pranešimas buvo apdorotas, bet apdoroti nepavyko.
- **Pranešimo turinys** – Šis filtras atlieką visą teksto paiešką pagal pranešimo turinį. (Pranešimo turinys nerodomas tinklelyje.) Filtras kaip tarpus traktuoja svarbiausius simbolius (pvz., „-") ir visus tarpų simbolius traktuoja kaip „Boolean“ AR operatorius. T=Pvz., tai reiškia, kad ieškosite konkrečios vertės, lygios `journalid` „USMF-123456", sistema surasti visus pranešimus, kuriuose yra „USMF" arba „123456", kurie tikriausiai bus ilgas sąrašas. Todėl būtų geriau tik įvesti „123456", nes taip bus pateikti išsamesni rezultatai.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Pavyzdinio pranešimo tipas: Prašyti atsargų koregavimo finansinio atnaujinimo

Pavyzdžiui, pranešimo tipas Reikalauti atsargų koregavimo finansinio atnaujinimo naudojamas kuriant ir registruojant inventorizacijos žurnalą centre, kai darbuotojas naudoja sandėlio programą atsargų koregavimui dėl svarstyklių vieneto valdymo **darbo** *krūvio* [registruoti](cloud-edge-warehouse-inventory-adjustment.md). Kadangi šis konkretus procesas kyla iš svarstyklių vieneto, pranešimų eilės lauke svarstyklių **vienetas** *bus rodomas kaip svarstyklių vienetas ir* centras.

Šiam pranešimo tipui skalės vieneto darbo krūvis įrašo pranešimą kaip sandėlio programos atsargų koregavimo operacijos dalį. Tada pranešimo duomenys perkeliami į tą patį procesą, naudojamą [„Commerce Data Exchange" architektūroje](../../commerce/commerce-architecture.md). Pranešimas bus atnaujintas, kad būtų rodoma **pranešimo būsena** darbo *eilėje*. Tada pranešimų procesorius bando apdoroti pranešimą ir atnaujina pranešimo būseną į Apdorota sėkmingai arba **Atšaukta** *trikties* *metu*.

## <a name="view-the-message-log-message-content-and-details"></a>Peržiūrėti pranešimų žurnalą, pranešimų turinį ir informaciją

Išsamią informaciją apie pranešimą galite rasti pasirinkę jį tinklelyje ir atidarydami žurnalo arba pranešimo turinio skirtukus pranešimų tinklelyje, kuriame rodomas kiekvienas **apdorojimo** **įvykis**.

Pranešimo **turinys priklauso nuo pranešimo** **tipo, todėl jo teksto ilgis bus** skirtingas. Įprastas pranešimo turinio tekstas prasidės su a **{** ir baigsis su a **}** tuo tarpu tarp jų bus laukelių pavadinimai, tokie kaip `journalId` ir vėliau a **:** ir vertė, tokia kaip *USMF-123456*.

Žurnalo skirtuke **esančioje** įrankių juostoje yra šie mygtukai:

- **Žurnalas** – rodo apdorojimo rezultatus. Tai ypač naudinga norint suprasti pranešimų, kurių apdorojimo rezultatas yra **Nepavyko,** apdorojimo *trikties* priežastis.
- **Grupavimas** – kelios pranešimų apdorojimo operacijos gali būti paleidžiaos kaip to paties paketinio vykdymo dalis. Pasirinkite šį mygtuką, jei norite peržiūrėti visus duomenis. Pavyzdžiui, galite pamatyti, ar yra priklausomybių, kurioms sistema reikalauja apdoroti konkrečius pranešimus tam tikra seka.

## <a name="message-processor-batch-job"></a>Pranešimų procesoriaus paketinė užduotis

Paleidus paskirstytą hibridinę topologiją su skalės vienetais, *Pranešimo tvarkyklės* bendra užduotis automatiškai bus iškviesta, kai naujas pranešimas bus sukuriamas siekiant sutvarkyti, todėl Jums nereikėtų suplanuoti šio darbo rankiniu būdu.

Jei reikia, paketinę užduotį galite pasiekti nueię į Sistemos administravimas **> Pranešimų procesorius > Pranešimų** procesorius.

## <a name="manually-process-or-cancel-a-message"></a>Pranešimo apdorojimas rankiniu būdu arba atšaukimas

Jei reikia, galite neautomatiniu būdu apdoroti arba atšaukti pranešimą, priklausomai nuo dabartinės jo būsenos. Norėdami tai padaryti, pasirinkite tinklelyje rodoimą pranešimą ir veiksmų **srityje pasirinkite Procesas** arba **Atšaukti**

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Nustatyti verslo įvykius, kurie turėtų pateikti įspėjimus dėl nesėkmingų rezultatų

Be filtravimo pranešimo būsenos reikšmės Atšaukta, kad būtų galima pateikti užklausą dėl nepavykusių pranešimų, galite nustatyti centro verslo įvykius, kad įspėtų jus **apie** *nesėkmingus* [rezultatus](../../fin-ops-core/dev-itpro/business-events/home-page.md). Norėdami tai padaryti, suaktyvinkite verslo įvykio, pavadinto *Pranešimų procesoriaus pranešimas* apdorotą **Verslo įvykių katalogo** puslapį (**Sistemos administravimas > Sąranka > Verslo įvykiai > Verslo įvykių katalogas**).

Kaip aktyvinimo proceso dalį jūs nurodysite, ar įvykis yra konkretus vienam ar visiems juridiniams subjektams ir pateikite galinio punkto pavadinimą, kurį **pirmiausia** reikia apibrėžti.

>[!NOTE]
> Jei **Numatytas verslo įvykis atsitinka** yra nustatytas į *„Microsoft Power Automate“* (o ne į *HTTPS*, pavyzdžiui), **Galutinio taško pavadinimas** bus automatiškai sukuriamas „Supply Chain Management“ pagal *„Microsoft Power Automate“* nustatymus.

### <a name="microsoft-power-automate-example"></a>Pavyzdys: „Microsoft Power Automate“

Šiame pavyzdyje naudokite Kai verslo įvykis įvyksta išsiunčiant el. laiškus, kuriuose yra Sistemos pranešimo pranešimai ir hipersaitai, kad atidarytumėte pranešimo procesoriaus pranešimų puslapį, skirta tam tikro nepavykusio pranešimo **pranešimą** diegiant *Microsoft Power Automate* **centrą**. Jei reikia, galite pridėti papildomą logiką, kad pranešimai būtų išsiunčiami lygiagrečiai, naudojant skirtingus kanalus ir valdyti gavėjus, remiantis įvykio duomenimis.

1. [„Power Automate“](https://preview.flow.microsoft.com), sukurkite naują automatizuotą debiesies srautą srauto paleidikliui **Įvykus veiklos įvykiui - „Fin & Ops App“ („Dynamics 365“)** po kurios seka **„Parse JSON“** ir **Siųsti el. laišką** veiksmus, kaip parodyta tolesniame paveikslėlyje.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatizuotas debesies srautas.":::

1. Kai verslo įvykis įvyksta, galite peržiūrėti ar įvesti centro egzempliorių pagal kategoriją ir tada apdorojamas verslo įvykio pranešimų procesoriaus pranešimas, kaip parodyta toliau pateiktame **kaip** **parodyta** **toliau** **pateiktame** *pavyzdyje*.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Kai vyksta verslo įvykis, veiksmas.":::

1. Įveskite **veiksmą Parse** JSON, **schemą,** apibrėžiaą išplėstinius laukus. Galite naudoti atsisiuntimo schemos parinktį verslo įvykių katalogo puslapyje „Supply Chain Management“ arba *pradėti* įklijuodami **į** pavyzdinį schemos tekstą. Šis pavyzdis tekstas pateikiamas po šio pavyzdyje.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Išanalizuoti JSON veiksmą.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. El. laiško siuntimo veiksme galite pasirinkti atskirus laukus arba pradėti įklijuodami el. **laiško** pranešimo pavyzdį į **lauką** Tekstas. Šis pavyzdis tekstas pateikiamas po šio pavyzdyje.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate el. laiško siuntimo veiksmas.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Įrašant verslo įvykį, jis bus automatiškai suaktyvintas ir paruoštas naudoti kaip „Supply Chain Management“ dalis.
