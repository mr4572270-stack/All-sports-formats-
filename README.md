Act as an Expert Full-Stack Web & Mobile App Developer. Build a complete, production-ready, single-file responsive Mobile Web App (HTML5, CSS3, and Vanilla JavaScript) named "SPORTS ALL FORMAT" with the subtitle "मेरा सपना - मेरा विद्यालय | राजस्थान विद्यालयी खेलकूद संपूर्ण प्रपत्र एवं स्कोर शीट जनरेटर".

### 1. CORE REQUIREMENTS & UI/UX:
- Language: Entire UI, labels, forms, and printable formats MUST be in Hindi (Devanagari script) using Google Font 'Noto Sans Devanagari'.
- Mobile-First Design: Sticky top app bar, smooth horizontal scrollable navigation tabs for 8 modules, clean card-based input forms, and touch-friendly buttons.
- LocalStorage Persistence: Automatically save all Master Setup inputs and the Master Player List in browser `localStorage` so the user never loses data on refresh. Provide a "डेटा रीसेट करें" (Reset Data) button as well.
- Print / PDF Engine: Every format tab must have a "🖨️ A4 प्रिंट / PDF सेव करें" button (`window.print()`). Use strict `@media print` CSS rules so that when printing or saving as PDF, all app headers, navigation tabs, input cards, and buttons are completely hidden (`.no-print`), and ONLY the official A4 document (`.print-area`) is printed cleanly with sharp black borders (`1px solid #000`) and proper signature footers.

### 2. PRE-LOADED DEFAULT MASTER DATA (Fully Editable by User):
- प्रतियोगिता / शिविर का नाम: "70वीं जिला स्तरीय विद्यालयी खेलकूद प्रतियोगिता"
- मूल / आयोजक विद्यालय का नाम: "राजकीय उच्च माध्यमिक विद्यालय समलेटी (महवा, दौसा)"
- प्रतियोगिता / शिविर स्थल: "रा.उ.मा.वि. समलेटी / बड़ागांव (झुंझुनू)"
- खेल का नाम (Dropdown): कबड्डी (Kabaddi), खो-खो (Kho-Kho), सॉफ्टबॉल (Softball), वॉलीबॉल (Volleyball), एथलेटिक्स (Athletics), क्रिकेट (Cricket).
- आयु वर्ग एवं श्रेणी (Dropdown): 17 वर्ष (छात्र), 17 वर्ष (छात्रा), 19 वर्ष (छात्र), 19 वर्ष (छात्रा), 14 वर्ष (छात्र/छात्रा).
- दिनांक / अवधि: "23/10/2026 से 26/10/2026"
- दल प्रभारी / शारीरिक शिक्षक: "श्री रामकेश मीना (शारीरिक शिक्षक)"
- संस्था प्रधान / मुख्य संयोजक: "श्री विजय सिंह मीना (प्रधानाचार्य)"
- शिविर / आवास व्यवस्था प्रभारी: "श्री कमलेश कुमार सैन / श्री हरफूल सिंह गुर्जर"

### 3. THE 8 INTERCONNECTED MODULES (TABS) TO BUILD:

#### TAB 1: ⚙️ मास्टर सेटअप एवं खिलाड़ी सूची (Master Setup & Player Database)
- Form inputs for all the default master fields above. Changing any field here must dynamically update the headers/footers of all other 7 tabs in real-time.
- Dynamic Master Player List Builder: Input fields to add players (खिलाड़ी का नाम, पिता का नाम, जन्मतिथि, कक्षा, एस.आर. नं. / SR No.) with an "➕ खिलाड़ी जोड़ें" button and delete ("✖") buttons for each row. Pre-load 5 sample players so the app looks ready immediately.

#### TAB 2: 📑 प्रपत्र - 'क' (समेकित दल पात्रता एवं पंजीकरण सूची)
- Printable A4 official format for "प्रपत्र - 'क' (Eligibility Proforma)".
- Automatically populate the table rows from the Master Player List (क्र.सं., खिलाड़ी का नाम, पिता का नाम, जन्मतिथि, वर्तमान कक्षा, एस.आर. संख्या, प्रवेश दिनांक, खिलाड़ी के हस्ताक्षर) plus empty rows up to 12.
- Include the official verification paragraph at the bottom and signature blocks for शारीरिक शिक्षक / दल प्रभारी and संस्था प्रधान (मय पद मुहर).

#### TAB 3: 🪪 प्रपत्र - 'ख' (व्यक्तिगत खिलाड़ी पात्रता एवं परिचय पत्र)
- Dropdown to select any player from the Master Player List (auto-filling their Name, Father's Name, DOB, Class, SR No.) PLUS editable inputs for Mother's Name, DOB in words, Admission Date, Previous Class Passed, Physical Identification Mark (शारीरिक पहचान चिन्ह), and Address/Mobile.
- Printable A4 format featuring a right-aligned passport photo box ("खिलाड़ी का नवीनतम पासपोर्ट साइज फोटो - संस्था प्रधान द्वारा प्रमाणित"), a structured 9-point details table, official certification text, and 3 signature blocks (खिलाड़ी, शारीरिक शिक्षक, संस्था प्रधान).

#### TAB 4: 🩺 प्रपत्र - 'ग' (अभिभावक सहमति, अध्ययनरत एवं चिकित्सा प्रमाण-पत्र)
- Synced with the selected player in Tab 3.
- Printable A4 format divided into 3 bordered sections on a single page:
  - भाग 1: अभिभावक का सहमति-पत्र (Parent Consent for tournament/camp & travel).
  - भाग 2: चिकित्सा अधिकारी द्वारा स्वास्थ्य प्रमाण-पत्र (Medical Fitness certification with Doctor seal/sign area).
  - भाग 3: संस्था प्रधान द्वारा अध्ययनरत एवं जन्मतिथि प्रमाणीकरण.

#### TAB 5: ⛺ शिविर एवं आवास व्यवस्था (Camp & Accommodation Format)
- Editable inputs for शिविर का प्रकार, आवास भवन का नाम, आवंटित कक्ष संख्या (Room Nos.).
- Printable A4 chart showing Camp Metadata and a daily attendance/accommodation table auto-populated with the Master Player List (क्र.सं., खिलाड़ी का नाम, पिता का नाम, आगमन समय, कक्ष सं., सुबह उपस्थिति, सायं उपस्थिति, प्रस्थान व हस्ताक्षर).

#### TAB 6: 💰 TA/DA बिल एवं भुगतान पंजिका (Auto-Calculating TA/DA & Acquittance Roll)
- Inputs for यात्रा मार्ग (Route), यात्रा का साधन (Mode), प्रति खिलाड़ी आने-जाने का कुल किराया (TA ₹), कुल दिवस (Days), दैनिक भत्ता दर (DA प्रति दिन ₹).
- Auto-calculate individual TA, individual DA (Days × Rate), individual Total, and Grand Totals (महायोग) for the entire team.
- Printable A4 Acquittance Roll listing all players from the Master List with their calculated amounts and a wide column for "प्राप्तकर्ता खिलाड़ी के हस्ताक्षर".

#### TAB 7: 📋 खेल स्कोर शीट (Dynamic Game-Specific Official Score Sheet)
- Inputs for टीम A का नाम, टीम B का नाम, मैच संख्या व राउंड, टॉस विजेता व निर्णय.
- Dynamic Layout Engine based on the selected Game in Master Setup:
  - If "कबड्डी" is selected: Render a special Kabaddi Running Score grid (1 to 25 points), Lona, Super Tackle, Time-out boxes, and Raider/Tackle columns.
  - If "खो-खो" is selected: Render Inning 1 & 2 Chaser/Defender points summary and Running Time / Out-by columns.
  - If "सॉफ्टबॉल" is selected: Render a 7-Innings Run Box Score table and Batting Order / Runs / Hits / Outs / Errors columns.
  - Include Half-Time Score, Final Score, Winner Name, and signatures for Captains, Scorer, Referee/Umpire, and Chief Convener.

#### TAB 8: 📄 कार्यमुक्ति एवं उपस्थिति प्रमाण-पत्र (Relieving & Attendance Certificate)
- Inputs for अधिकारी/शिक्षक का नाम व पद, पदस्थापन विद्यालय, ड्यूटी की भूमिका (निर्णायक / दल प्रभारी / आयोजन अधिकारी), और पत्रांक संख्या.
- Printable formal office certificate with header, reference number, date, justified Hindi body text certifying duty completion and relieving, and signature blocks.

### 4. OUTPUT FORMAT:
Provide the complete, unbroken, self-contained code inside a single `index.html` block without skipping or abbreviating any section.
