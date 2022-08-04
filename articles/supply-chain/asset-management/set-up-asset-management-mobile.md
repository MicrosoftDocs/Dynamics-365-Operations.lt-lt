---
title: Turto valdymo mobiliosios darbo srities nustatymas
description: Šiame straipsnyje aprašoma, kaip nustatyti "Microsoft Dynamics 365 Supply Chain Management " ir finansų bei operacijų ("Dynamics 365") mobiliąją programą, kad būtų galima vykdyti turto valdymo mobiliąją darbo sritį, kurią darbuotojai gali naudoti turto valdymo užduotims atlikti.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ef4e6bf2ae59adb05c7d4aacc3f5675a5adcafc9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070060"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Turto valdymo mobiliosios darbo srities nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti "Microsoft Dynamics 365 Supply Chain Management" ir finansų bei operacijų ("Dynamics 365") **mobiliąją** programą, kad būtų galima vykdyti turto valdymo mobiliąją darbo sritį, kurią darbuotojai gali naudoti turto valdymo užduotims atlikti.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Techninės priežiūros darbuotojo vartotojų nustatymas „Supply Chain Management”

Kiekvienas vartotojas, kuriam reikalinga prieiga prie **Turto valdymas** mobiliosios darbo srities, turi atlikti šiuos veiksmus.

1. „Supply Chain Management” eikite į **Žmogiškieji ištekliai \> Darbuotojai** ir įsitikinkite, kad egzistuoja pageidautino sukonfigūruoti vartotojo darbuotojo įrašas. Sukurkite būtiną naujo darbuotojo įrašą.
1. Eikite į **Turto valdymas \> Sąranka \> Darbuotojai \> Darbuotojai** ir įsitikinkite, kad jūsų ankstesniu veiksmu nustatytas (ar sukurtas) darbuotojo įrašas yra susietas su techninės priežiūros darbuotojo įrašu. Sukurkite būtiną naują techninės priežiūros darbuotojo įrašą ir nustatykite **Darbuotojas** lauką darbuotojo įraše iš ankstesnio veiksmo.
1. Eikite į **Turto valdymas \> Sąranka \> Darbuotojai \> Techninės priežiūros darbuotojų grupės** ir įsitikinkite, kad jūsų ankstesniu veiksmu nustatytas (ar sukurtas) techninės priežiūros darbuotojo įrašas yra susietas su techninės priežiūros darbuotojo įrašu.
1. Eikite į **Sistemos administravimas \> Vartotojai**.
1. Tinklelyje pasirinkite atitinkamą vartotoją.
1. „FastTab” **Vartotojo informacija** skirtuke nustatykite **Asmuo** lauką darbuotojo paskyroje, kurią norite susieti su dabartinio vartotojo paskyra. Ši darbuotojo paskyra turi būti jūsų 1-ame veiksme nustatytas (ar sukurtas) darbuotojo įrašas ir susietas su 2-ojo veiksmo techninės priežiūros darbuotojo įrašu.

> [!NOTE]
> Vartotojo teisės ir saugos vaidmenys taikomi **Turto valdymo** mobiliosios darbo srities funkcijoms, o taip pat ir „Supply Chain Management” vartotojo sąsajos funkcijoms. Todėl kiekvienas jūsų nustatytas vartotojas, norintis pasiekti **Turto valdymas** mobiliąją darbo sritį, privalo turėti saugos vaidmenis, būtinas atlikti panašias operacijas tiesiogiai „Supply Chain Management”.

## <a name="publish-the-asset-management-mobile-workspace"></a>Turto valdymo mobiliosios darbo srities paskelbimas

Norėdami, kad turto valdymo priemonės būtų galimos finansų ir operacijų ("Dynamics 365") mobiliųjų įrenginių programoje, turite paskelbti turto **valdymo mobiliąją** darbo sritį.

1. „Supply Chain Management” pasirinkite **Parametrai** mygtuką (krumpliaračio piktograma viršutiniame dešiniajame kampe) ir meniu pasirinkite **Mobilioji programėlė**.
1. Dialogo lange **Tvarkyti mobiliąją programėlę** suraskite plytelę **Turto valdymas**. Joje pateiktas tekstas „Metaduomenyse – nepublikuota”, darbo sritis dar nebuvo publikuota. Jei joje yra tekstas „Metaduomenyse – publikuota”, darbo sritis jau publikuota, o likusią procedūrą galite praleisti.

    ![Mobiliosios programėlės tvarkymo dialogo langas.](media/mobile-workspaces.png "Mobiliosios programėlės tvarkymo dialogo langas")

1. Pasirinkite **Turto valdymas** plytelę, tada įrankių pasirinkite **Publikuoti**. Po kelių sekundžių turėtumėte gauti pranešimą, kad darbo sritis sėkmingai publikuota. Be to, plytelės tekstas turi pasikeisti į „Metaduomenyse – publikuota”.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Įdiegti ir nustatyti finansų ir operacijų ("Dynamics 365") mobiliąją programą

1. Pereikite į vieną iš toliau nurodytų parduotuvių ir įdiekite " **Microsoft" finansų ir operacijų ("Dynamics 365")** programą mobiliajame įrenginyje:

    - [„Google Android” įrenginiams](https://go.microsoft.com/fwlink/?linkid=850662)
    - [„iOS” įrenginiams](https://go.microsoft.com/fwlink/?linkid=850663)

1. Atidarykite finansų ir operacijų ("Dynamics 365") programą. Turėtų pasirodyti prisijungimo puslapis. **Prisijungti** lauke įveskite „Supply Chain Management” URL arba įveskite neseniai naudotą URL **Neseniai naudotos aplinkos**  sąraše ir bakstelėkite **Prisijungti**.

    ![Prisijungimo puslapis.](media/mobile-app-sign-in.png "Prisijungimo puslapis")

1. Jei būsite paraginti patvirtinti ryšį, pažymėkite žymės langelį **Supratau**, tada spustelėkite **Prisijungti**.
1. Puslapyje **Pasirinkti paskyrą** naudokite „Microsoft” paskyrą, kad prisijungtumėte prie mobiliosios programėlės.

    Pasirodo puslapis **Darbo sritys**. Joje pateikiama kiekviena mobilioji darbo sritis, kurią publikavo „Supply Chain Management” programa.

    ![Darbo sričių sąrašas.](media/mobile-app-workspaces.png "Darbo sričių sąrašas")

1. Jei turite pakeisti juridinį asmenį (įmonę), bakstelėkite meniu mygtuką (trys horizontalios linijos) viršutiniame kairiajame kampe ir tada bakstelėkite **Keisti įmonę**.

    ![Juridinio asmens keitimas.](media/mobile-app-change-comp.png "Juridinio asmens keitimas")

1. **Darbo sritys** puslapyje pasirinkite darbo sritį, su kurią norite dirbti, kad ją atidarytumėte.

    ![Turto valdymo mobilioji darbo sritis.](media/mobile-app-asset-workspace.png "Turto valdymo mobilioji darbo sritis")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Darbas su Turto valdymo mobiliąja darbo sritimi

Daugiau informacijos apie tai, kaip dirbti su **Turto valdymas** mobiliąja darbo sritimi, žr. [žr. Turto valdymo mobiliosios darbo srities naudojimas](asset-management-mobile-workspace.md).

Norėdami gauti daugiau informacijos apie finansų ir operacijų ("Dynamics 365") mobiliųjų įrenginių programėlę, žr. pagrindinį [mobiliojo programos puslapį](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
