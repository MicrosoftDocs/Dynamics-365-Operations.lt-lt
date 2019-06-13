<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="lt-LT">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mažmeninės prekybos operacijų vientisumo tikrintuvas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos „Microsoft Dynamics 365 for Retail“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mažmeninės prekybos operacijų vientisumo tikrintuvas</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos, veikiančios „Microsoft Dynamics 365 for Finance and Operations“ 8.1.3 versijoje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Vientisumo tikrintuvas identifikuoja ir atskiria nesuderinamas operacijas prieš jas paimant į išrašų registravimo procesą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Išrašą registruojant sprendime „Microsoft Dynamics 365 for Retail“, užregistruoti gali nepavykti dėl mažmeninės prekybos operacijų lentelėse esančių nesuderinamų duomenų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Duomenų problema galėjo įvykti dėl nenumatytų problemų elektroninio kasos aparato (EKA) programoje arba dėl netinkamo operacijų importavimo iš trečiųjų šalių EKA sistemų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šio nesuderinamumo atvejų pavyzdžiai:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eilučių skaičius, nurodytas antraštės lentelėje, nesutampa su operacijų lentelės eilučių skaičiumi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kai nesuderinamos operacijos paimamos į išrašo registravimo procesą, sukuriamos nesuderinamos pardavimo SF ir mokėjimo žurnalai, todėl nepavyksta visas išrašų registravimo procesas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Norint atkurti išrašus iš tokios būsenos reikia pataisyti nemažai duomenų įvairiose operacijų lentelėse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mažmeninės prekybos operacijų vientisumo tikrintuvas apsaugo nuo tokių problemų.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šioje diagramoje parodytas registravimo procesas naudojant operacijų vientisumo tikrintuvą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Paketinis vykdymas <bpt id="p1">**</bpt>Tikrinti parduotuvės operacijas<ept id="p1">**</ept> tikrina mažmeninės prekybos operacijų lentelių vientisumą tolesniais aspektais.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kliento kodas<ept id="p1">**</ept> – tikrinama, ar kliento kodas, nurodytas mažmeninės prekybos operacijų lentelėse, yra HQ kliento bendruosiuose duomenyse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Eilučių skaičius<ept id="p1">**</ept> – tikrinama, ar eilučių skaičius, nurodytas operacijos antraštės lentelėje, sutampa su pardavimo operacijų lentelių eilučių skaičiumi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Į kainą įtrauktas mokestis<ept id="p1">**</ept> – tikrinama, ar parametras <bpt id="p2">**</bpt>Į kainą įtrauktas mokestis<ept id="p2">**</ept> yra nuoseklus visose operacijos eilutėse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Bendra suma<ept id="p1">**</ept> – tikrinama, ar antraštėje nurodyta bendra suma yra eilutėse nurodytų grynųjų sumų ir mokesčio sumos suma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Grynoji suma<ept id="p1">**</ept> – tikrinama, ar antraštėje nurodyta grynoji suma yra eilutėse nurodytų grynųjų sumų suma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Nepriemoka / permoka<ept id="p1">**</ept> – tikrinama, ar antraštėje nurodytos bendros sumos ir mokėjimo sumos skirtumas neviršija didžiausios nepriemokos / permokos konfigūracijos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Nuolaidos suma<ept id="p1">**</ept> – tikrinama, ar nuolaidos suma nuolaidos lentelėse ir nuolaidos suma mažmeninės prekybos operacijų eilučių lentelėse yra nuoseklios, bei ar antraštėje nurodyta nuolaidos suma yra eilutėse nurodytų nuolaidos sumų suma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Eilutės nuolaida<ept id="p1">**</ept> – tikrinama, ar operacijos eilutėje nurodyta eilutės nuolaida yra visų nuolaidų lentelėje, atitinkančioje operacijos eilutę, esančių eilučių suma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Dovanų kortelės prekė<ept id="p1">**</ept> – „Retail“ dovanų kortelių prekių grąžinimo nepalaiko.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tačiau dovanų kortelės likutį galima išgryninti. Bet kokiai dovanų kortelės prekei, kuri yra apdorojama ne kaip išgryninimo eilutė, o kaip grąžinimo eilutė, išrašo registravimo proceso vykdyti nepavyksta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dovanų kortelių prekių tikrinimo procesas padeda užtikrinti, kad mažmeninės prekybos operacijų lentelėse būtų tik tos grąžinamos dovanų kortelių eilučių prekės, kurios yra dovanų kortelių išgryninimo eilutės.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Neigiama kaina<ept id="p1">**</ept> – tikrinama, ar nėra neigiamos kainos operacijų eilučių.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Prekė ir variantas<ept id="p1">**</ept> – tikrinama, ar operacijų eilutėse nurodytos prekės ir variantai egzistuoja pagrindiniame prekių ir variantų faile.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Vientisumo tikrintuvo nustatymas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Sukonfigūruokite, kad paketinis vykdymas Tikrinti parduotuvės operacijas būtų paleidžiamas periodiškai, įėję į <bpt id="p1">**</bpt>Mažmeninė prekyba <ph id="ph1">\&gt;</ph> Mažmeninės prekybos IT <ph id="ph2">\&gt;</ph> EKA registravimas<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paketinė užduotis gali būtu suplanuota pagal parduotuvės organizacijos hierarchiją, panašiai kaip nustatyti procesai Skaičiuoti išrašus pakete ir Registruoti išrašus pakete.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų paleistas keletą kartų per dieną, ir suplanuoti taip, kad jis būtų vykdomas kiekvienos P užduoties pabaigoje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tikrinimo proceso rezultatai</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paketinio vykdymo tikrinimo rezultatai yra pažymimi atitinkamoje mažmeninės prekybos operacijoje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mažmeninės prekybos operacijos įrašo lauko <bpt id="p1">**</bpt>Tikrinimo būsena<ept id="p1">**</ept> reikšmė pateikiama arba <bpt id="p2">**</bpt>Sėkmingai<ept id="p2">**</ept>, arba <bpt id="p3">**</bpt>Klaida<ept id="p3">**</ept>, o lauke <bpt id="p4">**</bpt>Paskutinio tikrinimo laikas<ept id="p4">**</ept> rodoma paskutinio tikrinimo data.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Norėdami peržiūrėti išsamesnį klaidos tekstą tikrinimui nepavykus, pasirinkite atitinkamą mažmeninės prekybos parduotuvės operacijos įrašą ir spustelėkite mygtuką <bpt id="p1">**</bpt>Tikrinimo klaidos<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operacijos, kurias tikrinant rasta klaidų ir kurios dar nebuvo patikrintos, į išrašus įtrauktos nebus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proceso Skaičiuoti išrašą metu vartotojams bus pranešta, jei bus operacijų, kurios galėjo būti įtrauktos į išrašą, tačiau nebuvo.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Radus tikrinimo klaidų, vienintelis būdas jas ištaisyti yra kreiptis į „Microsoft“ pagalbos tarnybą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Būsimame leidime bus įtraukta galimybė vartotojui pataisyti klaidingus įrašus vartotojo sąsajoje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Be to, pradės veikti registravimo ir audito funkcijos, kad būtų galima sekti pakeitimų retrospektyvą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Į būsimas versijas bus įtraukta papildomų tikrinimo taisyklių, kurios palaikys daugiau scenarijų.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>