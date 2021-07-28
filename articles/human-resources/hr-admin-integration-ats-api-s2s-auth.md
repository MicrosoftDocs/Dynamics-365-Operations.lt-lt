---
title: ATS integravimo API dviejų serverių autentifikavimas
description: Šioje temoje aprašoma, kaip nustatyti dviejų serverių autentifikavimą integravimams pagal „Dynamics 365 Human Resources” Pretendento sekimo sistemos (ATS) integravimo API.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ed76d22ab6b917c931220f3ba462f4f14cae207
ms.sourcegitcommit: bd684c9eb6de718573e6be5479e1832fe614d919
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6373066"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>ATS integravimo API dviejų serverių autentifikavimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašoma, kaip nustatyti dviejų serverių autentifikavimą programos integravimams pagal „Dynamics 365 Human Resources” Pretendento sekimo sistemos (ATS) integravimo API. Yra keli saugos sluoksniai, kuriuos reikia valdyti tarnybos vadovui, kad būtų galima pasiekti „Microsoft Dataverse” virtualią lentelę ir susijusius duomenis. Vartotojui turi būti suteikta prieiga prie „Dataverse” virtualios lentelės „Microsoft Power Platform” platformoje ir prieiga prie duomenų „Dynamics 365 Human Resources”.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Prieigos prie „Dataverse” virtualiųjų lentelių „Power Platform” platformoje įgalinimas

Pirmasis veiksmas įgalina prieigą prie „Dataverse” virtualių lentelių „Power Platform” platformoje, kad jūsų programa būtų nustatyta „Power Platform” autentifikacijai pagal „Dataverse” virtualios lentelės galinius punktus. Veiksmai, kaip tai atlikti, aprašyti [„Microsoft Dataverse” programuotojo vadove](/powerapps/developer/data-platform).

  - Vieno nuomininko programos registracijoms: [Naudokite dviejų serverių autentifikavimą vienam nuomininkui](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Kelių nuomininkų programos registracijoms: [Naudokite dviejų serverių autentifikavimą keliems nuomininkams](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Saugos vaidmens kūrimas ATS integravimams

Vienas iš veiksmų, sukūrus programos vartotoją, yra priskirti vartotoją saugos vaidmeniui, kuris nustato būsimą programos prieigą prie galinių punktų. Tai yra 7 [Programos vartotojo kūrimo](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) vieno nuomininko programos registracijoms ir [Programos saugos vaidmens kūrimo](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) kelių nuomininkų registracijoms veiksmas. 

Vaidmuo, kuriam priskiriate programos vartotoją, turėtų turėti prieigą prie duomenų objektų, naudojamų jūsų ATS integravimui. Jis nėra parengtas naudojimui, todėl reikės sukurti naują saugos vaidmenį. Naujas vaidmuo gali būti sukurtas atliekant į veiksmus, aprašytus [Saugos vaidmens kūrimas](/power-platform/admin/create-edit-security-role#create-a-security-role).

Naujam vaidmeniui turi būti priskirta atitinkama prieiga bent prie toliau pateiktų naujo vaidmens objektų **Tinkintų objektų** skirtuke. Atkreipkite dėmesį, kad gali reikėti įtraukti papildomus objektus, jei integruojant naudojami išplėstiniai programos duomenys. Sukūrus naują vaidmenį, jį galima priskirti programos vartotojui.

  - Pagrindinis darbuotojas (mshr)
  - Samdytinas pretendentas (mshr)
  - Sertifikato kompetencija (mshr)
  - Sertifikato tipas (mshr)
  - Įmonė
  - Kompensacijos užduoties funkcija (mshr)
  - Kompensacijos užduoties tipas (mshr)
  - Šalis/regionai (mshr)
  - Padalinys (mshr)
  - Išsilavinimo kompetencija (mshr)
  - Išsilavinimo laipsnis (mshr)
  - Išsilavinimo disciplinos (mshr)
  - Išsilavinimo reikalavimai (mshr)
  - Identifikacija (mshr)
  - Identifikacijos tipas (mshr)
  - Institucija (mshr)
  - Išduodanti agentūra (mshr)
  - Darbo atlygis (mshr)
  - Darbai (mshr)
  - Išsilavinimo lygis (mshr)
  - Šalies kontaktai (mshr)
  - Asmenys (mshr)
  - Asmens adresai (mshr)
  - Asmens atranka (mshr)
  - Pareigų tipas (mshr)
  - Pareigos V2 (mshr)
  - Profesinės patirties kompetencija (mshr)
  - Vertinimo lygis (mshr)
  - Vertinimo modeliai (mshr)
  - Priežasties kodai (mshr)
  - Įdarbinimo užklausa (mshr)
  - Įdarbinimo užklausos vieta (mshr)
  - Įdarbinimo užklausos pareigos (mshr)
  - Įdarbinimo užklausos įgūdžiai (mshr)
  - Atrankos tipas (mshr)
  - Įgūdžių kompetencija (mshr)
  - Įgūdžiai (mshr)
  - Pavadinimai (mshr)
  - Seniai dirbančiojo būsena (mshr)
  - Darbuotojas (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Programos teisių suteikimas Žmogiškųjų išteklių duomenims

Antrasis žingsnis yra užtikrinti, kad programai būtų suteiktos atitinkamos teisės į Žmogiškųjų išteklių duomenis, susiejant ją su Žmogiškųjų išteklių programos vartotoju. Programos vartotojui serverio iškvietimai per „Dataverse” virtualias lenteles atliekami „Dataverse” vartotojo (programos), kuris iškviečia veiksmą, tapatybės kontekste. Tada virtualiosios lentelės adapterio tarnyba peržiūrės susietą vartotoją Žmogiškųjų išteklių srityje ir vykdys užklausą to vartotojo kontekste. Tai reiškia, kad Žmogiškųjų išteklių srityje reikia sukurti vartotoją su priskirtais tinkamais vaidmenimis, kad būtų galima suteikti prieigą prie duomenų, reikalingų integravimo programai.

Žmogiškųjų išteklių vartotojui taip pat reikės priskirti tinkamas teises į Žmogiškųjų išteklių duomenis. **Įdarbinimo prašymo** („HcmRecruitingIntegrator”) vaidmuo galimas su teisėmis į pirminius objektus, būtinus integruojant su įdarbinimo duomenimis. Šį vaidmenį galima priskirti programos vartotojui puslapyje **Vartotojai**, kad būtų galima suteikti tinkamą prieigą prie duomenų. Daugiau informacijos apie Žmogiškųjų išteklių saugos vaidmenis rasite [Vaidmenimis pagrįsta sauga](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Naujo vartotojo su atitinkamomis teisėmis nustatymas

Norėdami nustatyti naują vartotoją su atitinkamomis, atlikite šiuos veiksmus:

  1. Atidarykite **Vartotojų** puslapį Žmogiškuosiuose ištekliuose ir pasirinkite **Naujas**.
  2. Įveskite naujo programos vartotojo **Vartotojo ID** ir **Vartotojo vardą**. Pavyzdžiui, galite įvesti „ĮdarbinimoIntegravimas”.

      > [!NOTE]
      > Jei programoje nėra „Microsoft Azure Active Directory” („Azure AD”) vartotojo paskyros ar el. pašto adreso, vartotojo el. pašto adreso ir tiekėjo laukuose galite nurodyti „ĮdarbinimoPrograma”.

  3. „FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis** veiksmą.
  4. Srityje **Priskirti vaidmenis vartotojui** pasirinkite **Įdarbinimo prašymas** ir **Gerai**.
  5. Įrašykite naujo vartotojo įrašą.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Žmogiškųjų išteklių vartotojo susiejimas su programa

Sukūrus vartotoją, turi būti sukurtas programos įrašas **„Azure Active Directory” programų** formoje, kad susietų programą su Žmogiškųjų išteklių vartotoju.

  1. Atidarykite **„Azure Active Directory” prašymų** formą ir pasirinkite **Naujas**.
  2. Lauke **Kliento ID** įveskite programos vartotojo, sukurto programai, kliento ID.
  3. **Pavadinimo** lauke įveskite integruojamosios programos pavadinimą.
  4. Lauke **Vartotojo ID** pasirinkite naują Žmogiškųjų išteklių vartotoją, sukurtą įdarbinimo integravimui.
  5. Įrašykite naują įrašą.

Tada programa turės prieigą prie Žmogiškųjų išteklių duomenų, apribotų tik iki duomenų, kurių reikia įdarbinimo prašymo integravimams.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kandidatų į darbo vietas įdarbinimas](hr-personnel-recruit.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Naudokite „Microsoft Dataverse“ žiniatinklio API](/powerapps/developer/data-platform/webapi/overview)<br>
[Kurti ir naujinti parinkčių rinkinius naudojant žiniatinklio API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
