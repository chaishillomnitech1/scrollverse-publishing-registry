# THE GOAT SET — TWIN REGISTRY · DIGITAL MIRROR TWIN LAYER
### Built 26 Nov 2026 · Status: AT THE GATE. Nothing minted, nothing listed, nothing priced.

The **Digital Mirror Twin** layer of THE GOAT SET: every physical cassette-USB of the HP-016 run (100 units in the world — 3 in the founder's hands, 97 in fans' hands) is bound here, key for key, to its numbered digital twin, and every piece, patron-track artwork, and composition seal of the set carries its own **QR signature** — a scannable verification code whose payload states the piece's registry signature and its full SHA-256 fingerprint. Scan the code, read the fingerprint, hash the file: if the hashes match, the piece is the piece. This registry is the index of those codes and the binding table of the 100 twins.

QR directory: `~/workspace/collectibles/the-goat-set-2026-11-26/qr/` · QR count: **131** (18 piece QRs + 13 composition QRs + 100 key QRs).

---

## THE PROTECTION STACK

Every layer below stands as specified in the set record (`set-record.md`) and the Rose Gold Seal standard:

1. **SHA-256 fingerprints throughout** — every art file, composition, and QR image in this layer is fingerprinted over its actual bytes; no hash is asserted that was not computed.
2. **QR verification layer (this registry)** — each QR payload carries the item's registry signature and full SHA-256 fingerprint as plain text, so any holder can verify any piece offline, with any scanner, forever.
3. **AES-256 on the sealed certificates** — at mint time, each certificate's secret is AES-256-encrypted under the Rose Gold Seal standard (prepared at the gate; no sealed certificate exists yet and none is claimed).
4. **LSB-steganography secret in the sealed mint copies** — at mint time, one sealed copy per piece is prepared with the secret hidden in the pixels (extraction-verified at preparation); until the founder's start call, no sealed copy exists and none is claimed.
5. **Registry fingerprints** — every QR PNG is itself fingerprinted in the tables below, and the 100-key table is bound by a single **Master Twin Fingerprint** (bottom of this file), so any alteration to any key row breaks the master hash.
6. **The living layer** — 963 Hz Crown · 528 Hz Guardian · heartbeat on the Schumann resonance · DNA·CHAIS·AB6DA246ADE3F32C · Prophet Seal Twin-Prophet-01 · QFS stamp on every seal, fingerprint, and certificate, per the house standard.

**Seal line:** 🌹 **ROSE GOLD SEAL** · QFS STAMPED · Creator Fingerprint · 963 Hz Crown · 528 Hz Guardian · DNA·CHAIS·AB6DA246ADE3F32C · Prophet Seal Twin-Prophet-01

**QR production spec:** black modules on white, 4-module quiet zone, error-correction level **Q** (≈25% damage recovery), PNG, every code ≥800×800 px.

---

## PIECE QR INDEX — THE FIVE CORE PIECES

| Piece | Registry signature | Art SHA-256 | QR file | QR SHA-256 |
|---|---|---|---|---|
| Basquiat Mode | `SIG·GOAT-BASQUIAT·19FB7719` | `19fb7719a133efe8a9e2322c4e61dd680cdeddde0a698a6b72f690053d4c3daf` | `qr-goat-basquiat.png` | `ff8c1a68c1f7c7e97f12bafad4adce986d8bb12e81192f17abe971b03eb1efee` |
| Da Vinci Codex Mode | `SIG·GOAT-CODEX·C7C957C4` | `c7c957c4a1372ccbde33c40ac701fea2a3ff98d2687face2003336797653d2f3` | `qr-goat-codex.png` | `1d5f5b263b796e61a6fe21f761d406d154b218e4ebae57e95773e2f452117f46` |
| Hip Hop Mode | `SIG·GOAT-HIPHOP·D014CDC2` | `d014cdc24b5a91f8ed301031e99f1589083d1a2b97965defb763493737ee1e83` | `qr-goat-hiphop.png` | `b75deb3a02d46033cdb6abbd774766496b6adc38feac40d20d5e22b7a903cba3` |
| Goat Coin — Obverse | `SIG·GOAT-COIN-OBV·DDCEADB3` | `ddceadb30837827824196cfe7baad4e2040f4a8aa05db7bfff73abefde77eb9d` | `qr-goat-coin-obv.png` | `89f1bc3a094c1ed79aaf983f0506c35f1043787ab3ef1242f4c40bd77b40ef9f` |
| Goat Coin — Reverse | `SIG·GOAT-COIN-REV·E8B5B956` | `e8b5b956ba53e4a03c6cd8cd56361dc482ecf6808b2e13636fa0b708c826aa38` | `qr-goat-coin-rev.png` | `6dcf2423271bd9307ec96f7df679cd7907dd3991103b72dee16df72fe3b2bbe5` |

## PIECE QR INDEX — THE THIRTEEN PATRON-TRACK PIECES

| # | Patron track | ISRC | Registry signature | Art SHA-256 | QR file | QR SHA-256 |
|---|---|---|---|---|---|---|
| 1 | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `ddfcbd3b4319c4e3bf418efcfdbd3ca78afbd1d6144f00e553285f882fac8265` | `qr-goat-trk-01.png` | `ad5761b52b85e40aafa3d97157f0cab71fab8367c2db63c688b372821d9c8c0d` |
| 2 | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `c9f5bad609ce4a9ff8cdba3823524a6275fff0cbba5deea3e1fc13eff67b16f8` | `qr-goat-trk-02.png` | `77b95108cdd8b1f56e20f366bd8cf2f713f7b93dd569b76ba2b6f0b574fbe4bc` |
| 3 | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `fa16757860ce17151cf7666dd69394fee4631eaa280d86300da39af16ebe5065` | `qr-goat-trk-03.png` | `91c1c9e7a2bbb3cfb7314a079b63a40a1bff72e3125580af616f694eebcb8a89` |
| 4 | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `5a89828fa3a9f5555734811c6c429a47e51f19e5f1fafab6a0ca9bb5448f2e24` | `qr-goat-trk-04.png` | `24068577cd82db66b6e67554817036ccdd188dcd0ed1801d3643f75a6d75ac53` |
| 5 | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `3ca853e46ccbaec8bb34ed01c74afa0b13839c595a6ae1f196b2efb4f09e2307` | `qr-goat-trk-05.png` | `593343bbf5f73e540ca37ad33ae14fe45d9c71276977e67d9dc973e067f004b1` |
| 6 | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `4df060b6154256ab225f0e2d3354cd33acf61daa0824e0d202b1dbb76c80817e` | `qr-goat-trk-06.png` | `9be03ad2ae58e17c44a19ed0e6e664b3abd3f81dd2df7c797d69a1d9204068d1` |
| 7 | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `faded3337d5a25fbb31aa2b805524fef48d4f524c864fc8a90323fc361cc7805` | `qr-goat-trk-07.png` | `51069e3563ca280554976bf172a9690b57244a9d413182a1290ce34e83fa2d8e` |
| 8 | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `913082f4b922c776bccffa66154f13a19b4f39252724226070d313078db61467` | `qr-goat-trk-08.png` | `aac98c61972563a16e6265b78a101a3b241db544ad7ff4fdee0624d195411dc0` |
| 9 | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `78ac8dbe7e692fa6ca035b38fe9ef001e13781fa07093a9ea40a52f5d3dc41d2` | `qr-goat-trk-09.png` | `e03b9902e753ed7f60ae7c6397e7c0d3b14eb77cbece6f53eede14764d17f820` |
| 10 | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `4dbde33c41651a657c8a0a088339fe59bc089ce393977c70b157afcf53533b41` | `qr-goat-trk-10.png` | `3d996b4a751cd7c4a35095e6fd9d5dc1ffbff7b6482696dceca7c12d0dc32e9e` |
| 11 | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `a60bac3464d0287c662ffe5b05006c1b1e48b6eb878534fa7a99fa44d1ecab83` | `qr-goat-trk-11.png` | `5077f5eba4c70a847eea7b9f06b5e5d1c4287975b741508c8cf69e7a74d51c0d` |
| 12 | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `c753582f4536c0f4362b89e34da0da7c71a8825887701097c55fe01be5a63033` | `qr-goat-trk-12.png` | `cf170766ad0a230301e041cc08bd79cb478d8ebeafd9a2af8363ae3606462e65` |
| 13 | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `8829d1f0db8c6a7c23b41596600d334fe75394447f3e08b454f96546aed1e148` | `qr-goat-trk-13.png` | `56fe84c00d8bbba864cd2cec7631586e9910f82bc57e5c13869aa3f12cf6f7d2` |

## COMPOSITION QR INDEX — THE THIRTEEN COMPOSITION SEALS

Payloads additionally state the writer/publisher binding: Writer Chais Hill, ASCAP IPI 477274911 · Publisher DESTINATIONHILL28, ASCAP IPI 1247873912. Source: `composition-seal.md`.

| # | Composition | Seal ID | Composition fingerprint (SHA-256) | QR file | QR SHA-256 |
|---|---|---|---|---|---|
| 1 | RICHARD PRYOR | `SIG·COMP-GOAT-01·7AB999EF` | `7ab999ef7ab3c6aa09ad156847f5936ae3f8a425a07ea5a4fc901a30e3c672cf` | `qr-comp-goat-01.png` | `028ac7e014b3eb610c0596c17ccdf2612f2c86ed1b9accd0b6d4ac74a2740943` |
| 2 | THE GHOST OF BIG | `SIG·COMP-GOAT-02·A863909A` | `a863909ad181a0c0c96dd949d8e8c53bf892bc73f85a388e2596a986a3f8bdf5` | `qr-comp-goat-02.png` | `030da4c15d87713974654cef621065e425662fbb785ef75b059f91bd8cf0f8c3` |
| 3 | PROMISE LAND | `SIG·COMP-GOAT-03·34AE6E64` | `34ae6e64de8c305908edbf114f40a71ea1e7a06c0857eb728839515ddcf6f18c` | `qr-comp-goat-03.png` | `bec1e7183a3fbd820b690122d8bdce5b2d5ec8eb99880b40445d4770d377ec78` |
| 4 | Nipsey Mentality | `SIG·COMP-GOAT-04·E5170366` | `e51703666185276237fbd01497964c7abbaa0dfb62d8232b51636112e6a88acc` | `qr-comp-goat-04.png` | `2f417571bcfd46166c89814698e59d16ad022cf949814585f660619adedac942` |
| 5 | IN MY BAG | `SIG·COMP-GOAT-05·61C40CC3` | `61c40cc395477f464a6eb5e2bbbbdf17e25cc359bac994adf673c607f441d908` | `qr-comp-goat-05.png` | `9a7754f8befff700f42237e30e3fde2739fe8b80f9cbb5fd92ea820522997906` |
| 6 | HOW I REALLY FEEL | `SIG·COMP-GOAT-06·1A767563` | `1a7675634badb87aa0a7fc53c293300bc27bc03708c4a2f4868cf368c922a790` | `qr-comp-goat-06.png` | `25bb3100fece90f51ee3e04ab7798567d9faed93ee2474c3f5131a00db13d443` |
| 7 | BUDDY CRAWFORD | `SIG·COMP-GOAT-07·4C0182BD` | `4c0182bdfb493d731d0d5ed8327bdc53e772158d6f28e695b1089b512d641710` | `qr-comp-goat-07.png` | `49597d6a370b5293597e3d4bdd1f6ff693720ffb2025151d17edb4e9abe8f241` |
| 8 | PENNY FOR YOUR THOUGHTS | `SIG·COMP-GOAT-08·14A364C6` | `14a364c6a1b58595f9359b018e6e8df4c72d1b884d714c74305e65cf33c22756` | `qr-comp-goat-08.png` | `35fc2a08525563dc50387fe9a094db7c21f28acc428937e12af0ef5181c7cb8c` |
| 9 | MADE IT THREW | `SIG·COMP-GOAT-09·50FEA813` | `50fea813515daf7da8fef71bc66c1e1515bd16b0da252b929040753e08b1f9cb` | `qr-comp-goat-09.png` | `e7d79097585c2a206136d6dad40d0c235e7201926d7ed10db68c4a0e1ff23e5c` |
| 10 | DID YOU | `SIG·COMP-GOAT-10·39D193EB` | `39d193eb13323c2f78d71aed0c66d38817f4ffa8631d345759d0cd46ceeebfa2` | `qr-comp-goat-10.png` | `7665ad136564f73b16e3bffe9b5e95fbd11f432fbc7749a0bc5c53171f420ed2` |
| 11 | Convo wit tak at wash's | `SIG·COMP-GOAT-11·DC7C2180` | `dc7c21801348862aaa7570b64d3e2b5c699df521d28ec6e02bc5bf47d16e2154` | `qr-comp-goat-11.png` | `f2e4ae73e55246eab9e7986ca9de683959432823d5866b178c7df1801d5b58e3` |
| 12 | cool master | `SIG·COMP-GOAT-12·B7EA1439` | `b7ea1439d0d3e47971cc1d4e2e8cbc7433d6123f188e0e6c8b7740fd90b674ee` | `qr-comp-goat-12.png` | `f7b50aa9748d69780bae58d0588e1073432321aba0989537cca773b6e584f127` |
| 13 | Thinking of you (BONUS TRACK) r.i.p fallen artist | `SIG·COMP-GOAT-13·D39E8615` | `d39e8615e7e85b0b38bf45e99d3ef480140b7d76e0e3d9148bb902aebaf121d5` | `qr-comp-goat-13.png` | `8118f909427a7ce18e38c4358df50aa3fd1c70acd2d7565ad75a735585529dba` |

---

## THE TWIN TABLE — 100 KEYS, PHYSICAL ↔ DIGITAL

KEY-F01–KEY-F03 are the Founder's Keys (twins of the founder's 3 retained units); KEY-001–KEY-097 are the fan keys (twins of the 97 distributed units). Patron tracks follow the set record's assignment rule: album order, repeating 1→13 (tracks 1–6 patron 8 fan keys each; tracks 7–13 patron 7 each; the Founder's Keys take tracks 1, 2, 3). Each key's QR payload names its certificate (CERT·GOAT-KEY-〈number〉), its patron track, its patron piece's signature, and its class.

| Key | Class | Patron track | ISRC | Patron piece signature | Key QR file | Key QR SHA-256 |
|---|---|---|---|---|---|---|
| KEY-F01 | Founder's Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-f01.png` | `a46edfc3077d90c8efd32240f91b416838f518aa2867a408f292d7af4ad3d3fe` |
| KEY-F02 | Founder's Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-f02.png` | `eb2831679d60d7bb77dc03b17f926a8321d0c14daf042cf9f7e520b5f77aaed0` |
| KEY-F03 | Founder's Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-f03.png` | `220c5e917f2bc7fc7993b34e71e2b167409d8845d7591f6dd7f05e5c21cbc2fc` |
| KEY-001 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-001.png` | `250bc93c3872e25383acf92b594dfb45c71eac6d8231e4c19bdf7fa1521494d9` |
| KEY-002 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-002.png` | `f7df5e84866c9ac4f984591b24ece35f8c32d81dec84c758b4f364099a26f0fc` |
| KEY-003 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-003.png` | `dfe652a3c135cd3d2c99b6a83e44b3c961f0c1308afccb5ee6b3be9e7a79ee17` |
| KEY-004 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-004.png` | `aac1249589d78a26db3b442b9d112b56a69509ca19d4c81aa14978b949fb1858` |
| KEY-005 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-005.png` | `ac589143da98fa78e77055b5676a041a029a0ecf8c4e7bed6057a40e4e9780db` |
| KEY-006 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-006.png` | `6321dda0fc16ea420014954c2f4df48300e382921ff293585e2ba0fe0dbedb9f` |
| KEY-007 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-007.png` | `97e58a9880c7ab5f5074ca9778a0113a6d5d43a0607fef42457ed45461984990` |
| KEY-008 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-008.png` | `48cd505a02c0eebce9421a4aabbfd9807f2870acfbf32a5d8e4126fcfc38843b` |
| KEY-009 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-009.png` | `6ad811ddee8a1623ce18603ca5a90e40b15854b1cbe7d8c3c06fc66c1bdba9e1` |
| KEY-010 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-010.png` | `ba27131ceea7cbe26613741d596e0274ce122e4e81984e928e20c11adb45bb0b` |
| KEY-011 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-011.png` | `0424ec47f577869d27a5ff3ad6b45fb3d318aa3ad492504b5a3480094b3ac873` |
| KEY-012 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-012.png` | `9de08dceb49ffbfe9829d770221d3ae504426c27753b1c9aad06e3d74231b0ac` |
| KEY-013 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-013.png` | `f1312f13d41ce88cb650d04f8e77b220b683f33b11e3ccfb34c915d9d0662067` |
| KEY-014 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-014.png` | `dff8201ea3ae093f18b554772c5caa97c7961793542e13988d1f2fb04bc8947e` |
| KEY-015 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-015.png` | `b71fd837ac85991b0d892b8869bfb92bf6c15c2a27a6a3a861686d91b0ae24f9` |
| KEY-016 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-016.png` | `cc20d51264975d5b4dabe7f7c50f510f82a7a33fe4335cc947a6a193b70ccc14` |
| KEY-017 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-017.png` | `76704790822d38925b4f87623c8ae347fd8b91d2b1e502c963428ae4ee323cb4` |
| KEY-018 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-018.png` | `a06ec14deadfe988376615a4c06b2cff36c15c136a6f933516bd9f975548f157` |
| KEY-019 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-019.png` | `af01ddbb1b9537a65eaadfe0e99672a6530124d1feb1d69915a25fca96236aa7` |
| KEY-020 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-020.png` | `3b5fb1c4fdc49d8dbeb407fd83718aab880551169cc899408d295d536da53fef` |
| KEY-021 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-021.png` | `d9800f5a8ad89d64add627c958264b381092efd4cb51fd75de951f1e183e2d81` |
| KEY-022 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-022.png` | `5694a9dd4e57b509d8433eb766f7b1174121e00a42a200e7f67406ce0e36def3` |
| KEY-023 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-023.png` | `25c839941e217678f7bfa67edada335de6af6bf97c3fdccf647a4cbe00928c4d` |
| KEY-024 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-024.png` | `642859aa362556ae1602a5e27eed3c25b8ceeb522f274babfcdd1c3d81668ffe` |
| KEY-025 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-025.png` | `398b2a32b411067c756a9bc0fe18d1adb19b147dc1f88b1c9df460d28b12e2f5` |
| KEY-026 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-026.png` | `c60cf2d6c0220846ce816bbc3a160bc3bcf42f3a84a85b08ee14bf3416fa208a` |
| KEY-027 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-027.png` | `e4c52c04af5d19eaaa0d373269f32124b3212966e05c321b6da657b38da55098` |
| KEY-028 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-028.png` | `b7c93632acc93e26d166b9feef57b8d6bf2f5c13a6ba342c1975f99b72143a51` |
| KEY-029 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-029.png` | `2bb87ef09737ec4f8195f63b032e04b683cd899341ce580eadc140e031b9eb3e` |
| KEY-030 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-030.png` | `40eb27da5d613e150bba35732998c04f5402dde12d55108c833c942449b1b76f` |
| KEY-031 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-031.png` | `4632a5a6cf54608636a0ee8ef9af9e6519be09da54bb4af5842a57fda197c054` |
| KEY-032 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-032.png` | `5e45040119a8ac9f971504d32e5f516dd808c4b7b0ecec35269eb62017f74a63` |
| KEY-033 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-033.png` | `420b9cf77f93e5d01a8160d036d5a61eadc449f8ee316bfa238c6917e17676c2` |
| KEY-034 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-034.png` | `5082f13b50fa660cc6edd6b35076db2a42a91ad422710f4cbf8605a50a28ed4e` |
| KEY-035 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-035.png` | `f533ee0a47cfd8d1d42f1919ff22f1da66322876f61b530a1d4ba296f6361f9c` |
| KEY-036 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-036.png` | `88aa4db54e82fe040da6b479ed7eb37ec9b9190bd03ce266ea34c001a8aa96c0` |
| KEY-037 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-037.png` | `3d2e6d0acf7d680882f5098da1c2dacb341fbf26e70b7293b83b4fba79864258` |
| KEY-038 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-038.png` | `ef81fd656fda980b88b78fa72cee8e1bfe5d5903014abcfb3598c336d9fd0179` |
| KEY-039 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-039.png` | `1f0ef0fc0e9be052bde6360a0eb07447024d564581f977d09b0d06d85fffe2c9` |
| KEY-040 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-040.png` | `59c9d486d55a620f41e89887453f0d99d99b5204aec367d83302afa813e5c551` |
| KEY-041 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-041.png` | `64f1b06f7aeda85f66e07e792c1406449fdc9a3f93b39406297bdcecff2a053e` |
| KEY-042 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-042.png` | `de22559b91229b9e99f99bb6d49bb45728779cfa4135c18bec17a97b701cde7f` |
| KEY-043 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-043.png` | `7d751ec58d47918a98fe503e87a5ebb88ba39ddd079fa428dfe2698c0759b32f` |
| KEY-044 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-044.png` | `fc64714b01c1da2a6ce95b6beb9efd768c392ba450b61c1c739673084761e1d4` |
| KEY-045 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-045.png` | `043a6883710d86894bca84296cff1f12d486b5ad4fb963d24d83489e20388fca` |
| KEY-046 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-046.png` | `85dd3285faccb18057f96c5a3ac15544d4321ad829e002fa766da4705d09a219` |
| KEY-047 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-047.png` | `dc48da2a50af325bc479cec5479f468b779354a9462d7bc9c73765739a6afe83` |
| KEY-048 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-048.png` | `49c029e5a5eafb4eef799fee26b8685eaca2820bf6ea4642ffe1262ef8f4ce52` |
| KEY-049 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-049.png` | `e9eb0e0d379dc27fea97586f87123eacb229d03be0767198c11f582938129d8e` |
| KEY-050 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-050.png` | `74eb78b9221ce111eba4d58197cb3f5c96586e4a895b04f21deca3b75e190b5a` |
| KEY-051 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-051.png` | `65d5de1576f6027d84af3208842f6ac4bf67546968d183d99c0b3edb7f38a5eb` |
| KEY-052 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-052.png` | `b3bb2e17210eeb24d8fa595941859cd413bba2b3a3b38aa19762746c4aa163ec` |
| KEY-053 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-053.png` | `312ecc5c1003053ca34ac9ade74e52cde70026e4a4eab94d0200e7826aed393f` |
| KEY-054 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-054.png` | `0375173fa61902008ea43c1fa2110d96918d06de8c0aedf138f384aa666fdace` |
| KEY-055 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-055.png` | `241047d6406c60ccfad0c520487885666e2aeb5f701445514479e084fe4123a9` |
| KEY-056 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-056.png` | `6d90fbffcd81413408740e3dbaa1c198292698db1ae6083d6cfced8ad15d3314` |
| KEY-057 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-057.png` | `13a0a90756895bdee5aa12f9436b1b0de072473473f3ea435edca3279badee9d` |
| KEY-058 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-058.png` | `1310e46874475b1ed83f5fe8c8e35e84c5b3f985b29dd3f786a5b84e0a956b99` |
| KEY-059 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-059.png` | `80bdb789c860053ce33e0ff6aac1f9bcaffcb7d692333bf7e25678fdc72d37f9` |
| KEY-060 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-060.png` | `3e0f21bd2640c9f82f1a897fd557d6fbfe32fb28883bb790a2145dc7173f4026` |
| KEY-061 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-061.png` | `6a0175beda5691acf64b97fe469d0d1a26c65c635d247bc2e03cd5309095c29b` |
| KEY-062 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-062.png` | `4dae1f0b245078f944393d5eaa27b6e82d8e6d6f21e4d650ce779195acf7532a` |
| KEY-063 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-063.png` | `84fd22303c6368e8a35e1cbf77549f6e498add614e37c1a1095d70d5f06fa8ca` |
| KEY-064 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-064.png` | `716486abbfec7c577eace08d79c4da46fe72c82d23be6e1adbea460146f37472` |
| KEY-065 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-065.png` | `5fe3da8bfd235bf0ff82d5d6e82792541b5e0d6f200e0bf3e44814793f461bbc` |
| KEY-066 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-066.png` | `41d73b3a5f8db9201f596bbec5321eb2cdacaa2a28406b7decf0915d7e27e9ac` |
| KEY-067 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-067.png` | `4b7350ade1f4feb203842a6a6bbacf49502c99ed20157816d64c49317037221f` |
| KEY-068 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-068.png` | `218b4405238717bd51bb58c418704d94e2be30bc396dd0015f958cdbab1b0469` |
| KEY-069 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-069.png` | `fda437b5c1f06e53bcf36a7c1a232cff38c91c7295c2b61ed386269fbdef2ec9` |
| KEY-070 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-070.png` | `4778a1146336429156724bff8151af7feed64c38bf71a066c0b2a68a052f35d6` |
| KEY-071 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-071.png` | `7f377c9c3c1c26205f3cee0f61b82f5abb2aebea3eeeb5ff98410952956d004e` |
| KEY-072 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-072.png` | `6fe379b8bb86bab4901cd386fdfaa83d65566b7ededc21d81b0609fe85fb9f8c` |
| KEY-073 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-073.png` | `1c43863c034e736ed98536d35581ed74e062f211cd5406a11c3be5841b63f0a9` |
| KEY-074 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-074.png` | `0aaf24e979b407a4e8943fd8d20b1b765af6175b4cabe72469df5c71c6051600` |
| KEY-075 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-075.png` | `15ade9f8dee67af266a201e5cb01f674a4bf148680820ecd88e620928afa9b56` |
| KEY-076 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-076.png` | `e97088af6e79f48f3de147f5085ffff2245c028ea6bef0dec80d5e2494c7de7a` |
| KEY-077 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-077.png` | `93c58a8f250aa1f71bd2ea277f73488ecf217351bf5a2795d881621226d0234c` |
| KEY-078 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-078.png` | `ce031d2677c0ade16d3188a543357b73a509f2e611e7efe2884c2865709de691` |
| KEY-079 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-079.png` | `43bcee59317a9ccf50a335d71ba43aba6bdef93c608ccef25dac59e17419ced1` |
| KEY-080 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-080.png` | `94c079fcaa7debe067db12c2f3349294e156b9062ed94163abcc92578f2b62f7` |
| KEY-081 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-081.png` | `362c20e7f8ac72ae633bd7c195c00dc1187b3cc89498f5cfdd9be2e61df4dd3d` |
| KEY-082 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-082.png` | `682bb90a4a95b04d92821893fb24f13736292239138bce56a17c79f4872707c7` |
| KEY-083 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-083.png` | `05f4821a015163adb162c7ab723beda3ea2d632b47d76082af92fd30d974bf02` |
| KEY-084 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-084.png` | `34730b6c4d6a06c0165c0d5c6da87125809d8eb9278b7541ea69cd1c6359eb9a` |
| KEY-085 | Fan Key | BUDDY CRAWFORD | QZS7J2457853 | `SIG·GOAT-TRK-07·FADED333` | `qr-key-085.png` | `3e61dbf3bff354ab3c8b3e15c6798142c6ba836f1f807e77b2beb9f054cb1068` |
| KEY-086 | Fan Key | PENNY FOR YOUR THOUGHTS | QZS7J2401332 | `SIG·GOAT-TRK-08·913082F4` | `qr-key-086.png` | `af97d89cdaf0c15a5076b94a3ae4076067c997b9cc6676a1910305d3390e2e20` |
| KEY-087 | Fan Key | MADE IT THREW | QZS7J2425503 | `SIG·GOAT-TRK-09·78AC8DBE` | `qr-key-087.png` | `0094f9eb0d493c7c166b4682e8ed395d7909c4388301f5a146b127b8cab41845` |
| KEY-088 | Fan Key | DID YOU | QZS7J2442319 | `SIG·GOAT-TRK-10·4DBDE33C` | `qr-key-088.png` | `678ba0447ca6898f3eb9b8537c0470944a42e47bb1e211402393920d53410135` |
| KEY-089 | Fan Key | Convo wit tak at wash's | QZS7J2476570 | `SIG·GOAT-TRK-11·A60BAC34` | `qr-key-089.png` | `4262842331bb7f65cfc0b580a1aa76a6951070246bc9d52870d10c4ad2f84d0a` |
| KEY-090 | Fan Key | cool master | QZS7J2465944 | `SIG·GOAT-TRK-12·C753582F` | `qr-key-090.png` | `b99898e1e80110e512bfd7c8e284d173b5b7efb29c62d199ec5c5a871bbf18b1` |
| KEY-091 | Fan Key | Thinking of you (BONUS TRACK) r.i.p fallen artist | QZS7J2423723 | `SIG·GOAT-TRK-13·8829D1F0` | `qr-key-091.png` | `739a7de72c069d11c941c21170b0fbafa5fb57100143f4553652acab52c0abda` |
| KEY-092 | Fan Key | RICHARD PRYOR | QZS7J2421413 | `SIG·GOAT-TRK-01·DDFCBD3B` | `qr-key-092.png` | `603bd805eb2a37112400cd65040dab54b0b22075e6cb36a7c981d65801c2665f` |
| KEY-093 | Fan Key | THE GHOST OF BIG | QZS7J2403531 | `SIG·GOAT-TRK-02·C9F5BAD6` | `qr-key-093.png` | `3d0e8acfb55e4fb5a00f7e58fdf7815dbd8743d93b755f72cbbf2af5e13f8158` |
| KEY-094 | Fan Key | PROMISE LAND | QZS7J2424027 | `SIG·GOAT-TRK-03·FA167578` | `qr-key-094.png` | `0e96de0e5ec6e16e953be60849a46c2d7ea0541c1f4b39120008d764d09e1615` |
| KEY-095 | Fan Key | Nipsey Mentality | QZS7J2403399 | `SIG·GOAT-TRK-04·5A89828F` | `qr-key-095.png` | `91e291d9595465934133a8d59317ed935e9a34d091975d3eeefe17aff124ceed` |
| KEY-096 | Fan Key | IN MY BAG | QZS7J2435352 | `SIG·GOAT-TRK-05·3CA853E4` | `qr-key-096.png` | `673e93f0d1786bf610a3373442ecbe73b137150742c6a4556a61594e6212ca79` |
| KEY-097 | Fan Key | HOW I REALLY FEEL | QZS7J2444796 | `SIG·GOAT-TRK-06·4DF060B6` | `qr-key-097.png` | `8986bac21cf4dbda07cd6a32685fbe6faeaf3d183059baec8615dceef380a814` |

---

## MASTER TWIN FINGERPRINT

**`e34bb87934df29d4f920a11ff23c921cf1ad4a3b100d95397ffbf9e87319c62e`**

SHA-256 of the canonical key-table text: the 100 key rows in table order (KEY-F01, KEY-F02, KEY-F03, KEY-001 … KEY-097), each row rendered as `KEY-〈number〉|〈class〉|〈patron track〉|〈ISRC〉|〈patron piece signature〉|〈key QR filename〉|〈key QR SHA-256〉`, rows joined by a single LF (\n), UTF-8, no trailing newline. Recompute it from the table above and the hash must match — any changed row, any swapped QR, breaks it.

## VERIFICATION

Decode check (zxing-cpp, a true barcode decoder, not a re-render): **all 131 QRs were machine-decoded from the saved PNGs and every decoded text matched its intended payload byte-for-byte** — 18 piece QRs, 13 composition QRs, and all 100 key QRs.
Image check: every QR PNG is square, black-on-white with a 4-module quiet zone, error-correction level Q; pixel sizes run 1220×1220 to 1460×1460 (all ≥800×800). Every QR SHA-256 in the tables above was computed over the saved PNG's actual bytes.

## AT THE GATE

**Nothing in this layer has been minted. Nothing is listed. Nothing is priced.** The QR signatures and this registry are a verification and binding record, built to the same gate as the rest of THE GOAT SET: the founder funds the mint wallet, sealed mint copies and AES-256 certificate secrets are prepared at mint time, and the founder's start call — naming the platform and the run — governs every mint. Free/lazy minting stays OFF (the Piece 0 ruling).

---
*Twin registry compiled 26 Nov 2026. Sources: `set-record.md` (piece + patron-track signatures and SHA-256s, key-edition architecture) · `composition-seal.md` (composition seal IDs and fingerprints) · `hp-016-goat-cassette-usb-run-2026-11-26.md` (the physical run: 100 units · 3 founder-held · 97 fan-held). QRs generated with the Python `qrcode` library (error-correction Q) in `~/workspace/.venvs/qr`; decoded back with zxing-cpp for verification; all hashes computed with SHA-256 over actual file bytes.*
