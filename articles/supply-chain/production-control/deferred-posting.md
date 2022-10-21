---
title: Padarykite užbaigtas prekes fiziškai prieinamas prieš paskelbdami žurnaluose
description: Kai pagaminta prekė paskelbiama baigta, ji užregistruojama kaip galima toliau fiziškai apdoroti ir registruojamas vienas ar daugiau žurnalų. Šiame straipsnyje aprašoma, kaip atidėti žurnalo registravimus, įgalinus juos apdoroti pranešimų eilėje esančią paketinę užduotį.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689346"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Padarykite užbaigtas prekes fiziškai prieinamas prieš paskelbdami žurnaluose

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Kai darbuotojas praneša, kad pagaminta prekė baigta, sistema užregistruoja ją kaip galima toliau fiziškai apdoroti (pvz., siuntą ar put šitą). Šio proceso metu taip pat registruojamas vienas ar daugiau žurnalų (pvz., pranešimas, kad užbaigtas žurnalas, išrinkimo dokumento žurnalas ir maršruto kortelės žurnalas). Jei norite, kad prekės būtų faktiškai galimos prieš apdorodami visus registravimus, galite nustatyti sistemą, kad ji atidėtų žurnalo registravimus. Atidėti registravimus tada valdo paketinė užduotis, kuri apdoros registravimus kaip leidžia sistemos ištekliai.

Šioje iliustracijoje parodyta, kaip iškviečiami žurnalų registravimo procesai ir atidėto registravimo, ir jo neįregistravimo metu.

![Skelbimo baigtu procesas su atidėto žurnalo registravimu ir be jo.](media/deferred-posting-flowchart.png "Skelbimo baigtu procesas su atidėto žurnalo registravimu ir be jo")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Įjungti atidėto žurnalo registravimą jūsų sistemai

Kad būtų galima naudoti atidėtą žurnalo registravimą, jį reikia įjungti jūsų sistemoje. Administratoriai gali naudotis funkcijų [valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritimi, norėdami patikrinti funkcijos būseną ir ją įjungti. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Gamybos kontrolė*
- **Priemonės pavadinimas:** *(peržiūra), kad užbaigtos prekės būtų faktiškai galimos prieš registruojant į žurnalus*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Nustatyti žurnalo registravimo parinktis, kad būtų galima skelbti, kad baigta

Darbuotojai gali pranešti prekes kaip baigtas, naudodami bet kurį iš šių klientų:

- Žiniatinklio klientas
- Sandėlio valdymo mobilioji programa
- Gamybos laiko vykdymo sąsaja

Žiniatinklio klientas naudoja tą pačią registravimo būdo konfigūraciją kaip ir sandėlio valdymo mobilioji programa. Tačiau registravimo metodas, kurį naudoja gamybos laiko vykdymo sąsaja, turi būti sukonfigūruotas atskirai.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Nustatyti žiniatinklio kliento ir sandėlio valdymo mobiliosios programos žurnalo registravimo parinktis

Mobiliųjų įrenginių programoje darbuotojai praneša, kad prekės baigtos, atidarydami mobiliojo įrenginio **meniu** *·* *elementą, kur darbo kūrimo proceso vertė yra Pranešti, kad užbaigta arba Pranešti, kad baigta, ir atidėkite.* Žiniatinklio kliente darbuotojai prekes praneša kaip apie baigtas **iš visų gamybos užsakymų** sąrašo puslapio arba **gamybos užsakymo (informacijos)** puslapio. Galite konfigūruoti visos įmonės numatytąjį metodą ir taip pat galite nustatyti sandėliui bingus perrašymus, jei to reikia.

Naudokite nurodytą procedūrą, norėdami konfigūruoti visos įmonės numatytąjį registravimo metodą, skirtą tinklo kliento arba sandėlio valdymo mobiliosios programos prekėms skelbti baigtomis.

1. Eikite į **Gamybos kontrolės \> nustatymo \> gamybos kontrolės parametrus**.
1. Skirtuke **Žurnalai**, skyriuje **Skelbti baigtu** žurnalą nustatykite vieną **iš** šių lauko Registravimo metodas verčių:

    - *Nedelsiant* – kai prekė paskelbta baigta, sistema visiškai apdoroja visus susijusius žurnalų registravimus prieš ji pažymint baigtą prekę kaip faktiškai prieinamą.
    - *Atidėta* – kai prekė paskelbta baigta, sistema pažymi baigtą prekę kaip faktiškai prieinamą ir įtraukia žurnalo registravimus į pranešimų eilę. Sistema nelauks, kol registravimo įrašai bus visiškai apdoroti, kad ji pažymi baigtą prekę kaip faktiškai prieinamą.

Naudokite šią procedūrą, norėdami konfigūruoti sandėliui bingus **numatytojo registravimo metodo, konfigūruojamos gamybos kontrolės parametrų puslapyje, nepaisymus**.

1. Eikite **į Sandėlio \> valdymo \> nustatymas Atsargų paskirstymo \> sandėliai**.
1. Pasirinkite sandėlį, kurį norite nustatyti.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Sandėlio **"** FastTab" gamybos užsakymų **skyriuje** nustatykite vieną **iš** šių lauko Registravimo metodas verčių:

    - *Paveldėti* – pasirinktas sandėlis perima parametrą iš **puslapio Gamybos valdymo** parametrai.
    - *Nedelsiant* – kai prekė paskelbta baigta, sistema visiškai apdoroja visus susijusius žurnalų registravimus prieš ji pažymint baigtą prekę kaip faktiškai prieinamą.
    - *Atidėta* – kai prekė paskelbta baigta, sistema pažymi baigtą prekę kaip faktiškai prieinamą ir įtraukia žurnalo registravimus į pranešimų eilę. Sistema nelauks, kol registravimo įrašai bus visiškai apdoroti, kad ji pažymi baigtą prekę kaip faktiškai prieinamą.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Nustatyti gamybos laiko vykdymo sąsajos žurnalo registravimo parinktis

Naudokite šią procedūrą, norėdami konfigūruoti registravimo metodą, kuris naudojamas, kai gamybos laiko vykdymo sąsajoje prekės yra pranešamos baigtomis.

1. Eikite į **Gamybos kontrolės \> nustatymas \> Gamybos vykdymas \> Gamybos užsakymo numatytieji nustatymai**.
1. Skirtuke **Skelbti baigtu** žurnalo **·** **skyriuje** Skelbti baigtu nustatykite vieną iš šių lauko Registravimo metodas verčių:

    - *Nedelsiant* – kai prekė paskelbta baigta, sistema visiškai apdoroja visus susijusius žurnalų registravimus prieš ji pažymint baigtą prekę kaip faktiškai prieinamą.
    - *Atidėta* – kai prekė paskelbta baigta, sistema pažymi baigtą prekę kaip faktiškai prieinamą ir įtraukia žurnalo registravimus į pranešimų eilę. Sistema nelauks, kol registravimo įrašai bus visiškai apdoroti, kad ji pažymi baigtą prekę kaip faktiškai prieinamą.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Planuoti pranešimų procesoriaus paketinę užduotį atidėtų registravimų apdorojimui

Pranešimų procesoriaus paketinė užduotis yra atsakinga už žurnalo užregistravimo apdorojimą po to, kai jie į eilę. Norėdami užtikrinti, kad jūsų žurnalo registravimo įrašai apdoroti, turite sukonfigūruoti šią užduotį, kad ji būtų vykdoma įprastu intervalu. Norėdami nustatyti reikiamą paketinę užduotį, naudokite nurodytą procedūrą.

1. Eikite į Sistemos **administravimo pranešimų \> procesoriaus pranešimų \> procesorių**.
1. Parametrų **"** FastTab" nustatykite lauką **Pranešimų eilė** kaip *Gamyba*.
1. Dalyje Vykdyti **fone "FastTab"** nustatykite paketinio vykdymo **parinktį** *Taip*. Tada nustatykite pasikartojančią grafiką ir sukonfigūruokite kitus parametrus, jei reikia. Šie parametrai veikia kaip ir kitų tipų foninės užduotys [programoje](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) "Microsoft"Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Sekti atidėtų registravimus eigą

Atidėti žurnalų registravimus eilėje yra pranešimų *procesoriaus* pranešimai, kurie laukia, kol jie bus apdoroti pranešimų *procesoriaus*. Pranešimų procesorius turėtų būti nustatytas vykdyti kaip suplanuota paketinė užduotis. Norėdami peržiūrėti atidėtus registravimo pranešimus, kuriuos buvo ar apdoros pranešimų procesorius, **eikite į Gamybos kontrolės \> gamybos užsakymų atidėto \> gamybos užsakymo registravimą**.

### <a name="message-grid-columns-and-filters"></a>Pranešimų tinklelio stulpeliai ir filtrai

Galite naudoti laukus atidėtų gamybos **užsakymų registravimo** puslapio viršuje, norėdami padėti rasti bet kokius konkrečius pranešimus, kurių ieškote.

Galimi toliau pateikti filtrai.

- **Pranešimo tipas** – nurodykite tinklelyje rodoų pranešimų tipą.
- **Pranešimo būsena** – nurodykite tinklelyje rodomą pranešimų būseną. Yra tokios valstijos:

    - *Eilėje* – pranešimą gali apdoroti pranešimų procesorius.
    - *Apdorotos* – pranešimas buvo sėkmingai apdorotas pranešimo tvarkytojo.
    - *Atšaukta* – pranešimo nepavyko apdoroti galutinio bandymo metu, ir tada jį atšaukė vartotojas.
    - *Nepavyko* – pranešimo nepavyko apdoroti per paskutinį bandymą. Sistema tris kartus kartos nesėkmingus pranešimus. Tada jis atiduos ir išeis iš pranešimo būsenos *Nepavyko*. Atsidėmėkite, kad negalite rankiniu būdu atšaukti ar redaguoti pranešimo, kol po paskutinių iš šių trijų bandymų.

- **Pranešimo turinys** – Šis filtras atlieką visą teksto paiešką pagal pranešimo turinį. (Pranešimo turinys tinklelyje nerodomas.) Filtras kaip vietos simbolius (pvz., brūkšnelius) traktuoja kaip vietos simbolius ir visus tarpo simbolius traktuoja kaip Bulio logikos OR operatorius. Pavyzdžiui, jei ieškote konkrečios vertės, `journalid` lygios USMF-123456 *, sistema suras visus pranešimus*, kuriuose yra "USMF" arba "123456". Šiuo atveju tikėtina, kad rezultatų sąrašas bus ilgas. Todėl geriau įvesti ką tik *123456*, nes gausite daugiau konkrečių rezultatų.

Taip pat galite rūšiuoti ir filtruoti sąrašą pasirinkdami bet kurią stulpelio antraštę ir išplečiamajame dialogo lange įvesdami kriterijus.

### <a name="view-the-message-log-message-content-and-details"></a>Peržiūrėti pranešimų žurnalą, pranešimų turinį ir informaciją

Išsamią informaciją apie **pranešimą** **galite** rasti pasirinkę jį tinklelyje ir pranešimų tinklelyje pasirinkę žurnalo arba neapdoroto turinio skirtuką, kuriame rodomas kiekvienas apdorojimo įvykis.

Žurnalo skirtuke **esančioje** įrankių juostoje yra šie mygtukai:

- **Žurnalas** – pasirinkite šį mygtuką, jei norite matyti apdorojimo rezultatus. Šis mygtukas ypač naudingas, kai pranešimų **apdorojimo** rezultato *vertė yra Nepavyko*, ir jūs norite sužinoti trikties apdorojimo priežastis.
- **Grupavimas** – kelios pranešimų apdorojimo operacijos gali būti paleidžiaos kaip to paties paketinio vykdymo dalis. Pasirinkite šį mygtuką, jei norite peržiūrėti visus duomenis. Pavyzdžiui, galite pamatyti, ar yra priklausomybių, kurioms kai kuriems pranešimui reikia konkretaus apdorojimo užsakymo.

### <a name="manually-process-or-cancel-a-message"></a>Pranešimo apdorojimas rankiniu būdu arba atšaukimas

Jei reikia, atsižvelgiant į esamą jo būseną, pranešimą galite apdoroti arba atšaukti neautomatiniu būdu. Pasirinkite pranešimą tinklelyje, tada veiksmų srityje **pasirinkite** Procesas **arba** Atšaukti.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Nustatyti verslo įvykius, kurie turėtų pateikti įspėjimus dėl nesėkmingų rezultatų

Galite nustatyti verslo įvykius [, kurie](../../fin-ops-core/dev-itpro/business-events/home-page.md) jus įspėtų apie rezultatų nesėkmingus. Eikite į **sistemos administravimo \> nustatymo verslo \> įvykių \> verslo įvykių katalogą** ir suaktyvinkite verslo įvykį, kuris vadinamas Pranešimų *procesoriaus pranešimu*.

Kaip aktyvinimo proceso dalį jūs paraginamas nurodyti, ar įvykis yra konkretus vienam juridiniam subjektui, ar taikomas visiems juridiniams subjektams. Taip pat jus paragins pateikti galinio punkto **pavadinimo** reikšmę. Pirmiausia reikia nurodyti šią vertę.

> [!NOTE]
> Jei laukas **Kai įvyksta verslo įvykis,** *Microsoft Power Automate* nustatomas į (*pavyzdžiui, ne HTTPS*), **galinio** punkto pavadinimo vertė automatiškai sukuriama tiekimo grandinės valdymo dalyje, *Microsoft Power Automate* remiantis nustatymu.
