---
title: Vaizdinis ir bendrasis vykdymas
description: Šiame straipsnyje aprašoma, kaip stebėti jūsų poreikio valdomas medžiagų poreikių planavimo (DDMRP) išširpimo taškus, buferio zonas, suplanuotus užsakymus ir retrospektyvą.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740829"
---
# <a name="visual-and-collaborative-execution"></a>Vaizdinis ir bendrasis vykdymas

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Šiame straipsnyje aprašoma, kaip stebėti jūsų poreikio valdomas medžiagų poreikių planavimo (DDMRP) išširpimo taškus, buferio zonas, suplanuotus užsakymus ir retrospektyvą.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Vaizdiškai sekti pasirinktos prekės buferius ir kiekius

Microsoft galite Dynamics 365 Supply Chain Management vizualiai sekti, kaip bet kurio pasirinkto išleisto produkto buferiai, turimi kiekiai ir grynojo srauto lygiai gali keistis. Norėdami atidaryti ir peržiūrėti diagramas, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite išleistą prekę, kuri nustatyta kaip iššiavimo taškas. (Daugiau informacijos žr. [Atsargų padėties valdymas](ddmrp-inventory-positioning.md).)
1. Veiksmų srities skirtuke Planas **pasirinkite** Prekės **padengimas**.
1. Prekių padengimo **puslapyje** pasirinkite prekės padengimo įrašą, kuris sukuria iššipimo tašką. (Šiame įraše bus rodomas padengimo grupės, nustatytos sukurti atsišiejimo taškus, pavadinimas.)
1. **Pasirinkite skirtuką Turimos**. Šiame skirtuke yra diagrama, kurioje parodyta, kaip per tam tikrą laiką pasikeitė turimi kiekiai, ir turimo kiekio vertė, kuri buvo įrašyta tam tikrą laikotarpį kaskart, kai vykdomas bendrasis planavimas. Skirtuke taip pat yra lentelė, kurioje parodoma, į kurias iš šių kategorijų įeina kiekvienas įrašytas turimo kiekis:

    - **Kritinis žemas** – mažiau nei pusė laikotarpio minimumo.
    - **Mažas** – nuo pusės minimumo iki mažiausio.
    - **Vidutinis turimos atsargų** dydis – tarp minimumo ir mažiausios bei žalios zonos.
    - **Didesnis nei vidurkis** – didesnis nei vidurkis.

    ![Retrospektyvūs turimos atsargų lygiai skirtuke Turimos.](media/ddmrp-on-hand-graph.png "Retrospektyvūs turimos atsargų lygiai skirtuke")

    > [!NOTE]
    > Turimose atsargų skirtuke **naudojamos spalvos** nurodo skirtingus diapazonus nei panašios spalvos, naudojamos skirtuko lape **Buferio** vertės.

1. Norėdami peržiūrėti, kaip jūsų buferio vertės laikui bėgant pasikeitė ir kaip jos lyginamos su turimos bei grynojo srauto lygiais, pasirinkite skirtuką **Buferio** vertės.

    ![Praeities turimos vertės ir grynojo srauto lygiai skirtuke Buferio vertės.](media/ddmrp-buffer-values-graph.png "Praeities turimos vertės ir grynojo srauto lygiai skirtuke Buferio vertės")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Visų atsiejimo taškų būsenos ir suplanuotų užsakymų sekimas

Poreikio **valdoma MRP** darbo sritis pateikia keletą įrankių bei pagrindinius efektyvumo indikatorius (KPI) ir jūsų atsiejimo taškų prekių ir susijusių suplanuotų užsakymų būsenų apžvalgas. Norėdami ją atidaryti, eikite į Bendrojo **planavimo darbo \> sritis \> Poreikio valdomas MRP**.

![Poreikio valdoma MRP darbo sritis.](media/ddmrp-workspace.png "Poreikio valdoma MRP darbo sritis")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Gauti atsiejimo taškų ir suplanuotų užsakymų apžvalgas

Tiekimo grandinės **valdymas be poreikio pagrįstos MRP** darbo srities pateikia keletą puslapių, kuriuose galite peržiūrėti informaciją apie savo DDMRP nustatymą, atsiejimo taškus ir suplanuotus užsakymus. Kai kuriuose šių puslapių veiksmų srityje taip pat pateikti patogūs mygtukai, leidžiaysi tvarkyti buferius, paleisti bendrąjį planavimą ir atidaryti kitus susijusius rodinius.

- Norėdami peržiūrėti atsiejimo taškų būseną pagal grynojo srauto lygį, **\>\> eikite į bendrojo planavimo DDMRP \> išširpimo taškų būseną pagal grynąjį srautą**.
- Norėdami peržiūrėti atsiejimo taškų būseną pagal turimų atsargų lygį, **\>\> eikite į bendrojo planavimo bendrojo planavimo DDMRP \> atsiejimo taškų būseną pagal turimų atsargų kiekį.**
- Norėdami peržiūrėti suplanuotus prekių iššišiavimo taškų užsakymus, **\>\> eikite į bendrojo planavimo bendrojo planavimo DDMRP \> suplanuotus užsakymus, kuriuos reikia atlikti atsiejimo taškams.**
- Norėdami peržiūrėti suplanuotus gamybos laikus, eikite **į bendrojo planavimo \> bendrojo planavimo \> DDMRP \> susietą gamybos laiką**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Valyti iššiuosmos taško buferio vertes

Laikui bėgant jūsų sistema sukurs daug retrospektyvinių duomenų, susijusių su vykdomais buferio skaičiavimais. Dėl šių retrospektyvinių duomenų jūsų duomenų tūris gali padidėti, o tai galiausiai turės įtakos jūsų sistemos našumui. Dėl to rekomenduojame kartais išvalyti senas iššišiavimo taško buferio vertes.

> [!WARNING]
> Valymo užduotis pašalins retrospektyvos buferio vertės parametrus ir retrospektyvinę turimo / grynojo srauto informaciją. Jo negalima atšaukiama.

Norėdami išvalyti savo atsiejimo taško buferio vertes, atlikite šiuos veiksmus.

1. Eikite į **bendrojo planavimo \> bendrojo planavimo \> DDMRP išvalykite \> išširpimo taško buferio vertes**.
1. Dialogo lange **Valyti iššišiojimo taško buferio** vertes nustatykite šiuos laukus:

    - **Panaikinti senesnius įrašus nei (dienos)** – nurodytiestų išsaugoti įrašų amžių dienomis. Visi atsiejimo taškų buferio verčių įrašai, kurie yra senesni už šią reikšmę, bus panaikinti.
    - **Bendrasis planas** – pasirinkti bendrąjį planą, kuriame yra prekės, kurioms turi įtakos šis valymas. Valymas bus taikomas visoms plano prekėms, pritaikius **filtro** parametrus, kuriuos nurodote šiame dialogo lange.

1. Norėdami apriboti įrašų, kuriuos turėtų vykdyti paketinė užduotis, rinkinį, įrašuose, **kuriuose** reikia įtraukti "FastTab", pasirinkite Filtras, **·** **kad atidarytumėte dialogo** langą Užklausa. Šis dialogo langas veikia taip pat kaip ir kitiems tiekimo grandinės [valdymo fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Skirtuke **Vykdyti fone** FastTab nurodykite kaip, kada ir kaip dažnai valymas turi būti atliekamas. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai,** norėdami įtraukti naują užduotį į paketinių užduočių eilę vykdymui.
