---
title: „E-commerce“ vertinimo aplinkos konfigūravimas
description: Šiame vadove pateikiamos išsamios instrukcijos, kaip sukonfigūruoti ir konfigūruoti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771685"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>„E-commerce“ vertinimo aplinkos konfigūravimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šiame vadove pateikiamos išsamios instrukcijos, kaip sukonfigūruoti ir konfigūruoti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką. Prieš pradedant rekomenduojame bent peržvelgti dokumentaciją, kad suprastumėte, koks tai procesas ir kas nurodyta vadove.

*Pastaba. Jei dar nesate suteikę prieigos prie „Microsoft Dynamics 365 Commerce“ peržiūros, galite prašyti prieigos prie peržiūros [„Commerce“ svetainėje](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Suvestinė
Norint sėkmingai parengti aplinką, reikia sukurti projektą su tam tikru produkto pavadinimu ir tipu. Aplinka ir „Retail Cloud Scale Unit“ taip pat turi tam tikrų konkrečių parametrų, kuriuos reikia naudoti, kad vėliau būtų pradėtas el prekybos parengimas. Šio vadovo instrukcijose yra visi reikiami veiksmai, kuriuos reikia atlikti, ir parametrai, kuriuos reikia naudoti.

Sėkmingai parengus reikia atlikti keletą veiksmų po parengimo, kad būtų paruošta peržiūros aplinka. Kai kurie veiksmai yra pasirinktiniai, priklausomai nuo to, kokius sistemos aspektus norite įvertinti. Jei vėliau persigalvosite, galėsite visada vėliau vykdyti papildomus veiksmus.

Jei turite klausimų dėl parengimo veiksmų arba kyla problemų, praneškite apie tai [„Microsoft Dynamics 365 Commerce“ peržiūros „Yammer“ grupėje.](https://aka.ms/Dynamics365CommercePreviewYammer) 

## <a name="prerequisites"></a>Būtinieji komponentai
Toliau pateikti būtinieji komponentai, reikalingi rengiant savo „Dynamics 365“ peržiūros aplinką:
* Turite prieigą prie **„Lifecycle Services“ paslaugų portalo (LCS)**
* Buvote **priimti į „Dynamics 365 Commerce“ peržiūros programą**
* Turite reikiamas teises kurti **Galimi išankstiniai pardavimai** arba **Perkelti, kurti sprendimus ir sužinoti** projektą
* Jūs esate vaidmens **Aplinkos administratorius** arba **Projekto savininkas** narys projekte, kuriame ruošite aplinką
* Jūs turite administratoriaus prieigą prie savo „Azure“ prenumeratos arba prenumeratos administratoriaus, kuris gali atlikti du veiksmus, reikalaujančius administratoriaus teisių jūsų vardu, kontaktą
* Jūs galite pasiekti savo **AAD nuomotojo ID**
* Sukūrėte **AAD saugos grupę**, kuri bus naudojama kaip **el. prekybos sistemos administratorių grupė**, o jūs turite jos ID
* Sukūrėte **AAD saugos grupę**, kuri bus naudojama kaip **įvertinimų ir apžvalgų moderatoriaus grupė**, o jūs turite jos ID (gali būti tas pats SG kaip sistemos administratoriaus grupė viršuje)
## <a name="provisioning-preview-environment"></a>Peržiūros aplinkos parengimas
Šios instrukcijos apima „Microsoft Dynamics 365 Commerce“ peržiūros aplinkos parengimą. Po to, kai sėkmingai užbaigėte šiuos veiksmus, turėsite konfigūruotiną peržiūros aplinką. Visos čia aprašytos veiklos vyksta LCS portale.

*Atkreipkite dėmesį, kad peržiūros prieiga yra susieta su LCS paskyra ir organizacija, kurią nurodėte savo peržiūros programoje. Turite naudoti tą pačią paskyrą, kad būtų galima atlikti parengimą. Jei norite, kad peržiūros aplinkoje galėtumėte naudoti skirtingas LCS paskyras arba nuomotoją, turite mums pateikti šiuos duomenis. Dėl kontaktinės informacijos žr. toliau „Papildomi ištekliai“.*
### <a name="before-starting"></a>Prieš pradedant
##### <a name="grant-access-to-e-commerce-applications"></a>Prieigos prie el. prekybos programų suteikimas

*Pastaba. **Asmuo, kuris prisijungia, turi būti AAD nuomotojo administratorius**. Sėkmingai neužbaigus šio veiksmo, kitų parengimo veiksmų nepavyks atlikti.*

1. Šiam žingsniui reikia jūsų **AAD nuomininko ID**. Norėdami pasiekti savo „Azure“ prenumeratą, turite autorizuoti el. prekybos programas. Lengviausias būdas tai atlikti yra surinkti tokį URL:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Nespauskite URL tiesiogiai** – tiesiog kopijuokite ir įklijuokite jį į savo naršyklę arba teksto rengyklę ir pakeiskite **\{AAD_TENANT_ID\}** į savo **AAD nuomotojo ID**, prieš pereidami į URL.
3. Jums bus pateiktas „Microsoft“ AAD registravimosi dialogo langas, kuriame patvirtinsite, kad norite suteikti „Dynamics 365 Commerce (Peržiūros)“ prieigą prie savo prenumeratos.
4. Jums bus rodomas puslapis, kuris patvirtina, ar operacija buvo sėkminga.

##### <a name="log-in-to-the-lcs"></a>Prisijunkite prie LCS.
1. Prisijunkite prie LCS protalo: https://lcs.dynamics.com
1. Įsitikinkite, kad prisijungėte naudodami tą pačią LCS paskyrą, kurią naudojote prašydami prieigos prie peržiūros.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Patvirtinkite, kad peržiūros funkcijos prieinamos ir įgalintos
1. LCS pagrindiniame puslapyje slinkite į dešinę iki pat galo ir spustelėkite plytelę **Peržiūros versijos funkcijų valdymas**.
1. Slinkite žemyn iki „ASMENINĖS PERŽIŪROS FUNKCIJOS“ ir įsitikinkite, kad galimos šios funkcijos ir jos yra įgalintos:
    1. **El. prekybos vertinimas**
    1. **„Commerce“ peržiūros programos aplinkos**
1. Jei nematote šių funkcijų sąraše, kreipkitės į mus naudodami savo darbo el. pašto adresą, LCS paskyrą ir nuomininko išsamią informaciją. Daugiau informacijos apie tai, kaip su mumis susisiekti, žr. **Papildomi ištekliai**.

![Peržiūros versijos valdymo plytelė](./media/preview1.png)

![Peržiūros funkcijos](./media/preview2.png)
### <a name="create-project"></a>Kurti projektą
##### <a name="creating-new-project"></a>Naujo projekto kūrimas
1. Stustelėkite **+**, kad sukurtumėte naują projektą.
1. Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.
1. Jei esate klientas, pasirinkite **Galimi išankstiniai pardavimai**.
1. Įveskite pavadinimą, aprašą ir sektorių, kaip jums atrodo tinkama.
1. Dalyje **Produkto pavadinimas** pasirinkite **„Dynamics 365 Retail“**.
1. Dalyje **Produkto versija** pasirinkite **„Dynamics 365 Retail“**.
1. Dalyje **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.
1. Jei pageidaujama, galite importuoti vaidmenis ir vartotojus iš esamo projekto.
1. Spustelėkite **Kurti**.
1. Jūs nusiunčia į projekto rodinį.
##### <a name="add-azure-connector"></a>„Azure“ jungties įtraukimas
1. Jei esate partneris, spustelėkite **Projekto parametrai** įrankių plytelių dešinės pusės gale.
1. Jei esate klientas, iš viršutinio meniu pasirinkite **Projekto parametrai**.
1. Pasirinkite **„Azure“ jungtys**.
1. Norėdami įtraukti „Azure“ jungtį, spustelėkite **+ įtraukti**.
1. Įvesti vardą.
1. Įveskite savo **„Azure“ prenumeratos ID**.
1. Įjunkite **Konfigūruoti naudoti „Azure Resource Manager“ (ARM)**.
1. Įsitikinkite, kad **„Azure“ prenumeratos AAD nuomotojo domenas ( arba ID)** yra teisingas. Jei reikia, kreipkitės į „Azure“ prenumeratos administratorių.
1. Spustelėkite **Pirmyn**.
1. Sekite instrukcijas ekrane, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos. Jei reikia, kreipkitės į „Azure“ prenumeratos administratorių:
    1. Prisijunkite prie „Azure“ protalo: https://portal.azure.com/
    1. Įsitikinkite, kad pasirinkote tinkamą katalogą.
    1. Spustelėkite meniu kairėje pusėje **Prenumeratos**.
    1. Suraskite tinkamą prenumeratą iš sąrašo ir pasirinkite. Jei reikia, naudokite iešką.
    1. Pasirinkite iš meniu **Prieigos valdymas (IAM)**.
    1. Spustelėkite **Pridėti** dešinėje pusėje dalį **Įtraukti vaidmens priskyrimą**. Atidaroma sritis **Įtraukti vaidmens priskyrimą**.
    1. Kaip **vaidmenį** pasirinkite **Bendraautoris**.
    1. Dalyje **Priskirti prieigą prie**, palikite kaip **„Azure AD“ vartotojas, grupė arba paslaugos narys**.
    1. Dalyje **Pasirinkti** įveskite **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Sąraše pasirinkite **„Dynamics Deployment Services“ [wsfed-enabled]**.
    1. Spustelėkite **Įrašyti**.
1. Spustelėkite **Pirmyn**.
1. Sekite instrukcijas ekrane, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos. Jei reikia, kreipkitės į „Azure“ prenumeratos administratorių.
1. Spustelėkite **Pirmyn**.
1. Dalyje **„Azure“ regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.
1. Spustelėkite **Prisijungti**.
1. Jūsų „Azure“ jungtis turi pasirodyti sąraše.
### <a name="import-extension"></a>Plėtinio importavimas
1. Norėdami grįžti į savo projekto pagrindinį puslapį, spustelėkite projekto pavadinimą viršuje.
1. Jei esate partneris, spustelėkite **Išteklių biblioteka** įrankių plytelių dešinės pusės gale.
1. Jei esate klientas, iš viršutinio meniu pasirinkite **Išteklių biblioteka**.
1. Pasirinkite **Programinės įrangos diegimo paketas** iš sąrašo kairėje pusėje.
1. Spustelėkite veiksmų srityje **IMPORTUOTI**.
1. Pasirinkite turto sąraše **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**, esančio **BENDRAI NAUDOJAMŲ IŠTEKLIŲ BIBLIOTEKA**.
1. Spustelėkite **Pasirinkti**.
1. Jūs būsite grąžinti į išteklių biblioteką ir turėtumėte matyti plėtinį sąraše.

![Projekto kūrimas – versijos](./media/import.png)
### <a name="deploy-environment"></a>Diegti aplinką

*Pastaba. Gali būti, kad 6, 7 ir (arba) 8 veiksmai nebus rodomi, nes bus praleisti ekranai su vienu pasirinkimu. Kai esate rodinyje **Aplinkos parametrai**, patvirtinkite, kad turite tekstą „Dynamics 365 Commerce“ (peržiūra) – demonstracinė versija (10.0.6 su 30 platformos naujinimu) tiesiai virš lauko **Aplinkos pavadinimas**. Toliau žr. ekrano kopiją.*

1. Iš viršutinio meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Spustelėkite **+ Įtraukti**, kad pridėtumėte aplinką.
1. Dalyje **Programos versija** pasirinkite **10.0.6**.
1. Dalyje **Platformos versija** pasirinkite **30 platformos naujinimas**.
1. Spustelėkite **Pirmyn**.
1. Aplinkos topologijoje pasirinkite **DEMONSTRACINĖ VERSIJA**.
1. Aplinkos topologijoje pasirinkite **„Dynamics 365 Commerce“ (peržiūra) – Demonstracinė versija**.
1. Jei anksčiau sukonfigūruosite vieną „Azure“ jungtį, kuri bus naudojama šioje aplinkoje. Jei sukonfigūravote kelias „Azure“ jungtis, galite pasirinkti, kurią jungtį norite naudoti: **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2** (rekomenduojama geriausiam betarpiškam našumui užtikrinti)
1. Įveskite **Aplinkos pavadinimas**.
1. Koreguokite VM dydį, kaip jums atrodo tinkama. (Rekomenduojame VM SKU **D13 v2**.)
1. Nieko nekeiskite srityje **Išplėstiniai parametrai**.
1. Ekrane peržiūrėję įkainius ir licencijavimo sąlygas, pažymėkite žymės langelį, kad sutinkate.
1. Spustelėkite **Pirmyn**.
1. Diegimo patvirtinimo ekrane, patikrinę, kad išsami informacija yra teisinga, spustelėkite **Diegti**.
1. Jūs grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka bus rodoma sąraše.
1. Jūsų pageidaujama aplinka bus rodoma eilėje ir dar diegiama. Praeis kažkiek laiko, kol visos aplinkos darbo eigos bus užbaigtos, todėl po kelių valandų (maždaug 6–9 val.) patikrinkite.
1. Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.

![Projekto kūrimas – versijos](./media/project1.png)

![Projekto kūrimas – topologija 1](./media/project2.png)

![Projekto kūrimas – topologija 2](./media/project3.png)

![Projekto kūrimas – aplinkos parametrai](./media/project4.png)
### <a name="initialize-rcsu"></a>Paleiskite RCSU.
1. Būdami rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.
1. Dešinėje ekrano pusėje esančiame aplinkos rodinyje spustelėkite **Visa išsami informacija**. Bus rodomas aplinkos išsamios informacijos rodinys.
1. Dalyje **APLINKOS FUNKCIJOS** spustelėkite **Valdyti**.
1. Skirtuke **„Retail“** spustelėkite **Paleisti**. Bus rodomas RCSU inicijavimo parametrų rodinys.
1. Dalyje **REGIONAS** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.
1. Dalyje **VERSIJA** pirmiausia pasirinkite **Nurodyti versiją** iš išplečiamojo sąrašo, tada žemiau pasirodysiančiame teksto lauke nurodykite **9.16.19262.5**. *Pastaba. Įsitikinkite, kad **tiksliai nurodėte versiją**, kuri čia pateikiama, kad nereikėtų naujinti RCSU vėliau, kad pataisytumėte versiją.*
1. Įjunkite **Taikyti plėtinį**.
1. Iš plėtinių sąrašo pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.
1. Spustelėkite **Inicijuoti**.
1. Diegimo patvirtinimo ekrane, patikrinę, kad išsami informacija yra teisinga, spustelėkite **Taip**.
1. Jūs grąžinami į rodinį **„Retail“ valdymas** su suaktyvintu skirtuku **„Retail“**. Jūsų RCSU jau buvo rengimo eilėje.
1. Palaukite, kol RCSU būsena taps **SĖKMINGA** prieš tęsdami (užtruks apie 2–5 val.).
### <a name="initialize-e-commerce"></a>El. prekybos inicijavimas
1. Pereikite į skirtuką **El. prekyba (peržiūra)**.
1. Peržiūrėję peržiūros versijos sutikimą, spustelėkite **Sąranka**.
1. Įveskite **El. prekybos nuomotojo pavadinimas** pavadinimą. Tačiau atkreipkite dėmesį, kad tai bus matoma kai kuriuose URL, nukreiptuose į jūsų el. prekybos egzempliorių.
1. Iš **„Retail Cloud Scale Unit“ pavadinimas** sąrašo pasirinkite savo RCSU (sąraše turi būti tik viena parinktis).
1. **El. prekybos geografija** automatiškai įvedama ir negali būti keičiama.
1. Spauskite **Pirmyn**, kad tęstumėte.
1. Į **Palaikomi pagrindinio kompiuterio vardai** įveskite bet kokį tinkamą domeną (pvz., www.fabrikam.com).
1. Į **AAD saugos grupė sistemos administratoriui** įveskite AAD SG ID, kurį pageidaujate naudoti kaip el. prekybos sistemos administratoriaus grupę.
1. Į**AAD saugos grupė įvertinimų ir apžvalgų moderatoriui** įveskite AAD SG ID, kurį norite naudoti kaip įvertinimų ir apžvalgų moderatoriaus grupę.
1. Palikite **B2C** vertes tuščias (7 laukus, prasidedančius B2C).
1. Palikite **Įjungti įvertinimų ir apžvalgų paslaugą** įgalintą.
1. Spustelėkite **Inicijuoti**.
1. Jūs grąžinami į rodinį **„Retail“valdymas** su suaktyvintu skirtuku **El. prekyba (peržiūra)**. Jūsų el. prekybos inicijavimas pradėtas.
1. Prieš pradėdami, palaukite, kol el. prekybos inicijavimo būsena bus **INICIJUOTA SĖKMINGAI**.
1. Dalyje **SAITAI** apačioje dešinėje.
    * Atkreipkite dėmesį į saitą **el. prekybos svetainė**. Tai yra saitas į šakninę jūsų C2 svetainę.
    * Atkreipkite dėmesį į saitą **el. prekybos svetainės valdymo įrankis**. Tai yra saitas į svetainės valdymo įrankį (C1 kūrimo įrankis).
## <a name="post-provisioning-steps"></a>Veiksmai po parengimo
Šiame etape aplinka buvo parengta betarpiškai, bet vis dar yra konfigūracijos veiksmų, kurie turi atlikti prieš pradedant vertinti aplinką.
### <a name="before-starting"></a>Prieš pradedant
1. Iš viršutinio meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Spustelėkite **Visa išsami informacija** aplinkos informacijos dešinėje.
1. Spustelėkite **Prisijungimas**, kad atidarytumėte meniu, pasirinkite **Įeiti į aplinką**.

Įsitikinkite, kad pasirinktas juridinis subjektas **USRT** (viršutiniame dešiniajame kampe).

### <a name="configure-pos"></a>Konfigūruoti POS
##### <a name="associate-worker-with-your-identity"></a>Partnerio darbininkas su jūsų tapatybe
1. Naudodami meniu kairėje, eikite į **Moduliai > „Retail“ > Darbuotojai > Darbininkai**.
1. Sąraše raskite ir pasirinkite įrašą **000713 - Andrew Collette**.
1. Veiksmų srityje spustelėkite **„Retail“**.
1. Spustelėkite **Susieti esamą tapatybę**.
1. Lauke **El. paštas** (**Ieškoti naudojant el. paštą** lauko dešinėje) įveskite savo el. pašto adresą.
1. Spustelėkite **Ieškoti**.
1. Pasirinkite įrašą su savo vardu.
1. Spustelėkite **Gerai**.
1. Spustelėkite **Įrašyti**.
##### <a name="activate-cloud-pos"></a>Aktyvinti debesies EKA
1. Prisijunkite prie LCS protalo:.
1. Pereikite į savo projektą.
1. Iš viršutinio meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Spustelėkite **Visa išsami informacija** aplinkos informacijos dešinėje.
1. Spustelėkite **Prisijungimas**, kad atidarytumėte meniu, pasirinkite **Įeiti į debesies elektroninį kasos aparatą**, EKA turėtų būti įkeltas.
1. Spustelėkite **Pirmyn**.
1. Prisijunkite su savo AAD paskyra.
1. Dalyje **Parduotuvės pavadinimas**pasirinkite **San Franciskas**.
1. Spustelėkite **Pirmyn**.
1. Dalyje **Registras ir įrenginys**pasirinkite **SANFRAN-1**.
1. Spustelėkite **Aktyvinti**.
1. Turite atsijungti ir atsirasite EKA prisijungimo ekrane.
1. Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.
### <a name="site-setup"></a>Svetainės sąranka
1. Prisijunkite prie **svetainės valdymo įrankio** naudodami URL, kurį anksčiau pasižymėjote.
1. Spustelėkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.
1. Domenui rinkitės domeną, kurį įvedėte anksčiau, kai paleidote el. prekybą.
1. Norėdami naudoti numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**. *Pastaba. Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę*
1. Norėdami nustatyti numatytąją kalbą, pasirinkite**lt-lt**.
1. Nekeiskite **kelio**.
1. Spustelėkite **Gerai**.
1. Būsite nukreipti į svetainės puslapių sąrašą.
### <a name="enable-jobs"></a>Užduočių įgalinimas
1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami meniu kairėje, eikite į **„Retail“ > Užklausos ir ataskaitos > Paketines užduotys**.
1. Atlikite toliau nurodytus veiksmus kiekvienai užduočiai tolesniame sąraše:
    * **Apdorokite mažmeninės prekybos užsakymo el. laiško pranešimą**.
    * **Produkto pasiekiamumas**.
    * **P-0001**.
    * **Sinchronizuokite užsakymo užduotį**.
1. Naudokite spartųjį filtrą ieškoti užduotį naudodami jos pavadinimą (nurodytą anksčiau).
1. Jei užduoties būsena yra **Sulaikyta**, atlikite šiuos veiksmus:
    1. Pasirinkite įrašą.
    1. Veiksmų srityje atidarykite juostelę **Paketinė užduotis** ir spustelėkite **Keisti būseną**.
    1. Pasirinkite **Laukiama** ir spustelėkite **Gerai**.
### <a name="run-full-data-sync"></a>Vykdyti visą duomenų sinchronizavimą
1. Naudodami meniu kairėje, eikite į **Moduliai > „Retail“ > Būstinės sąranka > Duomenų apsikeitimo valdymas > Kanalo duomenų bazė**.
1. **Numatytasis** kanalas pasirenkamas iš kairiojo sąrašo. *Pasirinkite kitą galimą kanalą (pavadintą **scXXXXXXXXX**)*.
1. Spustelėkite veiksmų srityje **Visas duomenų sinchronizavimas**.
1. Įveskite **9999** kaip paskirstymo grafiką.
1. Spustelėkite **Gerai**.
1. Spustelėkite **Gerai**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Atlikę šiuos veiksmus, esate pasirengę atlikti savo peržiūros aplinkos vertinimą!
Naudokite **el. prekybos svetainės valdymo įrankio** URL, kad galėtumėte pereiti į C1 kūrimo patirtį, ir naudokite **el. komercijos svetainės** URL, kad galėtumėte pereiti prie C2 svetainės patirties.

## <a name="additional-resources"></a>Papildomi ištekliai
### <a name="how-to-find-your-aad-tenant-id"></a>Kaip rasti AAD nuomotojo ID
AAD nuomotojo ID yra GUID ir atrodo kaip šis pavyzdys:**72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Iš „Azure“ portalo
1. Prisijunkite prie „Azure“ protalo: https://portal.azure.com/
1. Įsitikinkite, kad pasirinkote tinkamą katalogą.
1. Spustelėkite meniu kairėje pusėje **„Azure Active Directory“**.
1. Pasirinkite **Ypatybės** dalyje **Valdyti**.
1. AAD nuomotojo ID rodomas dalyje **Katalogo ID**.
##### <a name="from-openid-connect-metadata"></a>Iš OpenID „Connect“ metaduomenų
Sukurkite **OpenID URL**, pakeisdami **\{YOUR_DOMAIN\}** į savo domeną, pvz., microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration taps https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Pereikite į **OpenID URL** naudodami jame savo domeną.
1. AAD nuomotojo ID gali būti matomas keliose ypatybių vertėse.
1. Suraskite **authorization_endpoint** ir išskleiskite GUID iškart po **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Kaip rasti savo AAD saugos grupės ID
AAD saugos grupės ID yra GUID ir atrodo kaip šis pavyzdys: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Atliekant šį veiksmą, daroma prielaida, kad vartotojas yra grupės, su kuriai mėginama surasti ID, narys.
1. Pereikite į „Graph“ naršyklę: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Spustelėkite **Prisijungti naudojant „Microsoft“** ir prisijunkite naudodami savo kredencialus.
1. Prisijungę kairėje spustelėkite **Rodyti daugiau pavyzdžių**.
1. Įjunkite **Grupės** iš dešiniosios srities.
1. Uždarykite dešiniąją sritį.
1. Spustelėkite **visos grupės, kurioms priklausau**.
1. Raskite savo grupę teksto laukelyje **Atsakymo peržiūra**.
1. Saugos grupės ID yra pažymėtas po ypatybių **id**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Bandomosios kredito kortelės informacija atlikti bandomąjį pirkimą
Norėdami atlikti bandomąsias operacijas svetainėje, galite naudoti šią bandomosios kredito kortelės informaciją:

Kortelės numeris: 4111-1111-1111-1111, galiojimo pabaiga: 10/20, CVV: 737

*Pastaba. Bandomojoje svetainėje jokiu būdu nereikia bandyti naudoti faktinės kredito kortelės informacijos!*
### <a name="useful-links"></a>Naudingi saitai
* [LCS („Lifecycle services“)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU („Retail Cloud Scale Unit“)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [„Microsoft Azure“ portalas](https://azure.microsoft.com/en-us/features/azure-portal)
* [„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)
* [„Dynamics 365 Retail“ žinyno ištekliai](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>„Microsoft Dynamics 365 Commerce“ peržiūros versijos palaikymas
Jei atlikdami parengimo veiksmus patiriate, apsilankykite [„Microsoft Dynamics 365 Commerce“ peržiūros versijos „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer) dėl pagalbos. 

Jei jums kyla problemų prisijungiant prie „Yammer“ grupės, taip pat galite susisiekti su mumis elektroniniu paštu **Dynamics365Commerce@microsoft.com**. Šis el. pašto adresas nėra aktyviai stebimas, todėl tikėtina, kad bus atsakyta ne iš karto.
***
## <a name="prerequisites-for-optional-features"></a>Papildomų funkcijų būtinos sąlygos
Jei norite įvertinti operacines el. pašto funkcijas, turi būti įvykdytos šios būtinosios sąlygos:
* Turite pasiekiamą el. pašto serverį (SMTP serverį), kuris gali būti naudojamas iš „Azure“ prenumeratos, kur konfigūruojate peržiūros aplinką.
* Turite pasiekiamus serverio FQDN/IP, SMTP prievado numerį ir autentifikavimo informaciją.

Jei norite įvertinti skaitmeninių išteklių valdymo funkcijas, konkrečiai tiesiogiai naudoti naujus daugiakanalio atvaizdus, turi būti įvykdytos šios išankstinės sąlygos:
* Turite turėti pasiekiamą savo **TVS nuomotojo pavadinimą**. Toliau pateikiami nurodymai, kaip rasti šį pavadinimą.
### <a name="configure-image-backend-optional"></a>Atvaizdo posistemio konfigūravimas (pasirinktinai)
##### <a name="finding-your-media-base-url"></a>Savo medijos pagrindinio URL radimas
*Pastaba. Kad galėtumėte atlikti šį veiksmą, turite užbaigti **svetainės sąranką**.*
1. Prisijunkite prie svetainės valdymo įrankio naudodami URL, kurį anksčiau pasižymėjote.
1. Atidarykite **„Fabrikam“** svetainę.
1. Meniu kairėje pusėje pasirinkite **Ištekliai**.
1. Pasirinkite bet kurį vieną vaizdo išteklių.
1. Suraskite **Viešasis URL** iš nuosavybės inspektoriaus dešinėje pusėje. Jame yra URL.
    * URL pavyzdys: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Pakeiskite paskutinį URL identifikatorių (MA1nQC, esantį aukščiau pateiktame URL pavyzdyje) naudodami šią eilutę: **search?fileName=**
    * URL pavyzdys po pakeitimo: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Tai yra jūsų **medijos pagrindinis URL** – atminkite.
##### <a name="updating-the-media-base-url"></a>Medijos pagrindinio URL naujinimas
1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami meniu kairėje, eikite į **Moduliai > „Retail“ > Kanalo sąranka > Kanalo profiliai**.
1. Spustelėkite **Redaguoti**.
1. Pakeiskite ypatybės iš **Profilio ypatybės** reikšmę **Medijos serverio pagrindinis URL** į anksčiau sukurtą **Medijos pagrindinis URL**.
1. Pasirinkite kitą kanalą iš sąrašo, esančio kairėje, dalyje **Numatytasis** kanalas.
1. Dalyje **Profilio ypatybės** spustelėkite **+ įtraukti**.
1. Įtrauktai ypatybei rinkite **Medijos serverio pagrindinis URL** kaip ypatybės raktą, o ypatybės vertę įveskite anksčiau sukurtą **Medijos pagrindinis URL**.
1. Spustelėkite **Įrašyti**.

### <a name="configure-email-server-optional"></a>El. pašto serverio konfigūravimas (pasirinktinai)
Atkreipkite dėmesį, kad SMTP serveris arba el. pašto paslauga, kurią čia įvedate, turi būti pasiekiami iš „Azure“ prenumeratos, kurią naudojate aplinkoje.
1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami meniu kairėje eikite į **Moduliai > „Retail“ > Būstinės sąranka > Parametrai > El. pašto parametrai**.
1. Spustelėkite skirtuką **SMTP parametrai**.
1. Lauke **Siunčiamo pašto serverio laukas** įveskite savo SMTP serverio arba el. pašto paslaugos FQDN ar IP adresą.
1. Lauke **SMTP prievado numeris** įveskite prievado numerį (numatytasis yra 25, kai nenaudojate SSL).
1. Lauke **Vartotojo vardas** įveskite reikšmę (jei reikia autentifikavimo).
1. Lauke **Slaptažodis** įveskite reikšmę (jei reikia autentifikavimo).
1. Spustelėkite **Įrašyti**.
1. Spustelėkite **Atnaujinti**.
1. Spustelėkite skirtuką **Bandomasis el. laiškas**.
1. Lauke El. pašto teikimo įrankis pasirinkite **SMTP**.
1. Lauke **Siųsti** įveskite el. pašto adresą, į kurį norite, kad bandomasis laiškas būtų išsiųstas.
1. Spustelėkite **Išsiųsti bandomąjį el. laišką**.
### <a name="configure-email-templates-optional"></a>El. laiškų šablonų konfigūravimas (pasirinktinai)
Kiekvieno operacinio įvykio, dėl kurio norite siųsti el. laiškus, el. laiškų šablonas turi būti atnaujintas, naudojant galiojantį siuntėjo el. pašto adresą.
1. Naudodami meniu kairėje eikite į **Moduliai > Organizacijos administravimas > Sąranka > Organizacijos el. laiškų šablonai**.
1. Spustelėkite **Rodyti sąrašą**.
1. Kiekvienam sąrašo šablonui:
    1. Lauke **Siuntėjo el. paštas** įveskite šio el. laiško šablono siuntėjo el. pašto adresą.
    1. (Pasirinktinai) lauke **Siuntėjo pavadinimas** įveskite pavadinimą, kuris bus naudojamas kaip šio el. laiško šablono siuntėjas.
1. Spustelėkite **Įrašyti**.
### <a name="customizing-email-templates-optional"></a>El. laiškų šablonų konfigūravimas (pasirinktinai)
Galbūt norėsite tinkinti el. laiškų šablonus naudodami skirtingus atvaizdus arba naujindami šablono saitus, kad jie nurodytų atgal į jūsų peržiūros aplinką. Toliau aprašomi veiksmai paaiškina, kaip atsisiųsti numatytuosius šablonus, juos tinkinti ir atnaujinti sistemos šablonus.
1. Naudodami naršyklę, atsisiųskite [„Microsoft Dynamics 365 Commerce“ peržiūros numatytųjų el. laiškų šablonų .zip failą](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), kuriame yra šie HTML dokumentai, skirti jūsų vietiniam kompiuteriui.
    1. Užsakymo patvirtinimo šablonas
    1. Dovanų kortelės išdavimo šablonas
    1. Naujo užsakymo šablonas
    1. Paketo užsakymo šablonas
    1. Paėmimo užsakymo šablonas
1. Tinkinkite šablonus naudodami teksto arba HTML rengyklę. Žiūrėkite toliau pateiktų palaikomų atpažinimo ženklų sąrašą.
1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami meniu kairėje eikite į **Moduliai > „Retail“ > Būstinės sąranka > Parametrai > Organizacijos el. laiškų šablonai**.
1. Išskleiskite sąrašą kairėje, kad pamatytumėte visus šablonus.
1. Kiekvienam šablonui, kurį norite tinkinti, atlikite šiuos veiksmus:
    1. Pasirinkite šabloną iš sąrašo.
    1. Dalyje **El. laiško pranešimo turinys** pasirinkite reikiamą kalbos versiją iš sąrašo (numatytoji **en-us**).
    1. Dalyje **El. laiško pranešimo turinys** spustelėkite **Redaguoti**, turėtumėte matyti atsidarančią sritį **Nusiųsti el. laiško šabloną**.
    1. Sustelėkite **Naršyti** ir raskite HTML failą, kuriame yra pritaikytas turinys.
    1. Spustelėkite **Nusiųsti**, jūsų šablonas nusiunčiamas į sistemą ir rodoma peržiūra.
    1. Spustelėkite **Gerai**.
    1. (Pasirinktinai) pritaikykite šablono ypatybę **Tema**.
    1. Spustelėkite **Įrašyti**.

#### <a name="supported-tokens-in-the-email-template"></a>Palaikomi el. laiškų šablono atpažinimo ženklai
Šie atpažinimo ženklai bus pakeisti el. pašto generavimo metu į faktines reikšmes, taikomas klientui ir jo užsakymui.

**Pardavimo užsakymas** – toliau nurodyti atpažinimo ženklai taikomi bendrai pardavimo užsakymui.

|Atpažinimo ženklo pavadinimas|Atpažinimo ženklas|
|---|---|
|Užsakymo numeris|%salesid%|
|Kliento pavadinimas|%customername%|
|Pristatymo adresas|%deliveryaddress%|
|Sąskaitų siuntimo adresas|%customeraddress%|
|Užsakymo data|%shipdate%|
|Pristatymo režimas|%modeofdelivery%|
|Nuolaida|%discount%|
|PVM|%tax%|
|Užsakymo suma|%total%|

**Pardavimo eilutė** – šiais atpažinimo ženklais yra užpildomas kiekvienas užsakymo produktas.

*Pastaba. Atpažinimo ženklai **Produktų sąrašas – pradžia** ir **Produktų sąrašas – pabaiga** yra HTML bloko pradžioje ir pabaigoje, ir taip kartojasi kiekvienam produktui.*

|Atpažinimo ženklo pavadinimas|Atpažinimo ženklas|
|---|---|
|Produktų sąrašas – pradžia|\<!--%tablebegin.salesline% -->|
|Produktų sąrašas – pabaiga|\<!--%tableend.salesline%-->|
|Produkto pavadinimas|%lineproductname%|
|Aprašymas|%lineproductdescription%|
|Kiekis|%linequantity%|
|Eilutės vieneto kaina|%lineprice% (tikrinti)|
|Iš viso eilutės elementų|%linenetamount%|
|eilutės nuolaida|%linediscount%|
|Siuntimo data|%lineshipdate%|
|Įsigijimo metodas|%linedeliverymode%|
|pristatymo adresas|%linedeliveryaddress%|
|Eilutės pardavimo vienetas|%lineunit%|

