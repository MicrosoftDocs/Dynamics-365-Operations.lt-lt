---
title: Debesies ir krašto skalės vienetai gamybai ir sandėlio valdymo darbo apkrovoms
description: Šioje temoje pateikiama informacija apie debesies ir krašto skalės vienetų gamybą ir sandėlio valdymo darbo apkrovas.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3a23ee452535423684c6d210a448ee768379fa08
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516840"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Debesies ir krašto skalės vienetai gamybai ir sandėlio valdymo darbo apkrovoms

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Debesies ir krašto skalės vienetai leidžia platinti parduotuvė aukšto ir sandėlio vykdymų darbo apkrovas tarp skirtingų aplinkų. Ši funkcija gali padėti pagerinti vykdymą, apsaugoti nuo paslaugų pertrūkių ir maksimizuoti veikimo laiką. Jį pateikia tolesni papildiniai:

- „Cloud Scale Unit“ papildinys „Dynamics 365 Supply Chain Management“
- „Edge Scale Unit“ papildinys „Dynamics 365 Supply Chain Management“

Bendrovės dirbančios su gamyba ir platinimu privalo galėti vykdyti pagrindinius verslo procesus septynias dienas, 24 valandas per savaitę be pertrūkių ir laipsniškai. Debesies ir krašto skalės vienetai leidžia įmonėms vykdyti pagrindinius misijos kritinius gamybos ir sandėlio procesus be pertrūkio, net jei jos susiduria su kartais pasireiškiančiomis tinklo ryšio ar vėlavimo problemomis.

## <a name="public-preview-information"></a>Viešosios peržiūros informacija

Peržiūra pateikia vieną aplinką, kuri veikia debesimi pagrįstame centre jūsų „Dynamics 365 Supply Chain Management“ aplinkoje ir vienoje aplinkoje, kuri veikia kaip debesies skalės vienetas.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Peržiūros prieinamumas

Peržiūra debesiui ir krašto skalės vienetams tampa įmanoma esantiems klientams „Supply Chain Management“2020 m. spalio mėn.

Norėdami prieiti prie spalio peržiūros leidimo 10.0.15/„Platform“ naujinimo 39 talpinimui jūsų [„Microsoft Dynamics Lifecycle Services“ (LCS)](https://lcs.dynamics.com/v2) aplinkoje, privalote būti peržiūros greitos prieigos programos dalimi (taip pat žinomos kaip PEAP) skirtos „Supply Chain Management“. Galite prisijungti prie PEAP jei jau esate platesnės programos nariu [„Dynamics Insider Program“](https://experience.dynamics.com/insider). Tik pasirinkite konkrečią programą pavadinimu „Finance & Operations: Preview early access program (PEAP)."

> [!IMPORTANT]
> Skalės vieneto pajėgumas „Supply Chain Management“ yra jums prieinamas tik, jei sutinkate su [„Cloud + Edge Preview“ skirtu „Finance and Operations“ sąlygomis](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Duomenų tvarkymas peržiūrai

Viešosios peržiūros metu, kai kurios valdymo paslaugos bus patalpintos tik Jungtinėse Amerikos Valstijose. Nepaisant to, kai funkcija tampa bendrai prieinama, šios valdymo paslaugos bus prieinamos visose geografinėse vietose palaikomose „Supply Chain Management“. Tai paveikia perdavimo ir talpinimo administravimo informaciją, kurią naudoja skalės vieneto vadovas, įskaitant:

- Jūsų nuomotojo pavadinimai ir ID
- Jūsų LCS projekto ID
- Administratoriaus el. pašto naudojamas prisijungimui
- Aplinkos ID centrui ir skalės vienetams
- Darbo apkrovos konfigūravimai
- Surinkti metriniai duomenys (tokie kaip vėlavimas ir srauto perdavimas), kurie yra rodomi žemėlapio analizės puslapyje

Duomenų perdavimas į ir laikymas JAV duomenų centruose bus pašalintas jums peržiūrint aplinkas, kai jos išjungtos.

### <a name="sign-up-for-the-preview"></a>Registravimasis peržiūros versijai gauti

Norėdami prisijungti prie debiesies ir krašto peržiūros „Supply Chain Management“, jūsų organizacija jau turi turėti galiojančią „Supply Chain Management“ debesies aplinką.

Skalės vieneto pajėgumai dabar yra rodomi viešojoje peržiūroje. Jums prisijungus, privalote naudoti vartotojo paskyrą konkrečiame nuomotojuje. Privalote taip pat būti prjekto savininku ar aplinkos administratoriumi LCS aktyviame „Dynamics 365 LCS“ projekte tame nuomotojuje.

Jums prisijungus peržiūrai, pasirinksite nuomotoją ir eisite per prisijungimo žingsnius. Kai tik „Microsoft“ galės priskirti peržiūros pajėgumą, nusiųsime jums el. laišką, kuriame bus suteikimo išsami informacija ir akcijos kodai dviem aplinkoms (centrui ir skalės vienetui) atitinkamam LCS projektui. Tuomet galėsite talpinti dvi aplinkas kaip tier-2 smėlio dėžės aplinkas. Šios aplinkos glaios 60 dienų nuo sukūrimo dienos su akcijos kodais. Turėtumėte nenaudoti abiejų aplinkų, kol žingsnis, aprašytas kitame skyriuje, bus užbaigtas.

Jums patvirtinus su „Microsoft“, kad abi aplinkos patalpintos naudojant akcijos kodus, viena aplinka bus sukonfigūruota dirbti kaip centras, o kita bus sukonfigūruota veikti kaip skalės vienetas. Tuomet galite konfigūruoti skalės vienetus ir talpinti pasirinktą sandėlio valdymą ir gamybos darbo apkrovas naudodami [„Scale Unit Manager“ portalą](https://aka.ms/SCMSUM).

Peržiūros alpinkos bus automatiškai panaikintos po 60 dienų. Nepaisant to, jos gali būti panaikintos anksčiau, jei pasirodys, kad nebėra naudojamos. Jums iš anksto peržiūrėjus panaikintas aplinkas, galite prisijungti ir laukti naujos peržiūros talpinimo.

Norėdami prisijungti peržiūrai, eikite į [„Scale Unit Manager“ portalą](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Apribojimai taikomi peržiūros laikotarpio metu

> [!IMPORTANT]
> Pradiniame etape peržiūros programa šiai funkcijai, „Microsoft“ palaiko tik centrus, kurie gali turėti debesies skalės vienetus, ne centrus turinčius krašto skalės vienetus. Krašto skalės vienetai yra įdiegti į patalpas ir tikėtina, kad jie taps prieinami ateinančiame programos etape.

Kadangi debesies ir krašto skalės vienetai yra peržiūros funkcija, su jais susijusios paslaugos yra šiuo metu prieinamos apribotose šalyse ir regionuose. Įjungus debesies ir krašto skalės vienetus, patvirtinate, kad suprantate, jog kai kurie duomenys yra susieti su konfigūravimu ir debesies ir krašto skalės vienetų apdorojimu, kurie gali būti laikomi duomenų centre esančiame JAV. Įjungę debesies ir krašto skalės vienetus, taip pat sutinkate su [„Cloud + Edge Previe“ skirtos „Finance and Operations“ sąlygomis](https://Aka.ms/SCMCnETerms). Norėdami sužinoti daugiau apie debesies ir krašto skalės vienetus, žr. [dokumentus](https://aka.ms/scmcne).

Jūsų privatumas „Microsoft“ yra svarbus. Norėdami sužinoti, perskaitykite mūsų [Pareiškimą dėl privatumo](https://aka.ms/privacy).

> [!IMPORTANT]
> Kai kurios verslo funkcijos nėra visiškai palaikomos viešoje peržiūroje, kai darbo apkrovos naudojamos skalės vienetuose. Dėl daugiau informacijos apie funkcijų darbo apkrovas, žr. tolesnius skyrius šioje temoje.

## <a name="scale-units-and-dedicated-workloads"></a>Skalės vienetai ir paskirtos darbo apkrovos

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="„Dynamics 365“ su skalės vienetais":::

Skalės vienetai išplečia jūsų centrinę „Supply Chain Management“ centro aplinką įtraukdami paskirtą apdorojimo pajėgumą. Skalės vienetai gali vykti debesyje. Kitu atveju, jie gali vykti krašte jūsų vietinėse patalpose. Skalės vienetai gali laikinai atsijungti nuo centro aplinkos. Jiems prisijungus, skalės vienetai gauna visą informaciją būtiną vykdyti paskirtą paskirtų darbo apkrovų tvarkymą.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Skalės vieneto parinktys viešojoje peržiūroje":::

Viešai peržiūrai galite konfigūruoti centro aplinką su pasirinktomis darbo apkrovomis debesies skalės vienete naudodami „Scale Unit Manager“ portalą. Iš anksto perževelgti dalyviai, turintys prieigą prie „Local Business Data (LBD)“ patalpų aplinkoje taip pat gali konfigūruoti LBD aplinką kaip krašto skalės vienetą.

Darbo apkrova yra nustatytas verslo funkcijų rinkinys, kuris gali veikti su faktoriais ir būti paskirtas skalės vienetui. Šiuo metu, peržiūros funkcijų darbo apkrovų tipai:

- Gamybos vykdymas
- Sandėlio valdymas

Galite paskirti vieną darbo apkrovos tipą vienam skalės vienetui. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Paskirtos gamybos vykdymo darbo apkrovos pajėgumai skalės vienete

Dėl gamybos vykdymo, debesiesi ir krašto skalės pajėgumai pristato tolesnius pajėgumus, net kai krašto vienetai nėra sujungti su debesiu:

- Mašinos operatoriai ir parduotuvės aukšto vadovai gali prieiti prie oepracijos gamybos plano.
- Mašinos operatiria gali turėti atnaujintą planą diskretiškam vykdymui ir proceso gamybos darbus.
- Parduotuvės aukšto vadovas gali keisti operacijos planą.
- Darbuotojai gali prieiti prie laiko ir lankymosi su laikrodžiu ir be jo veikiančiame krašte siekiant pataisyti darbuotojo užmokesčio skaičiuoklę.

Dėl daugiau informacijos, žr. [gamybos skalės vieneto darbo apkrovos išsami informacija](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Paskirtas sandėlio valdymo darbo apkrovos pajėgumai skalės vienete

Dėl sandėlio valdymo, debesiesi ir krašto skalės pajėgumai pristato tolesnius pajėgumus, net kai krašto vienetai nėra sujungti su debesiu:

- Pasirinktos bangos tvarkymo metodai yra įjungti prekybos užsakymams ir paklausos papildymui.
- Sandėlio darbuotojai gali vykdyti prekybos ir paklausos papildyma sandėlio darbui naudodami sandėlio programą.
- Sandėlio darbuotojai gali teirautis apie turimą inventorių su sandėlio programa.
- Sandėlio darbuotojai gali kurti ir vykdyti inventoriiaus judėjimus su sandėlio programa.
- Sandėlio darbuotojai gali registruoti įsigijimo užsakymus ir atidėti su sandėlio programa.

Dėl daugiau informacijos, žr. [sandėlio skalės vieneto darbo apkrovos išsami informacija](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Įvesties skalės vienetai „Supply Chain Management“ aplinkai

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Talpinti debesies ir krašto skalės vienetų peržiūrą

Tolesnis paveikslėlis rodo prisijungimo ir srauto suteikimo viešajai peržiūrai debiesies skalės vienetams.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Peržiūrėti prisijungimo žingsnius":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Pasirinkti savo LCS projekto nuomotoją ir išsamų peržiūros procesą

Viešojoje peržiūroje, [„Scale Unit Manager“ portalą](https://aka.ms/SCMSUM) rodo nuomotojų sąrašą, kurio dalis yra jūsų paskyrą ir kai jūsų savininkas ir aplinkos administratorius LCS projekte.

Jei nuomotojas, kurio ieškote nėra sąraše, eikite į [LCS](https://lcs.dynamics.com/v2) ir įsitikinkite, kad esate savo aplinkos administratorius ar LCS projekto savininkas nuomotojui. Atkreipkite dėmesį, kad „Azure Active Directory“ („Azure AD“) paskyros iš pasirinkto nuomotojo yra leidžiamos siekiant užbaigti prisijungimo patirtį.

> [!NOTE]
> Jums pritaikius pakeitimus LCS, gali užtrukti iki 30 minučių, kol nuomotojų sąraše bus padaryti pakeitimai.

Kiekvienam nuomotojui sąrašas rodo prisijungimo būseną.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Prisijungimo parinktis nuomotojui":::

Pasirinkite **Paspauskite čia, kad prisijungtumėte** nuorodą tam, kad prijungtumėte savo LCS nuomotoją ir jis dalyvautų peržiūroje. Turite priimti nuostatas. Turite taip pat pateikti verslo el. pašto adresą, į kurį „Microsoft“ gali siųsti pranešimus susijusius su peržiūros prisijungimo procesu.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Prisijungimo pateikimas nuomotojui":::

„Microsoft“ peržiūros jūsų prašymą ir informuos jus apie kitus žingsnius nusiųsdama el. laišką adresu, kurį pateikėte prisijungimo formoje.

Jums suteikus prieigos teisę prie peržiūros programos, gausite du akcijos kodus savo LCS projektui. Galite dabar naudoti šiuos akcijos kodus, kad talpintumėte dvi aplinkas LCS. Aplinkos turi naudoti PEAP versiją 10.0.15 ar vėlesnę. Jums baigus akcijos kodų taikymą, praneškite „Microsoft“ (kaip nurodyta), kad galime užbaigti aplinkas peržiūros funkcijoms. „Microsoft“ jus informuos, kai šis konfigūravimo žingsnis bus atliktas.

Dabar galite pradėti konfigūruoti skalės vienetus ir darbo apkrovas jūsų peržiūros aplinkoje.

> [!IMPORTANT]
> Jums konfigūruojant debesies skalės vienetus, galite [atlikti visus būtinus žingsnius „Scale Unit Manager“ portale](#scale-unit-manager-portal).
<!-- >
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Tvarkykite debesies skalės vienetus ir darbo apkrovas naudodami „Scale Unit Manager“ portalą

Eikite į [„Scale Unit Manager“ portalą](https://aka.ms/SCMSUM) ir prisijunkite naudodami savo nuomotojo paskyrą. Puslapyje **Konfigūruoti skalės vienetus** galite įtraukti centro aplinką, jei jos dar nėra. Galite tada rinktis centrą, kurį norite konfigūruoti su skalės vienetais ir darbo apkrovas.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Skalės vienetas ir darbo apkrovos valdymo patirtis":::

Norėdami įtraukti vienetą ar keletą skalės vienetų esančių jūsų topologijoje, rinkitės **Įtraukti skalės vienetus**. Peržiūroje, turėtumėte matyti debesies skalės vienetą, kurį patalpinote iš vieno akcijos kodo, gauto kaip dalį peržiūros programos.

<!-- > [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Skirtuke **Nustatytos darbo apkrovos** naudokite **Sukurti darbo apkrovą** mygtuką, kad įtrauktumėte sandėli ovaldymą ar gamybos vykdymo darbo apkrovą į vieną iš jūsų skalės vienetų. Kiekvienai darbo apkrovai turite nurodyti procesų kontekstą, kurį turės darbo apkrova. Sandėlio valdymo darbo apkrovoms, kontekstas turi konkretų sandėlį konkrečioje vietoje ir juridinį asmenį. Gamybos vykdymo apkrovoms, kontekstas turi konkretų sandėlį konkrečiame saite juridiniame asmenyje.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Darbo apkrovos sukūrimas":::

> [!IMPORTANT]
> „Scale Unit Manager“ portalas peržiūroje neleidžia jums pašalinti darbo apkrovų iš skalės vienetų ar nepriskirti skalės vieneto iš centro po jo priskyrimo. Jei panaikinate priskyrimą, susisiekite su savo kontaktiniu asmeniu programos valdymo peržiūrai.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]