---
title: Supažindinimo vadovų ir šablonų redagavimas „Dynamics 365 Talent - Onboard”
description: Šioje temoje paaiškinama, kaip įtraukti veiklas ir kitą informaciją į supažindinimo vadovus ir šablonus „Microsoft Dynamics 365 Talent - Onboard”.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462012"
---
# <a name="edit-onboarding-guides-and-templates"></a>Supažindinimo vadovų ir šablonų redagavimas

[!include [banner](includes/banner.md)]

Sukūrę supažindinimo vadovą arba šabloną „Microsoft Dynamics 365 Talent: Onboard“, turite pridėti įžangą, veiklas, kontaktus ir išteklius. Naudodami „Onboard” į supažindinimo vadovus galite įtraukti toliau nurodytą raiškųjį turinį.

- YouTube vaizdo įrašai
- „Microsoft Sway” pateiktys
- „Microsoft PowerApps” programėlės
- Microsoft Stream vaizdo įrašai
- „Microsoft Forms” formos
- „Iframe”, kuriuose yra žiniatinklio turinio

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Iš šablono importuotų įžangų ar veiklų redagavimas

Jei kuriate supažindinimo vadovą iš šablono arba importuojate veiklas iš vieno šablono į kitą, importuotose veiklose pastebėsite mygtuką **Užrakinti**. Šios veiklos vadinamos *valdomosiomis veiklomis*.

[![Valdomosios veiklos](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Pasirinkę valdomąją veiklą, veiklos viršuje galite matyti šaltinio šabloną.

[![Valdomosios veiklos šaltinis](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Jei redaguojate veiklą šablone, „Onboard” atliks keitimus visuose šablonuose ir neišsiųstuose vadovuose, kurie sukurti pagal tą šabloną. Jei pasirinksite neišsiųstą vadovą, kuris sukurtas remiantis jūsų redaguotu šablonu, o tada vadove pasirinksite skirtuką **Veiklos**, pamatysite pranešimą, kad jūsų vadovas buvo pakeistas. Norėdami atmesti pranešimą, pasirinkite **Gerai.** 

[![Pranešimas apie pakeitimą](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Šalia atnaujintų veiklų pamatysite juodą tašką.

[![Pakeista veika](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Negalite redaguoti valdomosios veiklos ne pagrindiniame šablone, nebent norite į dešiniąją veiklos dalį įtraukti priėmėją, terminą ar kitą informaciją.

Jei norite redaguoti valdomą veiklą arba jei nenorite, kad veikla gautų naujinimus iš šablono, iš kurio ji atsirado, pasirinkite tos veiklos mygtuką **Užrakinti**. Mygtukas **Užrakinti** išnyks. Veikla nebebus valdoma pradiniame šablone ir ji daugiau negaus to šablono naujinimų. Jūsų atlikti veiklos naujinimai neturi įtakos pradiniam šablonui.

Jei naikinate veiklą iš vadovo ir paskelbiate to vadovo šablono keitimus, veikla vadove liks panaikinta.

> [!NOTE]
> Kontaktai ir ištekliai nėra valdomi naudojant šablonus. Be to, skyriai nėra valdomi, todėl jei pridėsite arba redaguosite skyrių šablone, keitimai nebus skelbiami jokiuose vadovuose ar šablonuose, kurie naudoja tą šabloną.
> 
> Jei į šabloną įtraukiate naujų veiklų, jos yra paskelbiamos vadovuose ir šablonuose, pagrįstuose tuo šablonu, ir rodomos viršuje.

## <a name="import-activities-from-another-template"></a>Veiklų iš kito šablono importavimas

Veiklas į vadovą arba šabloną galite importuoti iš vieno ar daugiau šablonų.

1. Pasirinkite vadovą ar šabloną, kurį norite redaguoti.

2. Pažymėkite skirtuką **Veiklos**.

3. Dešinėje esančiame skyriuje pasirinkite skirtuką **Importavimas**.

   [![Veiklų importavimas](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Jei norite peržiūrėti užduotis naujame naršyklės skirtuke, bet kuriame šablone pasirinkite mygtuką **Atidaryti naujame skirtuke**.

   [![Veiklų importavimas](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Nuvilkite norimą šabloną į vietą, esančią vadovo šablone, kur norite, kad veiklos būtų rodomos. Toliau redaguokite vadovą ar šabloną.

Importuotose veiklose bus mygtukas **Užrakinti**, kuris nurodo, kad tas veiklas valdo šablonas, iš kurio importavote. Atlikus keitimus importuotame šablone, veiklos bus atnaujintos šablone, į kurį importavote. Tačiau keitimai nebus automatiškai paskelbti vadovuose, sukurtuose iš šablono, į kurį buvo importuota.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Keitimų iš šablono į kitus šablonus arba vadovus skelbimas

Jei redaguojate šabloną, kuriame yra veiklų, naudojamų kituose šablonuose arba vadovuose, turite paskelbti keitimus, jei norite, kad jie ten būtų rodomi.

Jei nesate tikri, ar šablono veiklos yra naudojamos kituose šablonuose ar vadovuose, pasirinkite skirtuką **Naudojama**, kad peržiūrėtumėte, kur tos veiklos yra rodomos.

   [![Vadovų ir šablonų, kuriuose veiklos naudojamos, rodinys](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Toliau nurodyti veiksmai, kuriuos turite atlikti norėdami paskelbti keitimus.

1. Išsaugokite keitimus pasirinkdami mygtuką **Įrašyti**. Jei to nepadarysite, būsite paraginti įrašyti keitimus kitame veiksme.

2. Pasirinkite **Skelbti šiuos pakeitimus**.

   
## <a name="add-or-edit-an-introduction"></a>Įžangos įtraukimas arba redagavimas

1. Skirtuke **Įžanga** įveskite vadovo pavadinimą ir pradinį pranešimą. Norėdami naudoti pavyzdinį tekstą, pasirinkite **Naudoti šį pranešimą**.

    [![Skirtukas „Įžanga” „Onboard” šablone](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Jei norite redaguoti tekstą pagal savo poreikius arba pridėti vaizdų ar saitų, naudokite formatavimo mygtukus.
3. Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.

## <a name="add-or-edit-activities"></a>Veiklų įtraukimas ir redagavimas

1. Skirtuke **Veiklos** nuvilkite elementus iš dešinės į redagavimo sritį.
2. Norėdami sutvarkyti savo vadovą, suskirstydami jį į skyrius, nuvilkite elementą **Naujas skyrius** į redagavimo sritį ir įveskite skyriaus pavadinimą bei pasirenkamą aprašą.

    ![[Naujo skyriaus įtraukimas į supažindinimo vadovą arba šabloną](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Jei norite pridėti veiklų naujam darbuotojui atlikti, nuvilkite elementą **Nauja veikla** į redagavimo sritį ir įveskite veiklos pavadinimą bei aprašą.

    ![[Naujos veiklos įtraukimas į supažindinimo vadovą arba šabloną](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Norėdami įtraukti raiškųjį turinį į supažindinimo vadovą, atlikite toliau nurodytus veiksmus.

    - Norėdami įtraukti „YouTube” vaizdo įrašą, nuvilkite elementą **YouTube** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei „YouTube” vaizdo įrašo URL.
    - Norėdami pridėti „Sway” pateiktį arba informacinį biuletenį, nuvilkite elementą **Sway** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei įveskite „Sway” pateikties arba informacinio biuletenio įdėtąjį URL.
    - Norėdami įtraukti „Microsoft Power Apps“ programėlę, nuvilkite elementą „**Power Apps**“ į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, tada pasirinkite „Power Apps“ programėlę arba įveskite „Power Apps“ programėlės ID.
    - Norėdami įtraukti „Microsoft Stream” vaizdo įrašą, nuvilkite elementą **Microsoft Stream** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei „Microsoft Stream” vaizdo įrašo URL.
    - Norėdami įtraukti „Microsoft Forms“ formą, nuvilkite elementą **Microsoft Forms** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, įveskite „Microsoft Forms“ formos URL ir nurodykite ekrano srities dydį.
    - Norėdami įtraukti „Iframe”, kuriame yra žiniatinklio turinio, nuvilkite elementą **Web Content (iframe)** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, įveskite žiniatinklio turinio URL ir nurodykite ekrano srities dydį.

    ![[Naujo raiškiojo turinio įtraukimas į supažindinimo vadovą arba šabloną](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Pasirinktinai: kiekvienos veiklos dešinėje srityje priskirkite veiklą konkrečiam asmeniui arba vaidmeniui, įtraukite terminą ir kontaktinį asmenį bei priskirkite kategorijos spalvą. Kai priskiriate veiklą asmeniui ar vaidmeniui, kiekvienam asmeniui sukuriama užduotis. Ši užduotis rodoma „Onboard” meniu **Užduotys**.

    [![Veiklos priskyrimas supažindinimo vadove ar šablone](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.

Norėdami panaikinti veiklą arba skyrių, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį viršutiniame dešiniajame veiklos arba skyriaus kampe.

Norėdami pertvarkyti veiklas ir skyrius, nuvilkite juos į naują vietą.

## <a name="add-or-edit-contacts"></a>Kontaktų įtraukimas ar redagavimas

Galite įtraukti kontaktinius asmenis, kurie gali padėti jūsų naujam darbuotojui nuo pirmosios dienos. Šie kontaktai gali būti darbdaviai, komandos nariai, priskirti pagalbos asmenys, mentoriai, administratoriai ir IT pagalbos darbuotojai.

1. Skirtuke **Kontaktai** pasirinkite **Naujas kontaktas**.
2. Dialogo lange **Įtraukti komandos narį** įveskite kontaktinio asmens vardą arba el. pašto adresą, trumpą aprašą, paaiškinantį, kaip kontaktinis asmuo gali padėti naujam darbuotojui, ir pasirinkite **Įtraukti**. 

    ![[Naujų kontaktų įtraukimas į supažindinimo vadovą arba šabloną](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Kitu atveju, galite pasirinkti vieną ar daugiau kontaktų po elementu **Pasiūlymai**.

3. Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.

Norėdami panaikinti kontaktą, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį kontakto dešinėje.

Norėdami redaguoti kontaktą, pasirinkite mygtuką **Redaguoti** (pieštuko simbolis), esantį kontakto dešinėje.

## <a name="add-or-edit-resources"></a>Išteklių įtraukimas ar redagavimas

Į supažindinimo vadovo skyrių **Ištekliai** galite įtraukti naudingų failų, schemų ir nuorodų.

1. Skirtuke **Ištekliai** pasirinkite **Nauji ištekliai**.
2. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami įtraukti failą, pasirinkite skirtuką **Failas** ir nuvilkite failą į paskirtą sritį. (Taip pat galite spustelėti bet kurioje tos srities vietoje, kad rastumėte failą kompiuteryje, arba pasirinkti **Naršyti „OneDrive”**.) Įveskite failo pavadinimą ir pasirinkite **Įtraukti**.
    - Norėdami įtraukti saitą, pasirinkite skirtuką **Saitas**, įveskite saito pavadinimą ir adresą, tada pasirinkite **Įtraukti**.
    - Norėdami įtraukti schemą, pasirinkite skirtuką **Schema**, įveskite schemos pavadinimą ir adresą, tada pasirinkite **Įtraukti**. „Onboard” pateiks adreso, kurį nurodėte, schemą.

    ![[Naujų išteklių įtraukimas į supažindinimo vadovą arba šabloną](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.

Norėdami panaikinti išteklius, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį išteklių dešinėje.

Norėdami redaguoti išteklius, pasirinkite mygtuką **Redaguoti** (pieštuko simbolis), esantį išteklių dešinėje.

## <a name="next-steps"></a>Kiti veiksmai

- [Turinio bendrinimas su kitais bendraautoriais](./onboard-share-template.md)
- [Užduočių ir darbuotojų supažindinimo būsenos peržiūra](./onboard-view-status.md)
- [Samdos komandų kūrimas „Onboard”](./onboard-create-team.md)

### <a name="see-also"></a>Taip pat žiūrėkite

- [Išbandykite arba įsigykite „Onboard” programėlę](https://dynamics.microsoft.com/talent/onboard/)
- [Kas nauja arba pasikeitė „Dynamics 365 Talent“](./whats-new.md)
- [Leidimo planai](https://docs.microsoft.com/business-applications-release-notes/index)
- [Palaikymo dėl „Microsoft Dynamics 365 Talent“ gavimas](./talent-support.md)
