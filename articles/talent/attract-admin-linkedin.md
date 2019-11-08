---
title: Integravimo su „LinkedIn“ nustatymas „Microsoft Dynamics 365 Talent - Attract“
description: Šioje temoje paaiškinama, kaip konfigūruoti „LinkedIn” integravimą „Microsoft Dynamics 365 Talent - Attract”, kad būtų galima lengvai registruoti darbo skelbimus „LinkedIn“ iš „Attract“ ir kad darbdaviai galėtų sinchronizuoti savo įdarbinimo informaciją su kandidato „LinkedIn” profiliu.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5cdce69396d6972d810e65e15b27c79119a0a9e6
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552122"
---
# <a name="set-up-integration-with-linkedin-for-microsoft-dynamics-365-talent---attract"></a>Integravimo su „LinkedIn“ nustatymas „Microsoft Dynamics 365 Talent - Attract“

[!include[banner](../includes/banner.md)]

Padėkite savo darbdaviams ir samdos vadovams pritraukti talentingiausius, sukonfigūruodami „LinkedIn“ integravimą su „Microsoft Dynamics 365 Talent: Attract”. „Attract” leidžia jums registruoti darbo skelbimus tiesiai į didžiausią profesionalų internetinį tinklą „LinkedIn”.

Darbo skelbimai, kuriuos registruosite į „LinkedIn” naudodami „Attract”, yra „Apriboti skelbimai” ir jie jūsų kompanijai suteikiami be papildomų išlaidų. Šie skelbimai yra galimi tik naudojant „LinkedIn” programinės įrangos partnerius, pvz., „Attract”. Jie nerodomi jūsų įmonės „LinkedIn” puslapyje, skydelyje **Karjeros**, nes ten rodomi tik mokami skelbimai. Tačiau jie rodomi, kai potencialūs kandidatai peržiūri visus laisvus darbus. Apriboti skelbimai taip pat rodomi „LinkedIn” darbo paieškose.

„Attract” pateikia du būdus, kaip integruoti su „LinkedIn”, kad jums būtų lengviau ieškoti kandidatų šioje populiarioje karjeros svetainėje:

- Darbo skelbimų registravimas „LinkedIn“ iš „Attract“.
- Kandidatų perkėlimas iš „LinkedIn“ į „Attract“.

Konfigūruokite abi parinktis skirtuke **„LinkedIn“ integravimas**, esančiame administravimo centre. Norėdami atidaryti administravimo centrą, eikite į <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Norint naudoti „LinkedIn Recruiter“ integravimą su „Attract“, jums reikia [išsamios įdarbinimo informacijos priedo](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) ir „[LinkedIn Recruiter” licencijų](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Norėdami gauti daugiau informacijos, žr. [Kurią „Attract“ versiją naudoti?](./attract-comprehensive-hiring.md).

Jei kyla problemų registruojant darbo skelbimus „LinkedIn”, žr. [„LinkedIn” integravimo trikčių diagnostika](./attract-troubleshoot-linkedin.md).

Norėdami gauti informacijos apie kitus būdus, kaip užregistruoti darbo skelbimus „LinkedIn”, žr. [DUK apie „LinkedIn“](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Konfigūruoti darbo registravimą „LinkedIn“

Prieš registruodami darbo skelbimus iš „Attract” į „LinkedIn”, jums reikia turėti [„LinkedIn“ įmonės ID](https://aka.ms/findID). Jūsų „LinkedIn“ įmonės ID yra skaičių, kurie unikaliai identifikuoja jūsų įmonę sistemoje „LinkedIn“, eilutė. Norėdami gauti daugiau informacijos, žr. [„LinkedIn” įmonės ID su „LinkedIn” darbo skelbimų lenta susiejimas – dažnai užduodami klausimai](https://aka.ms/findID).

„Attract” siunčia jūsų darbo skelbimų informacijos santrauką į „LinkedIn” ir „LinkedIn” patikrina informacijos santrauką maždaug kartą per dieną. Gali užtrukti iki 48 valandų, kol darbo skelbimai bus užregistruoti svetainėje.

„LinkedIn“ užregistruoti darbai rodomi „LinkedIn“ svetainėje realiuoju laiku. Darbų registravimo „LinkedIn“ tikrinimo aplinkos nėra. Todėl įsitikinkite, kad netyčia neregistruotumėte jokių tikrinimo darbų. 

1. Meniu **Sąranka** (krumpliaračio simbolis) viršutiniame dešiniajame kampe pasirinkite **Administravimo centras**. Taip pat galite pereiti į <https://attract.talent.dynamics.com/adminsettings>.
2. Pasirinkite skirtuką **„LinkedIn‟ integravimas**.
3. Dalyje **Įmonės pavadinimas** įveskite savo įmonės pavadinimą ir dalyje **Įmonės ID** įveskite savo „LinkedIn” įmonės ID. Įsitikinkite, kad įmonės pavadinimas sutampa su pavadinimu, kuris rodomas jūsų įmonės „LinkedIn” puslapyje. Daugiau informacijos apie „LinkedIn” įmonės ID, žr. [„LinkedIn” įmonės ID su „LinkedIn” darbo skelbimų lenta susiejimas – dažnai užduodami klausimai](https://www.linkedin.com/help/linkedin/answer/98972).

    Jei jums reikia pakeisti tam tikrą savo organizacijos informaciją, žr. [Organizacijos adreso, techninio kontakto ir kt. pakeitimas](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Jei vis dar kyla problemų, susisiekite su [„LinkedIn“ palaikymo tarnyba](https://www.linkedin.com/help/linkedin).

4. Pasirinkite **Įrašyti**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>„LinkedIn Recruiter“ ir „Attract“ nustatymas 

Norėdami leisti darbdaviams siūlyti darbo vietas „LinkedIn Recruiter”, turite sukonfigūruoti integraciją su „LinkedIn Recruiter” programoje „Attract”. Norėdami baigti konfigūravimo procesą, turite bendradarbiauti su vartotoju, kuris yra jūsų įmonės „LinkedIn Recruiter“ sutarties administratorius.

1. Meniu **Sąranka** (krumpliaračio simbolis) viršutiniame dešiniajame kampe pasirinkite **Administravimo centras**. Taip pat galite pereiti į <https://attract.talent.dynamics.com/adminsettings>.
2. Pasirinkite skirtuką **„LinkedIn‟ integravimas**.

    [![„Attract“ administratoriaus rodinys, skirtas pradėti „LinkedIn Recruiter“ integravimą](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Norėdami pradėti nustatymą, pasirinkite **Prisijungti**. Jums bus pateikti nurodymai, kaip prisijungti „LinkedIn“.
4. Jei turite vietų keliose „LinkedIn“ sutartyse, pasirinkite sutartį, kurią norėtumėte prijungti prie „Attract“ sistemos. Jei turite tik vieną vietą „LinkedIn“ sutartyje, galite praleisti šį veiksmą.
5. Skiltyje **„Recruiter System Connect” (RSC)** pasirinkite **Teikti užklausą**.

    [![„Attract“ administratoriaus rodinys, skirtas „LinkedIn Recruiter“ integravimo užklausai pateikti](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **„Recruiter System Connect” (RSC)** parametras dabar turėtų būti rodomas kaip **Partneris paruoštas**. Jei šiame puslapyje matote parinktį **Įspėti partnerį**, palaukite keletą sekundžių, pasirinkite **Įspėti partnerį**, tada atnaujinkite puslapį. Parametras dabar turėtų būti rodomas kaip **Partneris paruoštas**.

    [![„Attract“ administratoriaus rodinys, skirtas nurodyti, kad „Attract“ pusės užklausos yra įvykdytos](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Norėdami atlikti toliau nurodytus veiksmus, privalote turėti administratoriaus teises „LinkedIn Recruiter“ sutartyje.

    1. Prisijunkite prie „LinkedIn” naudodami savo administratoriaus abonementą, tada viršutiniame dešiniajame kampe pasirinkite **LinkedIn Recruiter**. 
    2. Puslapio viršuje esančiame meniu **Daugiau** pasirinkite **Administravimo parametrai**, tada pasirinkite skirtuką **ATS**.
    3. Norėdami įgalinti tik vienos sutarties eksportavimą vienu spustelėjimu, įjunkite **Sutarties lygio prieiga (kiekvienai šios sutarties vietai)**. Norėdami jį įgalinti visai įmonei, įjunkite **Įmonės lygio prieiga (kiekvienai jūsų įmonės sutarčiai)**.

    [![Įjunkite „Attract“ integravimą apsilankę „LinkedIn Recruiter“ administratoriaus rodinyje](./media/EnableRSC.png)](./media/EnableRSC.png)

8. „Attract” administravimo centre pasirinkite skirtuką **„LinkedIn” integravimas**. **„Recruiter System Connect” (RSC)** parametras dabar turėtų būti rodomas kaip **Įgalintas**.

    [![„LinkedIn Recruiter“ Integravimas baigtas](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Prašymo teikimo naudojant „LinkedIn“ programoje „Attract“ nustatymas

Jūs galite leisti kandidatams teikti prašymus dėl jūsų darbo vietų, naudojant savo „LinkedIn” profilius. Norėdami gauti daugiau informacijos apie prašymo teikimą naudojant „LinkedIn“, žr. [„LinkedIn” galia visur: prašymo teikimas naudojant „LinkedIn“](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Šiuo metu ši funkcija yra peržiūrima. Prieš atlikdami šiuos veiksmus, įsitikinkite, kad prašymo teikimas naudojant „LinkedIn” yra įgalintas. Daugiau informacijos apie peržiūros funkcijų įgalinimą žr. [Prieiga prie „Talent“ peržiūros funkcijų](./access-preview-feature.md).

1. Meniu **Sąranka** (krumpliaračio simbolis) viršutiniame dešiniajame kampe pasirinkite **Administravimo centras**. Taip pat galite pereiti į <https://attract.talent.dynamics.com/adminsettings>.
2. Pasirinkite skirtuką **„LinkedIn‟ integravimas**.

    [![„Attract“ administratoriaus rodinys, skirtas pradėti „LinkedIn Recruiter“ integravimą](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Norėdami **teikti prašymą naudojant „LinkedIn”**, pasirinkite **Prisijungti**, kad pradėtumėte nustatymą. Jums bus pateikti nurodymai, ką daryti toliau naudojant „LinkedIn”.

## <a name="see-also"></a>Taip pat žiūrėkite

[DUK apie „LinkedIn“](./attract-linkedin-faq.md)

[Darbo skelbimų skelbimas išorinėse svetainėse sprendime „Attract“](./posting-jobs-external.md)

[Kandidatų ieška naudojant „LinkedIn Recruiter”](./attract-linkedin-recruiter.md)

[Darbo vietų kūrimas](./creating-jobs-attract.md)

[Integravimo su „LinkedIn“ trikčių diagnostika](./attract-troubleshoot-linkedin.md)
