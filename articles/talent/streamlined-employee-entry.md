---
title: Supaprastintas darbuotojo įrašo sukūrimas ir naršymas
description: Buvo patobulintas darbuotojų duomenų įvedimas „Dynamics 365 Talent”, kad visiems buvusiems, aktyviems ar būsimiems darbuotojams būtų užtikrintas kuo greitesnis įvedimas. Supaprastintas/konsoliduotas naršymo modelis buvo atnaujintas, siekiant greitai rasti susijusią informaciją ir peržiūrėti bei atlikti būtinus naujinimus.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009427"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Supaprastintas darbuotojo įrašo sukūrimas ir naršymas

[!include [banner](includes/banner.md)]

„Dynamics 365 Talent” leidžia efektyviai įvesti darbuotojų ir įdarbinimo duomenis. Galite greitai atnaujinti buvusių, aktyvių ir būsimų darbuotojų bei rangovų darbo retrospektyvos informaciją.

Taip pat galite įgalinti supaprastintą naršymo patirtį, kad greitai rastumėte susijusią informaciją ir įvykdytumėte reikiamus pakeitimus. Ši funkcija dabar yra smėlio dėžės aplinkose. Norėdami įjungti šią funkciją, pereikite prie **Sistemos administravimas > Saitai > Sąranka > Sistemos parametrai > Peržiūros funkcijos**. Pasirinkite **Patobulintoji darbuotojo forma ir naršymas**. Tai įgalins šiuos pakeitimus visiems vartotojams. Šią parinktį galite bet kuriuo metu išjungti.

## <a name="view-options"></a>Rodyti parinktis

Norėdami pasirinkti bet kokį darbuotojų ir rangovų derinį iš vieno sąrašo, galite naudoti **Peržiūrėti parinktis** darbininko formoje. Šios parinktys leidžia peržiūrėti juridinių subjektų arba juridinio subjekto, prie kurio šiuo metu esate prisijungę, darbuotojus. Taip pat galite peržiūrėti aktyvius, laukiančius ir atleistus darbininkus ir apriboti rezultatus pagal darbininko tipą (darbuotojas ar rangovas). Jei įgalinote išplėstinę saugą, matysite tik tuos juridinių subjektų darbuotojus ir rangovus, prie kurių turite priėjimą.

Stulpeliai sąrašo rodinyje keičiasi pagal jūsų pasirinkimus. Pavyzdžiui, kai peržiūrite atleistus darbuotojus, atleidimo data ir priežasties kodai rodomi kaip papildomi stulpeliai sąraše. 

[![Rodyti parinktis](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Naršymas ir reklaminė juosta

Reklaminėje juostoje rodoma pagrindinė kiekvieno darbuotojo informacija. Aktyvių darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.

- **Pareigos**
- **Skyrius**
- **Pareigų tipas**
- **Darbininko tipas**
- **Vadovas**
- **Juridinis subjektas**

Atleistų darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.

- **Atleidimo data**
- **Priežastis**

Laukiančių darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.

- **Pareigos**
- **Skyrius**
- **Pareigų tipas**
- **Vadovas**
- **Pradžios data**
- **Juridinis subjektas**

Darbininko puslapio veiksmų sritis buvo perorganizuota, kad apimtų mažiau parinkčių. Informacija dabar yra suskirstyta į toliau nurodytas kategorijas. 

- Darbas
- Asmuo
- Išeiti
- Kompensacija
- Išmokos
- Atitiktis

Be to, naujame pagrindinio darbuotojo puslapio skirtuke **Saitai** vartotojams suteikiama centrinė vieta, kur jie gali pasiekti visą su darbuotoju susijusią informaciją.

Dėl šių pakeitimų informacija gali būti rodoma kitoje vietoje nei esate įpratę. Pavyzdžiui, algalapių informacija, kuri anksčiau buvo rodoma darbuotojo formoje, dabar rodoma veiksmų srities dalyje **Kompensacija > Algalapis**, o skirtuke **Asmeninė informacija** dabar yra mygtukas **Daugiau informacijos**, skirtas laukams, kurie nėra dažnai pasiekiami, paslėpti.

[![Reklaminė juosta](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Darbo istorija

Skirtuke **Darbo retrospektyva** rodoma visų juridinių subjektų darbo retrospektyva ir ją gali pasiekti atleisti, aktyvūs ir laukiantys darbuotojai bei rangovai. Dabar galite peržiūrėti visą juridinių subjektų, prie kurių turite prieigą, darbo retrospektyvą vienu metu. Be to, galite redaguoti kiekvieno darbo retrospektyvos įrašo informaciją nekeisdami duomenų konteksto. Visą informaciją galite atnaujinti tiesiogiai puslapyje. 

[![Darbo istorija](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Pareigų retrospektyva

Pagrindiniame darbininko puslapyje esančiame skirtuke **Pareigos** pateikiamas visų organizacijoje einamų pareigų, įskaitant buvusius, esančius ir būsimus priskyrimus, rodinys. Taip pat galite eiti tiesiai į darbininko pareigų retrospektyvą veiksmų srityje.

[![Pareigybės](./media/Worker-position-history.png)](./media/Worker-position-history.png)

