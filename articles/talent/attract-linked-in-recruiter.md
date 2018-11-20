---
title: "Darbuotojų pasirinkimas naudojant „LinkedIn Recruiter“"
description: "Šioje temoje pateikiama informacija mašininio mokymo naudojimą norint gauti darbų ir kandidatų į darbo vietas rekomendacijas."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: lt-lt
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>Darbuotojų pasirinkimas naudojant „LinkedIn Recruiter“
[!include[banner](../includes/banner.md)]

„LinkedIn“ yra didžiausia pasaulyje talentų duomenų bazė ir dažnai tai yra pagrindinė sistema, kurią naudodami darbdaviai ieško, bendrauja ir skiria užduotis kandidatams, kurie įdarbintojams reikalingi. „LinkedIn Recruiter“ integravimas su „Dynamics 365 for Talent: Attract“ palengvina vartotojų samdos procesą ir sinchronizuoja duomenis abiejose sistemose.

> [!NOTE]
> Jums reikia išsamios įdarbinimo informacijos priedo ir „LinkedIn Recruiter“ vietų, kad galėtumėte naudoti „LinkedIn Recruiter“ integravimą su „Attract“.

## <a name="set-up-linkedin-recruiter-with-attract"></a>„LinkedIn Recruiter“ is „Attract“ nustatymas 

Prieš naudodami „LinkedIn Recruiter“ galimybes, turite sukonfigūruoti sutarties lygio arba įmonės lygio prieigą su savo „Attract“ egzemplioriumi. Norėdami atlikti konfigūravimo procesą, turite bendradarbiauti su vartotoju, kuris yra jūsų „LinkedIn Recruiter“ sutarties administratorius. Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte „LinkedIn Recruiter“ su „Attract“.

1.  Prisijunkite prie „Attract“ kaip administratorius ir pasirinkite **Administravimo parametrai**.

2.  Kairiojoje srityje spustelėkite skirtuką **„LinkedIn integravimas**.

[![„Attract“ administratoriaus rodinys, skirtas pradėti „LinkedIn Recruiter“ integravimą](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Spustelėkite **Jungtis**, kad pradėtumėte nustatymą ir būtų teikiamos prisijungimo prie „LinkedIn“ proceso instrukcijos.

4.  Jei turite vietų keliose „LinkedIn“ sutartyse, pasirinkite sutartį, kurią norėtumėte prijungti prie „Attract“ sistemos. Jei turite tik vieną vietą „LinkedIn“ sutartyje, šis veiksmas nėra būtinas.

5.  Tada „LinkedIn“ valdiklis bus įkeltas į jūsų administravimo parametrus ir bus rodomas integravimų sąrašas. Skiltyje **„Recruiter“ sistemos prijungimas** spustelėkite **Teikti užklausą**.

[![„Attract“ administratoriaus rodinys, skirtas pateikti užlausą dėl „LinkedIn Recruiter“ integravimo](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Pateikus integravimo užklausą iš „Attract“, bus rodoma būsena **Partneris paruoštas** ir jį bus galima įjungti **„Recruiter“ administravimo parametruose**. Jei šiame puslapyje matote parinktį **Įspėti partnerį**, palaukite keletą sekundžių, spustelėkite **Įspėti partnerį**, tada atnaujinkite puslapį. Dabar turėtų būti rodoma būsena **Partneris paruoštas**.

[![„Attract“ administratoriaus rodinys, skirtas nurodyti, kad „Attract“ pusės užklausos yra įvykdytos](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Norėdami atlikti kitą veiksmą, turite turėti administratoriaus teisę „LinkedIn Recruiter“ sutartyje.

7.  Prisijunkite prie „LinkedIn“ naudodami administratoriaus paskyrą ir viršuje dešinėje atidarykite skiltį „LinkedIn Recruiter“. 

8. Ekrano viršuje esančiame meniu **Daugiau** spustelėkite **Administravimo parametrai**, tada spustelėkite skirtuką **ATS**.

„Attract“ sistema bus nurodyta pateikiant kelias parinktis, kurias galima įjungti.

9. Jei norite įjungti tik 1 spustelėjimo eksportavimo parinktį, skirtą **ATS vidiniam indikatoriui** ir **ATS vidiniam profilio valdikliui**, pasirinkite **Įmonės lygio prieiga**. Jei norite įjungti visos įmonės lygio prieigos funkcijas ir „InMail“ retrospektyvos, pastabų retrospektyvos ir „InMail“ šaknelės profilio prieigą, pasirinkite **Sutarties lygio prieiga**.

10. Įjunkite norimą prieigos lygį „LinkedIn Recruiter“ **Administravimo ATS** parametruose.

[![Įjunkite „Attract“ integravimą iš „LinkedIn Recruiter“ administratoriaus rodinio](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Vėl atidarykite „Attract“ administravimo parametrus kaip „Attract“ administratorius ir pasirinkite skirtuką **„LinkedIn“ integravimas**. Dabar turėtumėte matyti įkeltą „LinkedIn“ valdiklį, nurodantį, kad pasirinkto lygio prieiga įjungta, ir rodantį būseną **Įjungta**.

[![„LinkedIn Recruiter“ integravimas baigtas](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>„LinkedIn Recruiter“ galimybių naudojimas

Kai „Attract“ administratorius įjungia „LinkedIn Recruiter“ galimybes, jas gali pasiekti samdos vadovai ir įdarbintojai. Norėdami naudoti šias galimybes, prijunkite „LinkedIn“ paskyrą skiltyje **Vartotojo parametrai**. Kai administratoriaus ir vartotojo parametrai prijungiami, galima naudoti keletą galimybių.

### <a name="in-ats-profile-widget"></a>Vidinio ATS profilio valdiklis

Kandidato „LinkedIn“ profilį galite peržiūrėti „Attract“. „LinkedIn“ valdiklis rodys kandidato profilį, kai ATS informacija sutaps su „LinkedIn“ vartotojų informacija.

Norėdami peržiūrėti profilį, atidarykite kandidato profilį iš darbų arba talentų telkinio. Kandidato profilyje pasirinkite skirtuką **LinkedIn** ir bus įkeltas profilio valdiklis. Naudodami profilio valdiklį, nurodykite, ar tai teisingas atitikimas. Jei ne, raskite tinkamą asmenį. Taip pat galite įrašyti kandidatą savo „LinkedIn Recruiter“ projektuose šiame puslapyje.

### <a name="1-click-export"></a>1 spustelėjimo eksportavimas 

Samdydami kandidatus „LinkedIn“ galite 1 spustelėjimu eksportuoti kandidatą į darbus, kurie šiuo metu atidaryti. Atlikite tolesnius veiksmus, norėdami naudoti 1 spustelėjimo eksportavimo funkciją. Prieš baigdami šiuos veiksmus, įsitikinkite, kad jums priskirtas darbo samdos vadovo arba įdarbintojo vaidmuo, o darbo etapas yra **Potencialus klientas**.

1.  Kurkite darbus, priskirkite atitinkamiems vaidmenims ir aktyvinkite užduotis.

2.  Kai užduotis yra suaktyvinta, atidarykite „LinkedIn Recruiter“.

3.  Rasti ieškomą kandidatą ir atidarykite jo profilį.

4.  Naudodami darbo ieškos lauką kontakto kortelėje raskite darbą: naudokite pareigas arba užduoties ID, kuris buvo suaktyvintas „Attract“. Jei užduoties nerasite, spustelėkite **Keisti ATS**, kad rastumėte tinkamą „Attract“ egzempliorių.

5. Pasirinkę darbą spustelėkite **Eksportuoti**. Dabar kandidato duomenis nuskaito „Attract“.

6.  Atidarykite „Attract“ ir atidarykite atitinkamą darbą. Eksportuotą kandidatą rasite etapo **Potencialus klientas** darbe.

### <a name="in-ats-indicator"></a>Vidinio ATS indikatorius 

Naudodami „LinkedIn Recruiter“ galite sekti, ar kandidatas pateikė prašymą dėl kitų darbo vietų jūsų organizacijoje, pažiūrėti, kokie skirtingi jo prašymų dėl darbo etapai ir peržiūrėti atsiliepimus bei komentarus iš „Attract“ sistemoje „LinkedIn Recruiter“.

1.  Atidarykite „LinkedIn Recruiter“ ir suraskite ieškomo kandidato profilį.

2.  Slinkite žemyn ir peržiūrėkite skiltį **Vidinis ATS**, pateiktą kandidato profilyje.

3.  Šį valdiklį galite naudoti norėdami peržiūrėti visą informaciją apie kandidatą, kuris nurodytas „LinkedIn Recruiter“ rodinyje.

4.  Pasirinkite skirtuką **Darbai ir būsenos** norėdami peržiūrėti sudėtinius darbus, naujausias būsenas ir tai, kaip sekasi vykdyti bet kurį iš darbų.

5.  Pasirinkite skirtuką **Pokalbio atsiliepimas**, kad pamatytumėte atsiliepimą, kurį kalbintojai pateikė „Attract“.

6.  Pasirinkite skirtuką **Pastabos**, kad pamatytumėte „Attract“ užfiksuotas pastabas apie šį kandidatą.

### <a name="inmail-history"></a>„InMail“ retrospektyva

„LinkedIn InMail“ retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“. Kai ji įjungta, galite peržiūrėti visą „InMail“ restrospektyvą, susijusią su kandidatais. Taip pat galite peržiūrėti, kas dar iš jūsų organizacijos susirašinėjo su kandidatu naudodami „InMail“, tačiau negalite peržiūrėti jų žinučių.

Norėdami peržiūrėti „InMail“ retrospektyvą, atidarykite kandidato profilį, pasirinkite skirtuką **LinkedIn** ir slinkite į puslapio apačią, kad peržiūrėtumėte retrospektyvą. „InMail“ retrospektyvą galite peržiūrėti tik jei kandidatas yra atsakė į jūsų užklausą ir pasirinkto su jumis bendrinti savo profilį naudodami „LinkedIn InMail“. Pranešimus iš „InMail“ sinchronizuojami su „Attract“ kas kelias valandas.

### <a name="notes-history"></a>Pastabų retrospektyva 

„LinkedIn“ pastabų retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“. Kai ji įjungta, galite peržiūrėti pastabas, susietas su kandidatu ir užfiksuotas įvairių įdarbintojų iš jūsų organizacijos.

Norėdami peržiūrėti pastabų retrospektyvą, atidarykite kandidato profilį, pasirinkite skirtuką **LinkedIn** ir slinkite į puslapio apačią, kad peržiūrėtumėte retrospektyvą. Visas pastabas apie kandidatą galite peržiūrėti iš „LinkedIn Recruiter“.

### <a name="inmail-stub-profile"></a>„InMail“ šaknelės profilis

„InMail“ šaknelės retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“. Jei kandidatai sutinka bendrinti savo „LinkedIn“ profilį su bet kuriuo vartotoju jūsų organizacijoje, galėsite sekti kandidatus „Attract“ bus sukurtas kiekvieno kandidato įrašas.

Norėdami peržiūrėti kandidatų sąrašą, pasirinkite **Talentų telkinius**, kad peržiūrėtumėte sistemos sukurtą „LinkedIn“ talentų telkinį. Šiame talentų telkinyje kandidatai ir jų šaknelės profiliai pateikiami pagal „LinkedIn“ sistemą, kuriame rodomi kandidato vardas ir pavardė. Kandidato el. pašto adreso ID bus rodomas, jei kandidatas pasirinko bendrinti savo el. pašto adresą.

