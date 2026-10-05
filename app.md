# App — System Prompt Rules

> AI-generated UI ko real human-like best UI banane ke liye App specific guidelines.

## 🔔 Notifications — Badges & Status Dots

### Badge Count Behavior
- Ek unread pe single count dikhao; 200 jaisi badi value pe **"99+"** dikhao — cap badge ki shape stable rakhta hai.
- Badge hamesha icon ke **top corner** pe pin hota hai.
- Count 1 digit ho ya 3 digit, **icon kabhi apni jagah se move nahi hona chahiye** badge ke niche.
- Jab count badhta hai to badge **tick-up animate** hota hai — screen par kabhi zero pe reset/snap mat karo; wo flash users ko **bug** jaisa lagta hai.

### Badge Meaning & Colors
- 🔴 **Red = "act now"** — turant action chahiye.
- 🟢 **Green = online / active status.**
- Counting badge aur status dot **do alag objects hain** — inhe kabhi mix mat karo.
- Dot ka matlab: *"kuch change hua"*; number ka matlab: *"kitna hua"*.

### Noise Avoidance
- Status dot aur count badge dono ek saath dikhana **noise** hai — sirf ek use karo.
- Badge **sirf un cheezon pe lagao jinpe decision/action lena zaroori ho.**
- Agar sab kuch pe badge lagaoge to color apna meaning kho dega — red ka urgency khatam ho jayegi.

### Badge Clearing
- Badge usi moment **clear ho jana chahiye jab user wo view open kare.**
- Agar badge dekhne ke baad bhi linger karta hai, to users **har badge ko ignore karna seekh jate hain.**

> Source: designmotiony.com (UI systems series)

## ⚡ Perceived Speed — UI ko Fast Feel Karwana

> Same loading time, different feeling — ye 3 tricks app ko lightning-fast feel deti hain:

### Trick 1: Skeleton Screens
- Kuch bhi khali dikhane ke bajaye, **layout ka skeleton dikhao.**
- **Shimmer animation** brain ko signal deta hai ki content aa raha hai.
- Result: user ko **wait chhota perceive** hota hai.

### Trick 2: Optimistic UI
- Jab user button tap kare, **server ka wait mat karo.**
- **Success turant dikhao** (UI pehle update karo, server baad me confirm kare).
- Brain **instant feedback ko speed ki tarah register** karta hai.

### Trick 3: Progress Bar Psychology
- Progress bar **fast start** ho, aur **end pe slow** ho.
- Total time same hone ke bawajood, brain **quick start yaad rakhta hai** — isliye pura process faster feel hota hai.

### Teeno Ek Saath
- **Skeleton preview** (load hote waqt) + **instant UI updates** (actions pe) + **psychological progress** (long tasks pe) — jab ye teeno saath kaam karte hain to app genuinely fast feel hoti hai.
- Yaad rakho: **"Perception is reality"** — actual speed se zyada, **fast feel karna** matter karta hai.

> Source: UX tricks series (perceived performance)

## 🔤 Typography System — 7 Decisions

> Typography ek system hai. Same font + sirf 7 decisions — aur UI product jaisi professional lagti hai:

### 1. One Font Family
- Pure product me **sirf ek font** — fonts mix mat karo.

### 2. Max 5 Sizes
- Kabhi pixels **handpick mat karo.** Ek hi scale ratio use karo: **1.25.**
- 11 sizes ko collapse karke **sirf 5 sizes** rakho.

### 3. Sirf 3 Text Colors
- **Primary, Secondary, Muted** — 3 colors 10 sizes se zyada kaam karte hain.
- **Color rank karta hai line ke andar**; **size rank karta hai blocks ke beech.**

### 4. Sirf 2 Weights
- **400 (Regular)** = reading ke liye; **600 (Semibold)** = scanning ke liye.
- Jab sab kuch bold hota hai, to **kuch bhi bold nahi hota.**

### 5. Line-Height Size ke Ulta Chalti Hai
- Headings pe **1.1**, body pe **1.5.**
- Har jagah same line-height value = **AI-made tell.**

### 6. Letter-Spacing Rules
- **24px se bade** sizes → tighten karo: **−2%.**
- Chhote **uppercase labels** → open karo: **+5%.**

### 7. Line Length (Measure) & Tabular Figures
- Body text **45–75 characters per line** rakho.
- 1400px pe stretched paragraph unreadable hota hai — **measure cap karo, container nahi.**
- Tables, prices, timers ke numbers me **tabular figures** use karo (`font-variant-numeric: tabular-nums`) — warna har update pe **column wobble** karega.

**Yaad rakho:** 7 decisions → ek font jo product jaisa read hota hai.

> Source: UX Engine ("kills the AI look" series — typography)

## 💬 Chat UI System — 6 Decisions

> Same thread, half the noise — ye 6 decisions chat ko clean aur readable banate hain:

### Decision 1: Message Grouping
- **Same sender, 2 minutes ke andar** ke messages → **ek group, ek avatar.**
- Group ke andar **4px gap**; groups ke beech **16px gap.**
- Reader **logon ko scan karta hai, lines ko nahi.**

### Decision 2: Time — Precision On Demand
- ❌ Har bubble pe time mat dikhao.
- ✅ Jab date change ho → **date divider.**
- ✅ Exact time **sirf hover pe.**
- Precision **demand pe mile, kabhi raaste me nahi.**

### Decision 3: Instant Send Feedback
- Enter dabate hi **bubble turant dikh jaye** (optimistic UI).
- **"Sent" state baad me fade-in** ho.
- Fail hone par **red retry inline, usi message pe** dikhe.
- ❌ **User aur uske apne words ke beech kabhi spinner mat lagao.**

### Decision 4: New Messages — List Kabhi Jump Na Kare
- Agar user padh raha ho aur naya message aaye → **list jump nahi karti.**
- Ek **pill naye messages ka count** dikhata hai.
- Pill tap karo → **smooth slide to bottom.**
- **Anchoring sirf tab** jab user already bottom pe ho.

### Decision 5: Typing Indicator
- Typing indicator **flow ke andar** rehta hai — jahan agla message aayega, wahi jagah.
- **Three dots + avatar attached.**
- Jab indicator hat-ta hai to **baaki kuch bhi move nahi hona chahiye.**

### Decision 6: Composer & Attachments
- Composer **5 lines tak grow** hota hai, phir **scroll** karta hai.
- **Enter = send**; **Shift+Enter = new line.**
- Attachments ka preview **text ke upar** dikhe — **kabhi text ke andar nahi.**

**Yaad rakho:** 6 decisions → ek thread jo padhne layak rehta hai.

> Source: UX Engine ("kills the AI look" series — chat UI)

## 🧠 CSS `:has()` Parent Selectors — Zero JavaScript

> Ek line CSS — aur pura UI khud react karta hai. 20 saal tak CSS sirf niche aur aage dekh sakta tha; ab ye **upar (parent) bhi dekh sakta hai.** `:has()` har browser me 2023 se available hai.

### 1. `card:has(:checked)` — Card Apne Checkbox Pe React Kare
- Jab plan check hota hai, **pura card khud react** karta hai — koi JS event nahi.

### 2. `field:has(:user-invalid)` — Validation Sab Jagah Ek Saath
- **Border, label, aur icon — sab ek saath turn** hote hain.
- **No change handler, no React error state** — browser ko pehle se pata hai ki email galat hai.

### 3. `form:has(:user-invalid)` — Pay Button Khud Gray Ho
- Form me kahin bhi invalid field ho → **Pay button automatically gray out** ho jata hai.

### 4. `app:has(aside)` — Layout DOM Ko Follow Kare
- Sidebar render hua → **grid ek column grow** karta hai; sidebar hataya → **grid collapse.**
- **Layout follows the DOM, not a Boolean prop.**

### 5. `grid:has(:nth-child(5))` — Quantity Query
- 4 cards wide baithte hain; **5th aate hi sab tighten** ho jate hain.
- CSS me hi **quantity query** — **JavaScript me counting nahi.**

### 6. `body:has(dialog[open])` — Document-Level Modal Reaction
- Modal khulte hi **scroll lock**, piche ka page **dim** — pura document react karta hai.
- Dialog khud kuch nahi karta (zero logic).
- Band karo → **sab kuch wapas**, **no cleanup effect.**

**Yaad rakho:** 5 selectors, **zero JavaScript.**

> Source: UX Engine ("kills the AI look" series — CSS :has)
## 🔲 Corner Radii — Corners Ek System Hai

> Har corner rounded hone ke bawajood UI "off" lagti hai kyunki corners ko system ki tarah treat nahi kiya jata:

### Rule 1: Inner = Outer − Padding (Concentric Corners)
- Same radius inside aur outside → **inner corner bulge** karta hai.
- ✅ Formula: **Inner = Outer − Padding.** Example: outer 12px, padding 8px → inner 4px.
- Tab corners **concentric** ban jate hain.

### Rule 2: Radius Follows Size — Ek Scale
- ❌ Har cheez pe 8px — chip aur modal corner share nahi karte.
- ✅ Ek scale: **Small = 4px, Medium = 8px, Large = 16px** — har element usi pe ho.

### Rule 3: Full Radius Ek Number Nahi, Shape Hai
- Pill **sirf single-line content** ke liye fit hai — chips, avatars, toggles.
- Cards jaise multi-line content ko **real number radius** chahiye — full radius corners ko content nigal leta hai.

### Rule 4: Corner Ka Matlab Hai Uske Aage Space
- Bottom pe docked sheet → **top corners round, bottom corners zero.**
- Jo element **edge touch karta hai, uska corner nahi hota.**

### Rule 5: Selection Ring — Formula Ulta Karo
- Ring ko apna box maan ke (2px bahar) radius inherit karo to **corners pinch** ho jate hain.
- ✅ **Outer = Inner + Gap.** Example: inner 8px → outer 10px.

### Rule 6: Rounded Card Me Images
- Edge-to-edge image ke square corners bahar poke karte hain → **card ko clip karne do** (`overflow: hidden`).
- Inset image: **padding subtract karo, same rule.**

## 🌙 Dark Mode — Terminal Nahi, System

> "Black background + white text" dark mode nahi, **terminal** hai:

### Pure Black Nahi, Near-Black Se Shuru Karo
- Pure black OLED battery bachata hai, lekin **depth maar deta hai** — black se niche kuch nahi baithta, isliye **har surface ek hi plane ke liye fight karti hai.**
- ✅ **Near-black se start karo** — layers ke paas room hota hai.

### Elevation Shadows Se Nahi, Lightness Se
- Dark me **shadows mar jati hain** — black pe black invisible hai, card kahin bhi float nahi karta.
- ✅ Surface ko **lightness se raise karo** — jitni upar ki surface, utni lighter.

### Text: Three Tiers, One Variable
- ❌ Pure white text **vibrate** karta hai — dark surface pe full contrast ek paragraph baad burn karta hai.
- ✅ **Primary = 87%**, **Secondary = 60%**, **Disabled = 38%** — teen tiers, ek variable.

### Brand Colors: Lighten + Desaturate
- Dark surface pe saturated color **edges se bahar glow** karta hai aur content se zyada chamakta hai.
- ✅ **Lighten karo, desaturate karo** — same hue, less weight.

### Hairline Edges Alpha Se
- Edges ko hairline chahiye: **1px white at 8% alpha** — kisi bhi surface pe read hota hai.
- ✅ **Fixed gray ki jagah alpha use karo** — surface lighten hone pe line khud adapt hoti hai.

### Photos & Illustrations
- Dark page pe bright photo **glare** karti hai → **brightness 90% pe dim karo.**
- Illustrations ko **dark variant** mile — filter nahi.

## 👤 Avatars — Fail-Safe Component System

### Fallback Chain
- **Image first; fail hone par initials; generic icon = last resort.**
- ❌ Kabhi **broken square** mat dikhao.

### Color Name Se Generate Ho
- Background color **naam se hi generate** ho — same person, **same color, har screen pe, forever.**
- ❌ Random palette nahi.

### Initials Rules
- Default **do initials** (first + last name); **single letter sirf tiny sizes pe.**
- "JD" insaan jaisa read hota hai; akela "J" **bug jaisa** lagta hai.

### Groups & Overflow
- Group dikhane ke liye avatars **overlap** karo.
- Row **cap karo**, baaki **"+3"** me spill ho.

### Status Ring Pe Ho, Badge Pe Nahi
- Avatar ke ring se pata chale **kaun online** hai.
- Status hamesha **ring pe — dusra badge kabhi nahi.**

### Teen Sizes — Bas
- **24px** lists me, **32px** headers me, **40px** profiles me.

## 🔢 Number Formatting — Align, Abbreviate, Relative Time

> Pro ke numbers line up hote hain; amateur ke numbers dance karte hain:

### Tabular Figures On
- Default fonts har digit ko apni width dete hain (1 patla, 0 chauda) → **columns wobble.**
- ✅ **Tabular figures on** — har digit same width, decimals **seedhi column me snap.**

### Numbers Right, Text Left
- ✅ Numbers right-align, text left-align.
- Aankh magnitude **last digit se compare** karti hai, first se nahi.

### Bade Numbers Abbreviate Karo
- **1,000 → 1k**; **1,000,000 → 1M.**
- **Full precision hover pe** mile.

### Relative Time
- ❌ "14:32" insaan ke liye kuch mean nahi karta; ✅ **"2 hours ago" sab kuch mean karta hai.**
- **Recent ke liye relative, purane ke liye absolute.**

### Currency Alignment
- **Currency symbol ko number column se bahar** rakho.
- **Decimals align karo — dollar signs nahi.**

## 🔘 Buttons — One Intent, One Request (Double-Submit Prevention)

### Tap Hote Hi Disable + Locked Width
- Tap karte hi **button khud instantly disable** ho jaye — slow network user ko dusri baad buy nahi karwane dena chahiye.
- Label ki jagah **spinner same button ke andar**, **width locked** — aas-paas kuch bhi jump nahi karna chahiye.
- **Layout shift broken jaisa read hota hai.**

### Sirf UI Disable Karna Kaafi Nahi
- Handler ko **apne code me directly guard** karo.
- Server ko **real idempotency key** do.

### Success & Error Handling
- ✅ Success pe: spinner **check me morph** ho, **ek full beat** ruke, phir user ko aage le jao.
- ❌ Error pe: **snap back** karo aur reason **wahin button pe** batao.
- Re-enable **sirf real request resolve hone ke baad** — timer pe nahi, guess pe nahi.

## 📋 Copy Button — One Click, One Checkmark

### Instant Feedback
- Copy fire hote hi copy icon **check me flip** ho — **no spinner, no delay.**
- Check ko **~2 seconds hold** karo, phir copy icon pe **fade back.**
- Check forever stuck rahe to **agli copy pe koi signal hi nahi milega.**

### Raw Value Copy Karo
- **Raw value copy karo** — formatted span nahi jisme line breaks aur hidden zero-width characters hon.
- (Aisa paste terminal me daalo — toot jayega.)

### Accessibility: Announce Karo
- Icon chup-chaap badalta hai to screen readers ko **kuch sunai nahi deta.**
- **Live region se "copied" announce** karo — silent success bhi kisi ke liye failure hi hai.

### Insecure Origin Fallback
- Insecure origin pe clipboard call **bina bataye fail** hoti hai.
- **Legacy copy command pe fall back** karo.
- **Silent button jhooth bolta hai.**

## 🖱️ Scroll Memory — SPA Position Bhool Nahi Sakta

### Har History Entry Ke Liye Scroll Save Karo
- Back dabao aur wo post kho gayi jahan tak scroll kiya tha — SPA har route change pe **scroll zero** kar deta hai; browser pehle ye khud yaad rakhta tha, router ne bhula diya.
- ✅ **Scroll position har history entry ke liye save** karo, aur user ke lautne par **wapas restore** karo — top pe phekna nahi.
- **Position bhi state hai.**

### Sticky Header Ka Offset
- Sticky header landing row ko chhupa deta hai → restore ko **header ki height se offset** karo, warna "close but wrong" landing hoti hai.
- Jump links pe **`scroll-margin-top`** lagao — warna heading bar ke niche chhup jati hai.

### Infinite Scroll Footer Ko Hamesha Dur Dhakelta Hai
- Links, contact, terms — sab footer me rehte hain, aur **koi wahan tak pahunchta hi nahi.**



## 🚫 Disabled Buttons — Button Ko Alive Rakho

### Disabled Button Reason Chhupa Deta Hai
- Gray button click karo → kuch nahi hota, aur **kuch batata bhi nahi kyu.**
- Disabled button **tab order se bahar** nikal jata hai — keyboard users skip kar dete hain, screen readers chup rehte hain.
- Gray-on-gray **contrast fail** karta hai — label bhi aapse ladta hai.
- ❌ Disabled element pe tooltip **kabhi fire nahi hota** (pointer events dead hain) — reason **by design unreachable.**

### Button Live Rakho
- ✅ Click pe **validate karo aur jo fields block kar rahi hain unhe light up karo.**
- **Focus pehli blocking field pe jump** kare — aage ka raasta visible ho jaye.

### Disabled ≠ Loading
- Request ke dauran button **focus hold kare, spinner dikhaye, busy report kare.**
- Gray out karne se **user ki jagah kho jati hai.**

## 🎨 Design System — Ek Source of Truth

### Problem: Kuch Bhi Screens Ke Beech Carry Nahi Hota
- Agar generations ke beech kuch carry nahi hota, to **har screen akeli decide karti hai** — aur product **ek product jaisa dikhna band** kar deta hai.

### Rule Zero: Invent Se Pehle Read Karo
- **Tailwind config, CSS variables, aur sabse zyada reuse hone wala component** padho — agar ye decisions already ho chuke hain, to **system already exist karta hai.**

### Tokens Extract Karo, Invent Nahi
- Tokens **extract karo, invent nahi** — aur har token apne saath **ek one-line reason** rakhe ki wo kyu hai.
- Naya blue aaye to **roko aur closest token se replace** karo.
- Extensions allowed hain — par **reason ke saath likhi jayen.** **Silent invention se hi ye sab shuru hua tha.**

### Ek Decision Per Axis
- Type, color, space, finish — **har axis pe ek decision.**
- **Default ship karne se inkaar karo** — coherent hona distinctive hone se alag cheez hai.

## ✂️ Text Overflow & Truncation

### Flex Me Ellipsis Kyu Nahi Chalta
- Flex child **apne text se niche shrink hone se inkaar** karta hai — naam button ko card se bahar dhakel deta hai, ellipsis kabhi fire nahi hota.
- ✅ Jo child shrink hona chahiye uspe **`min-width: 0`.**

### Middle Truncate — End Hi Jawab Ho To
- End mat kato jab end hi jawab hai — **file name uska extension hai, email uska domain.**
- ✅ **Middle truncate** karo — dono ends survive karte hain.

### Live Numbers Layout Ko Twitch Karate Hain
- Proportional digits alag width ke hote hain → har update **layout ko nudge** karta hai.
- ✅ **`tabular-nums`** unhe ek width pe lock kar deta hai — dead still.

### Long URLs
- Browser **word ke andar kabhi break nahi karta** → ek lamba URL container ko stretch kar deta hai jab tak layout haar na maan le.
- ✅ **`overflow-wrap: anywhere`** use break karne ki permission deta hai.

## 🔁 Buy Flow — Spinner Ke Niche Ka Pura Round Trip

### "Buy" Click → 6 Cheezein Hoti Hain
1. **Browser form validate** karta hai — abhi koi network nahi. **Instant feedback front-end ka kaam hai.**
2. **Request nikalta hai** — ek JSON payload, headers, aur **ek token jo prove karta hai ki aap kaun ho.**
3. **Back-end sab dobara validate** karta hai — client input **kabhi trusted nahi**; koi bhi request forge kar sakta hai.
4. **Business logic chalta hai** — stock check, price check, payment charge.
5. **Database order likhta hai** — ek transaction har row ko wrap karta hai: **ya to sab commit honge, ya koi nahi** — yahi **atomicity** hai.
6. **Response wapas aata hai** — status 200 + order ID jo server ne banaya. Spinner rukta hai; **UI server truth se repaint hota hai — guess se nahi.**

### Optimistic Kab Theek Hai
- Fast apps cheat karti hain: **like, favorite, rename** — instantly repaint karo, baad me reconcile.
- Lekin **paisa optimistic nahi hota** — **payment apna spinner earn karta hai.**

## 💾 Autosave — Ek System Ki Tarah

### Har Keystroke Pe Save Nahi — Debounce
- "Saved." — tha nahi. Wi-Fi shabd ke beech me mar gaya.
- ✅ **Timer pause pe start hota hai, type karne pe reset**; **800ms ki silence → ek clean write.**

### Save Pill Ek State Machine Hai
- States: **Typing → Saving → Saved → Offline → Error.**
- Users **pill pe feature se zyada trust** karte hain — **use kabhi jhooth mat bolne do.**

### Offline Queue
- Offline me har edit **local queue me** jata hai; **badge count dikhata hai** kitna wait kar raha hai.
- Reconnect hote hi **queue order me drain** hoti hai — **oldest first.**

### Conflict: Kabhi Chup-Chaap Overwrite Nahi
- Do tabs, ek document — **last write wins ka matlab kisi ka ek ghanta gayab.**
- **Changes merge karo ya warn karo — chup-chaap overwrite kabhi nahi.**

### Unsaved Kaam Ke Saath Close
- Kaam unsaved hai aur user close kare → **browser tab block kare aur puche.**
- **Ek ugly dialog ek dopahar ke re-type se behtar hai.**

## 🔄 Pull-to-Refresh — Gesture Hi Loader Hai

### Threshold Ke Baad Hi Fire
- Refresh **threshold ke baad hi fire** hota hai — **kabhi pehle nahi.**
- Line se upar release → **list snap back**, koi reload nahi.

### Weight — Resistance Feel
- Zyada drag karo to pull **resist kare** — jaise content me **real weight** ho.
- ❌ 1:1 drag **cheap** lagta hai; **weight hi bechta hai.**

### Threshold Pe Handoff + Haptic
- Threshold pe stretch indicator **spinner ko hand off** karta hai — **gesture khud loader ban jata hai.**
- Threshold pe **ek short haptic tick** — finger glass se uthe, usse pehle hi thumb ready ho jata hai.
- *"The hand knows it caught. Feedback beats the release."*

### Rubber Band Overshoot
- Threshold ke aage → **rubber band overshoot, phir settle** back into place.
- ❌ **Hard stop broken** lagta hai.

### List Alive Rahe
- Reload ke dauran **scroll lock mat karo** — list niche **alive** rahe.
- **Frozen content dead lagta hai.**

## 👆 Hover vs Touch — Mobile Pass

### Touch Pe Hover Fake Hota Hai
- Touch me hover nahi hota — browser fake karta hai: **pehla tap hover ban jata hai**, aur hover-revealed actions **wahi lit freeze** ho jate hain jab tak user kahin aur tap na kare.

### Media Query Se Guard Karo, Device Sniffing Nahi
- ✅ `@media (hover: hover)` use karo — ye **pointer ke baare me puchta hai**, isliye **mouse wale tablet ko bhi full treatment** milta hai.
- Saath me `(pointer: coarse)` pair karo jab **targets ko grow** karna ho.

### Jo Hover Ke Piche Chhupa Hai, Mobile Pe Gaya
- Actions ko **card me, swipe me, ya bottom sheet me** le aao.
- Hover **extras reveal kare — primary action kabhi nahi.**

### Tap Targets
- Tap targets ko **44px** chahiye.
- 20px icon design review pass kar lega, par **thumb miss** kar dega — **hit area pad karo, icon chhota rakho.**

## ✏️ Inline Editing — Editable Text Ko Whisper Karna Chahiye

### Editability Ka Signal Do
- Title click karo → wo input ban jata hai, **kuch bhi move nahi hota.**
- Editable text ko **whisper** karna chahiye: **hover pe pencil, soft background tint.**
- Signal nahi → users **title change karne ke liye tickets file karte hain.**

### Swap Me Har Pixel Same Rahe
- **Same font, same size, same padding**; border **transparent** bana do.
- **Ek jump — aur illusion collapse** ho jata hai.

### Commit/Cancel Universal Hai, Blur Fight Hai
- **Enter commits, Escape cancels** — sab ispe agree karte hain.
- **Blur ek fight hai**: Notion click-away pe save karta hai, spreadsheets discard karte hain.
- **Ek rule chuno — aur use kabhi todna mat.**

### Save Optimistically
- Text **screen pe update ho jab tak request hawa me** hai.
- Server fail ho → **roll back karo, draft rakho, reason batao.**

### Editability Cost Se Match Karo
- Airtable har cell editable banata hai; Docs permission mangwata hai.
- **Zyada power = zyada accidents.** Mode ko **typo ki cost se match** karo.

## 🎯 Destructive Actions — Delete Button Ki Language

### Ring = Confirmation
- **Hold to delete**; jaldi release kiya → kuch nahi marta.
- **Ring hi confirmation hai** — **300ms ka commitment** dialog ko replace karta hai.

### Action Ka Naam Lo
- ❌ "Are you sure?" → "Yes." **Koi nahi padhta.**
- ✅ Action ka naam lo: **"Delete project"** / **"Keep project"** — **verb hi warning hai.**

### Delete Wahan Mat Rakho Jahan Confirm Rehta Hai
- **Muscle memory primary spot pe blind click** karti hai.
- Delete ko **door rakho** — autopilot ki pahunch se bahar.

### Red Ek Budget Hai
- **Red sirf destruction pe kharch karo.**
- Red logout button **bhediya aaya** jaisa hai — phir delete routine lagta hai.

### Geography = Friction
- GitHub deletion ko **danger zone me dafnata hai**: **bordered, labeled, page ki last position.**

### Time = Last Defense
- Kuch platforms **cooldown** dete hain: *"Deletion scheduled — 14 days to cancel."*
- **Waqt aakhri defense line hai.**

## ↩️ Undo System — Deletion Ek State Hai, Event Nahi

### Confirm Mat, Undo Do
- ❌ "Are you sure?" **ek ki galti ke liye sabko punish** karta hai.
- ✅ **Undo kisi ko punish nahi karta** — action instantly hota hai, **regret ko second chance** milta hai.

### Soft Delete Rakho
- File **screen se gayi, database se nahi**: **deleted flag → 30 days trash → phir sach me gayi.**

### Friction Wahi Lage Jo Wapas Nahi Aata
- Kuch actions ka koi raasta wapas nahi — **friction wahi belong karta hai.**
- GitHub repo delete se pehle **naam type karwata hai** — **irreversible ko earn karo.**

### Undo Stack = Time Machine
- Ek undo = **toast**; stack = **time machine.**
- **⌘Z har step me order se wapas** chalta hai — Figma sab yaad rakhta hai, aapka app bhi rakh sakta hai.

### Delay Bhi Feature Hai
- Gmail send ke baad **10 seconds email hold** karta hai — **delay hi feature hai.**
- Typo, galat recipient, reply-all disaster — sab pakde jaate hain.

## ♿ Focus & Accessibility — Ring Ek Haq Hai

### Outline: None = Lawsuit
- `outline: none` **style choice nahi — lawsuit hai.**
- Ring ko chahiye: **2px, offset, aur har background pe contrast.**
- Default ko maarte ho to **usse behtar ship karo.**

### :focus-visible — Dono Jeette Hain
- Mouse users ne ring manga nahi; keyboard users ke bina kaam nahi chalta.
- ✅ **Click = no ring; Tab = ring.**

### Focus DOM Follow Karta Hai, Layout Nahi
- CSS se columns reorder karo → **Tab page pe teleport** karne lagta hai.
- **Visual order aur DOM order match hona chahiye.**

### Modal Focus Management
- Modal khule → **focus andar lock** ho; Tab dialog me **cycle karke wrap** ho.
- Escape close kare → focus **us button ko wapas** mile jisne modal khola tha.

### Skip Link
- 40 links Tab aur content ke beech khade hain.
- **Skip link ek press me sab jump** kar de — **focused hone tak invisible**, page ka **pehla element.**

## ⚡ Optimistic UI — Speed Nahi, Uska Feeling Khareedo

### Screen Pehle, Server Baad Me
- Like click: slow version server ka wait karta hai; fast version **screen pehle update** karta hai, **background me sync.**
- **Same network — ek ne bas wait karna chhod diya.**

### 400ms Ka Rule
- Brain **400ms se niche ki har cheez ko instant** padhta hai.
- Uske baad spinner **broken read hota hai — chahe sab theek chal raha ho.**
- Aap speed nahi khareed rahe — **aap uska feeling khareed rahe ho.**

### Rollback Ready Rakho
- Request fail → **fast wala roll back karta hai**: like khud undo hota hai, count wapas.
- Optimistic hona **errors ignore karna nahi — success pe bet lagana hai.**

### Happy Path Render Karo, Baad Me Reconcile
- Happy path assume karo, **abhi render karo**, server reply pe reconcile — **99% baar aap sahi the.**

### Lekin Har Jagah Nahi
- **Payment, transfer, ya jo undo na ho sake — use kabhi fake mat karo.**
- Unhe **truth dikhao — chahe truth ek spinner ho.**

## 🗣️ UX Writing — Server Jaisa Nahi, Insaan Jaisa Likho

### Button Label = Promise
- "Submit" ek chore hai — aage kya hoga kuch nahi batata.
- **"Create my free account" ek promise hai** — label **commit se pehle padhi jane wali aakhri cheez** hai. Use **payoff banao.**

### Error = Detour Sign, Dead End Nahi
- ❌ "Invalid input" kisi kaam nahi aata — problem bata ke chal deta hai.
- ✅ *"That email's taken. Want to log in?"* — **fix haath me pakdao.**

### Empty State = Pehla Lesson
- Khali inbox **blank screen nahi — pehla action sikhane ka best chance** hai.
- **Ek button, ek next step** dikhao — bug jaisi void nahi.

### Placeholder Label Nahi Hai
- Placeholder **type karte hi gayab** ho jata hai — sawal bhi saath le jata hai.
- User jawab ghoor raha hota hai bina ye jaane ki wo kis cheez ke liye tha.

### Words Brand Hain
- Koi asli insaan **"Operation failed"** ya **"Invalid entry"** kabhi nahi bolta.
- **Aapke words brand ko color palette se zyada loud carry karte hain.**

## 📝 Validation Timing — Validate On Blur

### Dono Extremes Galat Hain
- ❌ **Sirf submit pe validate** → user 10 fields blind bharta hai, phir sab ek saath red — upar scroll karke dhundhna padta hai.
- ❌ **Har keystroke pe validate** → user ko **mid-word punish** karte ho — pehla letter type kiya aur "invalid email." Technically correct. **Completely cruel.**

### Sahi Rule: Blur Pe Validate
- ✅ **Field chhodne tak ruko, phir check karo.**
- User ka thought pura ho chuka hota hai — feedback **helpful land hota hai, nagging nahi.**

### Ek Baar Galat → Live Ho Jao
- Field ek baar wrong ho jaye → **use live pe switch** kar do, aur **fix hote hi error turant clear.**
- User ko maaf hone ka pata karne ke liye **dobara submit mat karwao.**

### Green Check Bhi Feedback Hai
- Field sahi hai to **confirm karo** — sirf galat flag mat karo.
- Mehnat ke baad ki **silence aisi lagti hai jaise form judge kar raha ho.**

## 👆 Swipe Gestures — Thresholds, Direction, Aur Net

### Do Thresholds Har Swipe Me
- **Chhota pull** → buttons reveal hote hain — **pause, choice.**
- **Aur aage pull** → **commit line cross** hoti hai.
- Action **release pe fire** hota hai.

### Rubber Band + Haptic Beat
- Finger ke niche row **rubber band jaisa resist** karta hai.
- Commit point pe **icon pop hota hai aur resistance mar jata hai.**
- Wo chhota haptic beat **pura interaction aapse baat karna** hai.

### Direction Ek Language Hai
- **Right = safe actions** — archive, mark as read.
- **Left = destructive.**
- Sides swap kiye to **muscle memory galat email delete** kar degi.

### Gestures Invisible Hote Hain
- Naye users unhe **akele kabhi nahi dhundhte.**
- ✅ **First launch pe pehli row peek** karo — buttons **half reveal ho, phir settle** jao.
- **Ek hint — aur pattern hamesha ke liye seekh liya jata hai.**

### Full Swipe Sirf Net Ke Saath
- Full swipe **ek motion me delete** karta hai — **bina dialog ke.**
- Ye speed **sirf net ke saath kaam karti hai**: **toast slide in — "Undo" — 5 seconds ki grace.**

## 🖲️ Context Menus — Measure, Group, Navigate

### Kholne Se Pehle Measure
- Context menu **open hone se pehle measure** karta hai.
- Niche jagah nahi → **flip up**; right me jagah nahi → **mirror left.**
- Hamesha **cursor se anchored, hamesha viewport ke andar.**

### Group By Intent
- ❌ 12 flat actions **noise** hain.
- ✅ **Intent se group karo, dividers se split.**
- **Rename duplicate ke saath**, **share copy-link ke saath**; **delete akela, bottom me, red me.**

### Hover Intent — Invisible Triangle
- Cursor drift kare to submenu **mar jata** hai — isliye Figma cursor se submenu tak ek **invisible triangle** draw karta hai.
- Us path ke andar **menu hold hota hai** — yahi **hover intent** hai.

### Power Users Aim Nahi Karte
- **Arrows list me walk** karte hain; **letters jump** karte hain — D dabao, duplicate pe pahuncho.
- **Escape ek level band karta hai — pura nahi.**

### Mobile: Same Menu, Dusra Trigger
- Mobile pe right-click nahi hota — **long press same actions ko bottom sheet me** kholta hai.
- **Ek menu system, do triggers.**

## 🌈 Color Picker System — 5 Rules

> "Pick a color. Your whole UI answers." — color select karte hi **pura UI context me update** hona chahiye, taaki decision real use me dikhe.

### Rule 1: FORMAT — Machine Nahi, Human-Readable Format
- **"Hex is for machines. OKLCH reads human."**
- HEX/RGB technical formats hain — insaan color jaisa perceive karta hai waise match nahi karte.
- ✅ **OKLCH perceptually uniform** hai — lightness adjust karo to perceived brightness **evenly** badalti hai.
- HEX, RGB, HSL, OKLCH ke beech switch milna chahiye; OKLCH se **light/dark themes consistent** bante hain aur hue/lightness tweak karne pe **muddy colors nahi** bante.

### Rule 2: MEMORY — Recent Picks One Tap Away
- **"Your last five picks. One tap away."**
- Designers brand palette aur recent experiments ke colors **baar-baar reuse** karte hain — unka track chhutna speed maarta hai.
- ✅ **Memory section**: last 5 selections + saved brand swatches — dobara eyedrop kiye bina instant reuse.

### Rule 3: CONTRAST — Ship Se Pehle Accessibility Check
- **"Bad pairs die before they ship."**
- Low contrast text **WCAG fail** karta hai — **~8% users** (color vision deficiency wale) ke liye UI padhna mushkil ho jata hai.
- ✅ Color select karte waqt **real-time contrast check**; **contrast ratio badges UI me hi** — turant dikhe ki text-on-background **AA ya AAA pass** karta hai ya nahi.

### Rule 4: ALPHA — Transparency Jhooth Bolti Hai, Dono Worlds Preview Karo
- **"Transparency lies. Preview both worlds."**
- Semi-transparent color white pe theek lag sakta hai, par dark pe **gayab ya clash** ho jata hai.
- ❌ Checkerboard preview **realistic nahi** hai.
- ✅ Transparent color ko **light aur dark dono backgrounds pe ek saath** preview karo — contrast issues **pehle pakde jaate hain.**

### Rule 5: PALETTE — Ek Pick Pura System Banaye
- **"One pick builds the system. 10 tokens • 1 decision."**
- Manual color system tedious hai — 10+ shades/tints haath se pick karna padta hai.
- ✅ Base color pick karte hi **automatic full palette**: **10 tokens — tints, shades, aur semantic colors.**
- **Ek decision se pura design system scale** — sab kuch consistent rehta hai.

## 🔐 OTP Input — Six Digits, Zero Friction

> Auth OTP input secure bhi ho aur smooth bhi — friction hatao, security rakho.

### Rule 1: Paste One Shot Me Kaam Kare
- User SMS se pura 6-digit code **ek saath paste** karna chahta hai.
- Handle nahi kiya to paste **sirf pehle box me** jata hai, ya spaces/dashes saath le aata hai.
- ✅ Non-digits strip karo (`value.replace(/\D/g, "")`), phir clean string ko **saare 6 boxes me auto-split** karo.
- *"One paste, six boxes, done."*

### Rule 2: Auto-Advance — Natural Keyboard Flow
- Digit type hote hi focus **agle box me jump** kare — manual tap ki zaroorat nahi.
- Khaali box pe **Backspace → focus pichhle box me** jump kare, taaki galti tez sudhari jaye.
- Hands keyboard pe rehte hain, manual entry fast hoti hai.

### Rule 3: One Value, Six Inputs
- ❌ Har box ki alag state variable = messy, validate karna mushkil.
- ✅ **Ek single string state** (e.g. `"847291"`) rakho; har character ko uske box me map karke render karo.
- Validation, submission, clearing — sab **bahut aasan.**

### Rule 4: Mobile Autofill
- ✅ `inputmode="numeric"` → **number pad** khulta hai.
- ✅ `autocomplete="one-time-code"` → OS (iOS 12+, Android) **SMS code keyboard ke upar suggest** karta hai.
- Ek tap → code **automatically fill** — copy/paste ki zaroorat nahi.

### Rule 5: Resend Throttle
- Resend spam → SMS provider rate limits, **429 errors**, badhte costs.
- ✅ Resend button **30 seconds ke timer ke piche lock**; **countdown dikhao**; zero hone par button **re-enable.**

### Rule 6: Visual Feedback — Clear Success vs Error
- ❌ **Wrong code** → **shake + inputs clear** — user ko turant pata chale ki fail hua, aur wo turant re-enter kar sake.
- ✅ **Correct code** → boxes **green + checkmarks** + **"Verified" badge** — instant confirmation.

### Security Note (Zaroori)
- ❌ Digit-by-digit green mat karo — attacker **code ko ek-ek digit brute-force** kar sakta hai.
- ✅ Green **sirf full verification pe** — pura input ek saath.

## 🏷️ Filter Chips — 6 Rules

### Rule 1: One Chip, Three States
- **Idle:** surface + border — tappable hai, chosen nahi.
- **Active:** teal fill + check — clearly selected.
- **Disabled:** dimmed — uske piche koi results nahi hain.

### Rule 2: Chips Kaise Combine Hote Hain
- **OR within:** ek hi category ke andar chips **OR logic** se — Color me Red OR Blue → results **expand** hote hain.
- **AND across:** alag categories ke beech **AND logic** — Color + Size dono → results **narrow** hote hain.

### Rule 3: Har Tap Ka Jawab Mile
- Har tap pe **result count turant update** ho — "Ergonomic" select kiya → 120 se 48 results.

### Rule 4: One Clear-All, Always
- Ek **"Clear all" button** jo ek tap me sab filters reset kar de.
- Button **bataye ki kitne filters remove ho rahe hain.**

### Rule 5: One Scrolling Row
- ❌ 10 chips ko **vertical wall me wrap mat** karo.
- ✅ **Horizontal scrolling row** — mobile pe space bachti hai.

### Rule 6: Active Filters Top Pe Pin
- Active filters ko **results ke top pe pin** karo.
- User ko samajh aata hai ki **list kyun shrink hui.**

## 💳 Card Number Input — 6 Rules

### Rule 1: 4-4 Ke Blocks Me Group Karo
- 16 digits ko **4-4 ke blocks** me group karo — readability ke liye.

### Rule 2: First Digit Brand Batata Hai
- Pehla digit = card brand — **'5' type karte hi Mastercard logo** dikh jaye.

### Rule 3: Caret Apni Jagah Rahe
- Auto-formatting ke waqt **caret ki position wahi rahe.**
- ❌ "Caret jumps" galat; ✅ **"Caret held"** sahi.

### Rule 4: Validate On Blur, Not Keystroke
- Validation **typing complete hone ke baad** — har keystroke pe nahi.
- Har keystroke pe "Invalid card number" **premature** hai.

### Rule 5: Pasted Junk Strip Karo
- Paste kiye text se **dashes aur non-numeric characters automatically remove** karo.

### Rule 6: Show Formatted, Store Raw
- User ko **formatted number** dikhao; backend me **raw digits** store karo.

## 🎚️ Sliders — 6 Rules

### Rule 1: Puri Row Draggable Banao
- ❌ 4px hairline track bahut chhota hai — finger se precise drag mushkil.
- ✅ **Puri row draggable** — hit area bada ho jata hai.

### Rule 2: Track Ko Fill Karo
- **Fill length hi value** dikhaye.
- ❌ "No fill" me value glance pe padhna mushkil; ✅ filled me value **fill se read** hoti hai.

### Rule 3: Steps Pe Snap
- Continuous ki jagah **discrete steps pe snap.**
- Volume, rating, price me **47.3 jaisi value kisi ko nahi chahiye.**

### Rule 4: Value Float Kare
- Drag ke waqt **current value thumb ke upar float** kare (e.g. **25%**).

### Rule 5: Range Ke Liye Two Thumbs
- Range select karne ke liye **do thumbs**; beech me **filled band.**
- Example: price range **$20–$80.**

### Rule 6: Keyboard-Se Accessible
- **Arrow keys** se step karo; **Home/End** se jump karo.

## 🫳 Drag & Drop — Grab, Drop, Recovery

### The Grab — Three Signals, One Grab
- Card hold hone par **3 signals ek saath**: **cursor change, card lift, background fade.**

### The Drop — Drop Zones Speak First
- **Blind drops se bachao**: **insertion line + column highlight** jaise visual cues pehle bolo.
- **"Snap matches structure"** — Kanban board me structured snap.
- **"Free matches canvas"** — Figma jaise canvas me free movement.
- Galat choose kiya to user **frustrated** hota hai.

### The Recovery — Bad Drop, Toast, Undo
- Accidental move ke baad **5 seconds ka Undo toast** — user ko panic se bachao.

## 🔀 Toggle Switch — 4 Rules

### Anatomy — Ratios
- **Width = 2× knob**; **padding = knob radius.**

### Transition — Snap Nahi, Morph
- **250ms ease-out** me **4 properties morph** karo: **rail color, knob slide, knob shadow, label.**

### Accessibility
- **Keyboard navigation** support; **focus rings**; screen reader ke liye **ARIA-checked.**

### Loading States — Optimistic + Rollback
- Flip karte hi **UI pehle update**; **spinner knob ke andar.**
- API fail ho → **state roll back.**

## 🔔 Notification Surfaces — Severity Picks The Surface

### Chaar Surfaces
- **Toast** — non-intrusive feedback ke liye.
- **Banner** — system-level alerts ke liye.
- **Modal** — blocking actions jisme **user input zaroori** ho.
- **Badge** — quiet persistence ke liye.

### Severity → Surface
- Trigger ki **severity decide karti hai** kaunsa surface use hoga.
- ***"The trigger picks the volume."***

### Lifecycle
- Kuch notifications **auto-dismiss** hoti hain; kuch ko **manual dismissal** chahiye.

### Stack Behavior
- ✅ Toasts **cleanly stack** ho — *"Stacked — Breathe."*
- ❌ Modals **overlap nahi** hone chahiye — *"Trainwreck."*

## 🪜 Multi-Step Forms (Wizards) — 5 Rules

### Chunking — Wall Nahi, Path
- Lambe form ki **"wall of fields"** ko steps me todo — **"path" banao.**
- Fields ko **3 ke sets** me break karo — cognitive load kam hota hai.

### Progress — Feedback Do
- **Progress indicator zaroori hai**: **linear bar, numbered dots, ya step labels.**

### Boundaries — Context Se Group Karo
- Fields ko **count se nahi, context se** group karo: **Personal, Shipping, Payment, Review.**

### Validation — Inline, Real-Time
- ❌ Final screen pe rejection nahi; ✅ **instant inline validation.**
- Error **field ke saath hi** dikhe (e.g. "Invalid format").

### State — Persist Karo
- User ka data **locally save** karo (localStorage me wizard state) — **refresh pe data loss nahi.**

## ⭐ Star Ratings — 4 Rules

### Rule 1: Hover Preview Kare
- Hover pe **potential rating dikhe — click se pehle.**
- ❌ "Reacts on click" ki jagah ✅ **"previews on hover."**

### Rule 2: Preview ≠ Committed
- **Preview layer aur committed layer alag** rakho — cursor move karne par **flickering na ho.**

### Rule 3: Round Up Karna Band Karo
- ❌ 4.4 rating ko 5 stars mat dikhao.
- ✅ **4 full stars + 1 partially filled star.**

### Rule 4: 30ms Ka Stagger — Alive Feel
- Stars ko fill karne me **30ms staggered animation** — interface **responsive aur alive** lagta hai.

## 📑 Tabs — 5 Rules

### Rule 1: Indicator — Motion + Physics
- ❌ Hard cut nahi; ✅ **smooth slide: 280ms, ease-out.**
- Sliding underline ke liye **spring physics**: `spring({ damping: 22, stiffness: 200 })`.

### Rule 2: Overflow — Bahut Saare Tabs
- ❌ Tabs ko **2 lines me wrap mat** karo.
- ✅ **Horizontal scrolling + edge fades + desktop chevrons.**

### Rule 3: Keyboard — Accessibility
- **Arrow keys, Home, End** support zaroori hai.
- **FOCUS kabhi ACTIVE jaisa nahi hona chahiye** — focus ring active state se distinct ho.

### Rule 4: Mobile
- **5 se kam tabs** → **Segmented Control.**
- **5 se zyada tabs** → **List view / bottom sheet.**
- Touch targets **≥ 44px.**

### Rule 5: Content — Transitions
- Content change pe **"Fade – Pause – Fade"** transition.
- Layout shift se bachne ke liye **container height interpolate** karo.

## 📅 Date Picker — 5 Rules

### Rule 1: Presets — 90% Use Cases
- **Today, Yesterday, Last 30 days** — majority cases **ek click me solve.**

### Rule 2: Range Highlight — Hover, Click, Drag
- Hover = **preview state** dikhao.
- Range **click & drag** se select ho.

### Rule 3: Two Months
- **Side-by-side do months** dikhao.
- **Cross-month range selection** normal hona chahiye.

### Rule 4: Keyboard
- Power users ke liye **arrow keys navigation.**
- Manual entry: **type karo → validate ho.**

### Rule 5: Mobile = Sheet
- Mobile pe **full-screen sheet** layout.
- **Vertical scrolling** se date selection.

## ⏱️ Animation Timing — 5 Secrets

### Entrance — 200–300ms
- Modal/panel entrance: **200–300ms** — yahi **sweet spot** hai.

### Exit — Entrance Se 30% Faster
- Exit animations **entrance se 30% faster**: **150–200ms.**

### Feedback — Under 100ms
- Click/hover feedback **100ms se kam** — **Doherty threshold**: interface **instant feel** hota hai.

### Attention — 500–800ms
- Error/alert jaisi attention-grabbing animations: **500–800ms.**
- **Bounce effect** eye-catching hota hai.

### Stagger — 50ms
- List items ko sequentially animate karte waqt **har item ke beech 50ms delay.**

## 🧠 Serial Position Effect — Edges Strongest Hote Hain

### Memory U-Shaped Hai
- Users **pehle aur aakhri items** sabse zyada yaad rakhte hain; **middle sabse zyada bhoolte** hain.
- Pattern: **Primacy (#1)** — Middle (#2–#8) — **Recency (#9).**

### Application: Navbars
- **Logo first position pe**, **CTA last position pe.**
- **Strongest links edges pe, weakest middle me.**

### Application: Landing Pages
- **Strongest USP top pe**, **strongest social proof bottom pe.**
- **"Don't bury the gold in the middle."**

### Application: Onboarding
- **Slide 1 = hook**; **last slide = payoff.**
- *Magic at the bookends. Filler in the middle.*

### Core Principle
- **Strongest content first rakho. Strongest content last bhi rakho.**

## 🔁 Zeigarnik Effect — Open Loops Users Ko Wapas Late Hain

### 80% Principle
- Task ko 100% complete karne ki jagah **80% pe chhodo.**
- Unfinished tasks brain me **"open loop"** banate hain jo **active memory me rehte hain.**

### Incomplete = 2x Memory Weight
- Incomplete tasks completed tasks se **2x zyada memory me hold** hote hain — user **wapas aane ke liye motivate** hota hai.

### Onboarding Checklist
- Checklist me **unchecked box** rehne se user return karta hai — *daily, sirf ek unchecked box ki wajah se.*

### Real Example — LinkedIn
- **"Profile strength 80%"** bar — user ko profile complete karne ke liye wapas bulata hai.

### Critical Catch
- Ye effect **sirf desired outcomes pe kaam karta hai** — **chores pe use karne se kaam nahi karta.**

## ⛰️ Peak-End Rule — Peak + End = Memory

### Brain Average Nahi Nikalta
- Experience ki memory = **peak intensity moment + final moment.**

### Cold Ending vs Joyful Ending
- ❌ **Cold ending** — abrupt "Done" screen. Memory rating **58/100.**
- ✅ **Joyful ending** — confetti + *"You're all set!"* Memory rating **94/100.**

### Intentional Peaks Design Karo
- Journey me **deliberate peak moments** banao — surprise upgrade, clever interactions.

### Ending Ki Power
- Same flow me sirf ending badalne se **recall +40%** badh sakta hai.
- **"One delight beats five neutrals."**

### Negative Ending Sab Ruin Kar Deti Hai
- Smooth onboarding ke baad bhi ek **negative ending** (e.g. payment failed screen) **pura experience ruin** kar deti hai.

## 🔍 Search UX — 5 Rules

### Placeholder = Onboarding
- ❌ Generic "Search" nahi; ✅ **"Search by name, SKU, or brand"** — specific likho.

### Recent — Empty State Khali Nahi Hota
- Search bar focus karne par **recent searches** dikhao.

### Autocomplete Popularity Se Rank Karo
- Suggestions ko **alphabet se nahi, clicks/popularity se** rank karo.
- Suggestions ke saath **category badges** dikhao.

### Keyboard Visible + Cues
- Keyboard focus **hamesha visible**; clear cues: **arrows navigate, Enter select, Esc close.**

### Zero Results ≠ Dead End
- ❌ "No matches" pe mat ruko; ✅ **recovery path** do — suggestions list.

## 🚨 Error States — 5 Rules

### Pattern — 4 Error Types
- Error type ke hisab se pattern match karo: **VALIDATION, NETWORK, SERVER, PERMISSION.**

### Recovery — Hamesha Exit Path
- Har error state me **exit ya recovery path** ho: **Retry, Refresh, Contact support.**

### Hierarchy — Severity Se Surface
- **INLINE → TOAST → MODAL** — severity badhne par surface badalta hai.

### Copy — Human, Machine Nahi
- ❌ "Error 500"; ✅ **"Lost connection."**

### Prevention
- Live validation se **80% errors prevent** ho sakte hain — signup me password requirements meet hote hi **field green.**

## 🧭 Navigation Patterns — Sahi Pattern Chuno

### Bottom Tabs — Mobile
- **3–5 destinations max.**
- ❌ Primary navigation ko hidden menu me mat daalo — **engagement ~40% drop** hota hai (Nielsen Norman).

### Sidebar — Desktop
- **Persistent rakho** — click-to-reveal ❌.
- ❌ Collapsed by default mat rakho.

### Hamburger — Sirf Mobile Secondary
- Hidden menu **sirf mobile pe, secondary content ke liye.**
- ⚠️ Desktop par hamburger se **engagement 56% drop** hota hai.

### Command Palette — Sirf Power Users
- Ye **shortcut hai, primary nav nahi.**
- ❌ New users ke liye primary navigation mat banao.

### Breadcrumbs — Deep Hierarchy
- Use karo jab **depth > 2** ho.
- ❌ Flat structure me breadcrumbs mat lagao.

**System Rule:** **Mobile = Tabs. Desktop = Sidebar.**

## 📝 Input Field — 6 States

### Default
- **Label outside, helper text niche.**
- ❌ Placeholder-as-label mat — typing karte hi **vanish** ho jata hai.
- Contrast **≥ 4.6:1.**

### Focus
- Ring contrast **≥ 3:1** (accessibility).

### Error
- **Color + icon + message — teeno.**
- Color-blind users ke liye **sirf color pe depend mat** raho.

### Success
- Confirmation **field ke andar hi** dikhe.
- ❌ Toast notifications pe rely mat karo.

### Disabled
- Grayscale background + `cursor: not-allowed`.
- Screen readers ke liye **visible** rahe.

### Loading
- Spinner **input ke andar** + input disable — **double-submit bug prevent.**

## 💬 Tooltips — 5 Rules

### 300ms Delay
- Tooltip **300ms delay ke baad** appear ho — accidental triggers bachte hain, **user intent confirm** hota hai.

### Arrow
- Arrow tooltip ko **trigger se clearly connect** karta hai.

### Positioning — Edge Pe Flip
- Screen edge ke paas **flip kar do taaki clipping na ho** — hamesha **viewport ke andar.**

### Dismissal — Multiple Ways
- **Mouse leave, Escape, focus out, tap outside** — sab kaam karein.

### Brevity
- Tooltip **hint hai, documentation nahi** — **max 300px**, 600px ki deewar ❌.

## 📋 Dropdowns — 5 Rules

### Clickable
- Touch targets **44–48px** + hover state ke saath proper clickability.

### Flip On Edge
- Screen ke bottom pe menu **automatically upward flip** ho — clipping prevent.

### Keyboard
- **Arrow keys** navigate; **Enter** select; **Esc** close.

### Search For 10+ Items
- 10+ items wale lists me **search** do — typing ke saath list **filter** ho.

### Animation 150ms
- Na 50ms jaisi tez, na 500ms jaisi slow — **150ms ideal.**

## ⏳ Loading Patterns — Sahi Wala Chuno

### Skeleton — Known Shape
- Known-shape layouts ke liye.
- **Wait > 300ms** ho tab hi dikhao.

### Spinner — Unknown Duration
- **< 3 seconds** ke short loads ke liye best.

### Progress Bar — Known %
- **> 3 seconds** ke file uploads me **trust build** karta hai.

### Optimistic UI — Instant Feedback
- Action **turant dikhao, fail ho to rollback** — like karte hi heart red.

### Show Nothing — Very Fast
- **200ms ka skeleton broken feel deta hai** — is case me **kuch mat dikhao.**

## 🍞 Toasts — 5 Rules

### Position
- **Desktop: bottom-right.** **Mobile: top.** Center blocking ❌.

### Timing By Severity
- **Info: 4s** auto-dismiss; **Warning: 7s**; **Error: ∞ — until acknowledged.**

### Stacking
- **Max 3 visible.** Spring physics: **damping 20, stiffness 180.**

### Dismissible
- Dismiss ke **multiple ways**; **hover pe pause** ho.

### Color Coding
- Sirf tint pe depend mat karo — **icons + borders** se differentiate karo (**~6% users** color se distinguish nahi kar paate).

## 🕳️ Empty States — 5 Rules

### Illustration > Void
- Empty screen **khali mat chhodo** — illustration use karo (*"Nothing here yet"* + box icon).

### Tone = Brand Voice
- ❌ Corporate "ERROR 404" nahi; ✅ human voice — *"Looks quiet in here."*

### Primary CTA Mandatory
- Hamesha **ek primary CTA** — e.g. *"+ Create project."*

### Context = Design
- **First run, no results, error** — har scenario ka **alag approach.**

### Empty = Onboarding
- Empty state ko **onboarding opportunity** ki tarah use karo — instructional pointers se guide karo.

## 🧱 Design System Foundations — 5 Pillars

### Colors — Semantic, Raw Nahi
- **Semantic tokens** use karo (`var(--brand)`, `var(--bg-surface)`) — raw hex values nahi.

### Typography — Intentional Hierarchy
- Scale establish karo: **48px se 20px tak**, weights aur labels defined.

### Spacing — 4px Base
- Consistent spacing: **4px unit**, scale **4px se 64px tak.**

### Components — Har State Account Me
- Har component ke **saare states design karo**: hover, active, disabled...

### Motion — Purposeful
- Sahi easing (**ease-out / ease-in-out / ease-in**) + duration standards: **100ms (micro) se 500ms (XL) tak.**

## 🦴 Skeleton Screens — 4 Secrets

### The Brain: Prediction Machine
- **Spinner anxiety create karta hai.**
- **Skeleton anticipation build karta hai** — content preview dikha kar.

### Shimmer Direction — Reading Flow
- **Left-to-right shimmer** use karo — ye **standard reading pattern se match** karta hai.

### Content-Aware Shapes
- ❌ Generic blocks = lazy design.
- ✅ **Content-aware = smart design**: avatar ke liye **circle**, text ke liye **rectangles.**
- Skeleton ki shape **actual content se match** kare.
- Perceived time: generic **2.4s** → content-aware **1.2s.**

### Optimistic UI — The Beautiful Lie
- **Instant feedback do**: user action ko **turant successful dikhao.**
- Server fail ho → **rollback karo.**

## 🌈 Gradients — 4 Rules (Sparingly Use Karo)

> Yaad rakho: gradient wahan mat lagao jahan kehne ko kuch nahi — lekin jab lagao, to sahi lagao:

### Adjacent Hues
- Color wheel pe **60° apart** colors use karo — harmonious look.
- ❌ **180° apart** colors **clash** karte hain.

### Direction — The Premium Angle
- **135° direction** use karo — better depth ke liye.

### Mesh Gradients
- Linear gradient = sirf 2 colors.
- **Mesh gradient = 3 color points** — organic transitions.

### Text Gradients
- Text pe gradient lagate waqt **readability maintain** rakho.
- **Sirf headlines pe** — statement style me.

---

## 📐 SafeAreaView — Har Screen Ka Pehla Layer

> Real app me **koi bhi content SafeAreaView ke bahar nahi hona chahiye** — notch, status bar, home indicator sab content ko khata hai.

### Rule 1: SafeAreaView Hamesha Root Pe
- **Har screen ka sabse bahar ka wrapper SafeAreaView hona chahiye.**
- ❌ Content ko direct `View` me mat daalo — **notch ke peeche chhup jayega.**
- ✅ `SafeAreaView style={{ flex: 1 }}` — **har screen ka default starting point.**

### Rule 2: Edges Define Karo
- **`edges={['top']}`** sirf top safe area chahiye to (status bar + notch protection).
- **`edges={['bottom']}`** sirf bottom chahiye (home indicator area on iPhone X+).
- **`edges={['left', 'right']}`** landscape mode me side notch/protection.
- Default `edges={['top', 'bottom']}` — **zyadatar screens ke liye ye hi chahiye.**

### Rule 3: Tab Screens Me Bottom Mat Lo
- Bottom tab navigator **khud bottom safe area handle karta hai** — screen ko `edges={['top']}` do.
- ❌ Dono taraf safe area = **tab bar ke upar extra gap** — content beech me atak jayega.

### Rule 4: Full-Screen Content (Video/Map)
- Full-screen video ya map me **SafeAreaView hatao** — content edge-to-edge chahiye.
- **Overlay controls** ko khud padding do — `Platform.OS === 'ios' ? 44 : 24` top padding.

### Rule 5: Modal Me Safe Area Alag Hai
- **Bottom sheet modals** ko sirf bottom edge chahiye — top content khud handle kare.
- **Full-screen modals** ko dono edges chahiye — normal screen jaisa.

---

## 📏 Padding & Spacing System — Consistent Spacing Har Jagah

> Real apps me **spacing ek system hai**, random numbers nahi. Ye rules follow karo:

### Left/Right Horizontal Padding = 8px Default
- **Har screen ka left/right padding minimum 8px** hona chahiye — content screen ke edge se chipke nahi hona chahiye.
- ✅ `paddingHorizontal: 8` — **standard baseline.**
- Cards, list items, sections — sab me **8px side padding consistent.**
- ❌ `paddingHorizontal: 0` — **content edge-to-edge dekhne me sasta lagta hai.**

### Content Sections Ke Liye 16px
- **Major content sections** (cards, forms, profile sections) ke liye `paddingHorizontal: 16`.
- **Sub-sections** ke andar `paddingHorizontal: 8` — **nested padding hierarchy.**

### Gap Spacing = 8px Between Items
- **List items ke beech gap = 8px** — na zyada na kam.
- ✅ `gap: 8` ya `marginVertical: 8` — **consistent breathing room.**
- **Header se content ke beech = 16px** — zyada gap lagta hai section separation.
- **Footer se content ke beech = 16px**.

### Spacing Scale (4px Base Unit)
- **4px** — tight spacing (icon se text ke beech, badge adjustments)
- **8px** — default gap (list items, horizontal padding, inline elements)
- **12px** — medium gap (card internal padding, button padding)
- **16px** — section spacing (header to content, card to card)
- **24px** — large section gap (between major sections)
- **32px** — screen sections (top margin, bottom safe area)
- **48px–64px** — hero/empty state spacing

### Negative: Kab Gap Mat Use Karo
- ❌ **List data me gap mat use karo** — **divider lines use karo** (neeche dekho).
- ❌ **Same-level elements ke beech uneven gaps** — visual rhythm toot-ta hai.
- ❌ **Gap aur padding mix mat karo** — ek parent padding do, children ko gap se space karo.

---

## ➖ List Dividers — Gap Ki Jagah Lines Use Karo

> **Jab data list ho (contacts, messages, settings, orders) — gap ki jagah divider lines use karo.** Gap list items ko disconnected banata hai; line unhe ek **connected list** banata hai.

### Rule 1: Hairline Divider = 1px, Subtle Color
- ✅ `height: 1, backgroundColor: 'rgba(0,0,0,0.08)'` — **light mode.**
- ✅ `height: 1, backgroundColor: 'rgba(255,255,255,0.08)'` — **dark mode.**
- ❌ **2px ya bold divider = overkill** — line subtle honi chahiye, loudest cheez nahi.
- ❌ **Har jagah same divider color** — dark mode me alag, light mode me alag.

### Rule 2: Divider Left Padding = Content Se Match
- Divider ka **left edge content ke left edge se aligned** hona chahiye.
- ✅ `marginLeft: 56` (avatar width 40 + 16px padding) — **avatar ke baad start ho.**
- ❌ Full-width divider jab content inset hai — **line content se disconnected lagti hai.**
- **Inset divider** = jab content me left icon/avatar ho.
- **Full-width divider** = jab content edge-to-edge ho (settings list bina icon).

### Rule 3: Last Item Pe Divider Nahi
- ❌ Last item ke baad divider — **list ka end confuse hota hai next section se.**
- ✅ `n - 1` dividers for `n` items — **last item clean end.**

### Rule 4: Group Headers Ke Baad Divider Nahi
- Section header ("Recent Orders", "Account Settings") ke baad **divider mat lagao** — header khud separator hai.
- ✅ Divider **sirf items ke beech**, **group boundaries ke baad nahi.**

### Rule 5: Divider Kahan Gap Se Better Hai
| Scenario | Gap ❌ | Divider ✅ |
|---|---|---|
| Contact list | disconnected feel | connected list |
| Settings/options | airy but loose | scannable rows |
| Order history | items float apart | timeline feel |
| Chat list | gaps break grouping | clean separation |
| Card grid/cards | ✅ gap works here | ❌ divider odd lagta hai |

### Rule 6: Divider Me Animated Transitions
- Swipe-to-delete karne pe **divider smoothly shrink** ho — **hard cut ❌.**
- New item insert hone pe **divider fade-in** — **pop-in broken lagta hai.**

---

## 🎨 Icons — Custom-Generated, Premium Quality

> ❌ **Simple FontAwesome/MaterialIcons se kaam nahi chalega** — real apps me **custom crafted icons** hote hain jo brand se match karte hain. Library icons **generic lagte hain** aur product ko **template jaisa banate hain.**

### Rule 1: Custom SVG Icons Generate Karo
- **Har icon ko SVG me manually craft karo** — perfect pixel alignment, consistent stroke width.
- ✅ **24×24 viewBox** standard — responsive scaling ke liye.
- ✅ **2px stroke width** — clean, modern look.
- ✅ **stroke-linecap: round**, **stroke-linejoin: round** — soft edges.
- ❌ `fill`-based icons **outdated lagte hain** — **outline/stroke icons modern hain.**

### Rule 2: Consistent Icon Grid
- Har icon **24×24 grid** me hona chahiye — **2px padding** inside (20×20 live area).
- **Optical alignment** > mathematical alignment — circle ko 1px bada karo taaki square jaisa lage.
- **Har icon me same visual weight** — ek patla, ek mota nahi hona chahiye.

### Rule 3: Icon Styles Jo Real Apps Use Karti Hain

#### Outline (Default)
```svg
<path d="M12 5v14M5 12h14" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
```
- **Subtle, reading mode** — navigation, secondary actions.

#### Filled (Active/Selected State)
```svg
<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2z" fill="currentColor"/>
```
- **Bold, active state** — selected tab, favorited item.

#### Duotone (Two-Tone Visual Hierarchy)
```svg
<path d="..." fill="currentColor" opacity="0.15"/>
<path d="..." stroke="currentColor" stroke-width="2"/>
```
- **Depth + hierarchy** — ek shape background me, ek foreground me.

#### Gradient Fill (Premium Feel)
```svg
<linearGradient id="grad"><stop offset="0%" stop-color="#6366F1"/><stop offset="100%" stop-color="#8B5CF6"/></linearGradient>
<path d="..." fill="url(#grad)"/>
```
- **Feature icons, achievements, rewards** — premium feel.

### Rule 4: Icon Sizes — 4 Sizes, Har Jagah Consistent
| Size | Use Case | CSS |
|---|---|---|
| **16px** | Inline text ke saath, badges, tags | `width: 16; height: 16` |
| **20px** | Buttons ke andar, input fields, list items | `width: 20; height: 20` |
| **24px** | Navigation tabs, standalone icons, toolbar | `width: 24; height: 24` |
| **32px** | Empty states, feature highlights, onboarding | `width: 32; height: 32` |

### Rule 5: Essential App Icons — Ye Har Real App Me Hote Hain

#### Navigation & Actions
- **Home** — house outline with chimney detail
- **Search** — magnifying glass with subtle depth (not just a circle + line)
- **Bell/Notification** — bell with small dot indicator capability
- **User/Profile** — person silhouette with subtle shoulders
- **Settings/Gear** — gear with 6 teeth, not 8 (cleaner)
- **Back Arrow** — chevron-left with proper curve, not straight line
- **Close/X** — rotated 45° cross, not just two lines
- **Menu/Hamburger** — 3 lines with rounded caps, 16px total height

#### Content & Media
- **Heart/Favorite** — organic shape, not geometric; filled state me proper red
- **Star/Rating** — 5-point star with proper inner radius; partial fill support
- **Bookmark** — bookmark with folded bottom corner detail
- **Share** — iOS style (box + arrow up) ya Android style (3 dots connected)
- **Camera** — camera body + lens circle + flash indicator
- **Image/Photo** — landscape frame with mountain + sun
- **Play** — triangle with proper proportions (not equilateral — wider base)
- **Pause** — two vertical bars, equal width, proper spacing

#### Communication
- **Chat/Bubble** — speech bubble with rounded tail
- **Mail/Envelope** — envelope with V-fold lines
- **Phone** — phone with subtle curve (not just rectangle)
- **Send/Paper Plane** — folded paper plane, not just arrow
- **Attachment/Paperclip** — curved paperclip with proper loops

#### Status & Feedback
- **Check/Circle** — checkmark inside circle (success)
- **Warning/Triangle** — triangle with exclamation (warning)
- **Error/X-Circle** — X inside circle (error)
- **Info/Circle-i** — i inside circle (info)
- **Loading/Spinner** — circular arc, animated rotation
- **Download** — arrow down + horizontal line (tray)
- **Upload** — arrow up + horizontal line (tray)
- **Refresh** — two curved arrows forming circle

#### E-Commerce Specific
- **Cart/Bag** — shopping bag with handles
- **Tag/Price** — price tag with string
- **Wallet** — wallet with card slot detail
- **Delivery/Truck** — delivery truck side view
- **Filter/Sliders** — 3 horizontal sliders at different positions
- **Sort** — 3 horizontal lines decreasing in width
- **Grid View** — 2×2 grid of squares
- **List View** — 3 rows with circle + line

### Rule 6: Icon Colors — Semantic, Not Decorative
- ✅ `color: theme.colors.text.secondary` — **default icon color = secondary text.**
- ✅ `color: theme.colors.primary` — **active/selected state.**
- ✅ `color: theme.colors.error` — **destructive action icons.**
- ❌ **Har icon alag color** — rainbow effect, koi meaning nahi.
- ❌ **Decorative colors** (pink camera, blue search) — **icons functional hain, decoration nahi.**

### Rule 7: Icon + Text Pairing
- **Icon aur text ke beech 8px gap** — na zyada na kam.
- **Icon size = text line-height ka ~75%** — icon text se chhota hona chahiye.
- **Vertical center alignment** — icon aur text ka **optical center** match hona chahiye.
- ✅ `alignItems: 'center', gap: 8` — **consistent icon-text pairs.**

### Rule 8: Animated Icons — Micro-Interactions
- **Tab switch** pe icon **outline → filled morph** (200ms ease-out).
- **Like/Heart** pe icon **scale bounce** (1.0 → 1.3 → 1.0, 300ms).
- **Notification bell** pe **swing animation** (rotate ±15°, 2 cycles, 400ms).
- **Download** pe **arrow bounce down** (translateY +4px → 0, 200ms).
- **Error shake** — icon **translateX ±4px**, 3 cycles, 300ms.
- ❌ **Har icon pe animation** — **sirf meaningful interactions pe.**

---

## 📱 Real App Screen Architecture

> Real apps me **har screen ka ek consistent structure** hota hai. Ye template follow karo:

### Screen Anatomy
```
┌─────────────────────────┐
│     SafeAreaView (top)  │  ← Status bar + notch protection
├─────────────────────────┤
│     Header/NavBar       │  ← Screen title, back button, actions
│     paddingHorizontal: 16│
├─────────────────────────┤
│                         │
│     Content Area        │  ← Main content with paddingHorizontal: 8
│     flex: 1             │
│                         │
├─────────────────────────┤
│     Footer/Tab Bar      │  ← Bottom actions or tab navigation
│     SafeAreaView (bottom)│
└─────────────────────────┘
```

### Header Component Rules
- **Height: 56px** (Android) / **44px + safe area** (iOS).
- **Left: Back button** (if not root screen) — **24px icon, 44px hit area.**
- **Center: Title** — **single line, semibold, centered.**
- **Right: Action icons** — max 2 icons with **8px gap** between them.
- **Shadow/border-bottom**: `borderBottomWidth: 1, borderBottomColor: 'rgba(0,0,0,0.06)'`.
- ❌ **Title left-aligned jab center me space hai** — **centered feels premium.**

### Content Area Rules
- **`flex: 1`** — content area baaki space le.
- **`paddingHorizontal: 8`** — baseline side padding.
- **Keyboard-aware**: `KeyboardAvoidingView` wrap karo jab input fields ho.
- **Scrollable content**: `ScrollView` ya `FlatList` with `contentContainerStyle={{ paddingBottom: 24 }}`.

### Bottom Actions / Floating Buttons
- **FAB (Floating Action Button)**: **56×56px, right-bottom, 16px margin** from edges.
- **Bottom bar**: **height 56px + safe area**, with `paddingHorizontal: 8`.
- **Sticky footer** (like "Place Order" button): `position: 'absolute', bottom: 0`.

---

## 📋 Real List Patterns — Contacts, Orders, Settings

> Real apps me lists **data-rich** hote hain — sirf title nahi, **subtitle, metadata, actions, status** sab hota hai.

### Contact/User List Item
```
┌──────────────────────────────────────────┐ paddingHorizontal: 8
│ ┌──────┐                                 │
│ │Avatar│  Name (Semibold 16px)           │ ← 8px gap avatar → text
│ │ 40px │  Last message preview (14px, muted)│
│ └──────┘                                 │
│──────────────────────────────────────────│ ← 1px divider, marginLeft: 56
│ ┌──────┐                                 │
│ │Avatar│  Name (Semibold 16px)           │
│ │ 40px │  Last message preview (14px, muted)│
│ └──────┘                                 │
└──────────────────────────────────────────┘
```

### Settings/Options List Item
```
┌──────────────────────────────────────────┐ paddingHorizontal: 8
│ [Icon 24px]  Setting Name        [>]     │ ← 8px gap icon → text
│──────────────────────────────────────────│ ← 1px divider, marginLeft: 48
│ [Icon 24px]  Setting Name        [>]     │
│──────────────────────────────────────────│ ← 1px divider, marginLeft: 48
│ [Icon 24px]  Setting Name        [Toggle]│
└──────────────────────────────────────────┘
```

### Order/Transaction List Item
```
┌──────────────────────────────────────────┐ paddingHorizontal: 8
│ Order #28491              ₹2,499         │ ← Title left, amount right
│ 3 items • 12 Oct 2025     [Delivered]    │ ← Metadata left, status badge right
│──────────────────────────────────────────│ ← 1px divider
│ Order #28490              ₹899           │
│ 1 item • 10 Oct 2025     [In Transit]    │
└──────────────────────────────────────────┘
```

### Notification List Item
```
┌──────────────────────────────────────────┐ paddingHorizontal: 8
│ ●  [Icon]  Notification Title    2m ago  │ ← Bold dot = unread, relative time
│──────────────────────────────────────────│ ← 1px divider
│    [Icon]  Notification Title    1h ago  │ ← No dot = read
│──────────────────────────────────────────│ ← 1px divider
│ ●  [Icon]  Notification Title    3h ago  │
└──────────────────────────────────────────┘
```

---

## 🃏 Real Card Patterns

> Cards **containers** hain — content-rich, **not just title + image.**

### Product Card
```
┌─────────────────────┐ borderRadius: 12
│ ┌─────────────────┐ │
│ │                 │ │ ← Image, borderTopRadius: 12
│ │    [Product     │ │
│ │     Image]      │ │
│ │                 │ │
│ └─────────────────┘ │
│                     │ padding: 12
│ Product Name        │ fontSize: 14, fontWeight: 600
│ Brand Name          │ fontSize: 12, color: muted
│                     │
│ ₹1,299  ₹2,499     │ Price: bold + strikethrough old
│ ★★★★☆ (128)       │ Rating: star icons + count
│                     │
│ [Add to Cart]       │ Button: fullWidth, height: 40
└─────────────────────┘
```

### Profile Card
```
┌─────────────────────────────┐ borderRadius: 12, padding: 16
│  ┌────────┐                 │
│  │Avatar  │  Name           │ ← 56px avatar + text
│  │  56px  │  @username      │
│  └────────┘  Bio text here  │
│                             │
│  ┌────────┬────────┬──────┐ │ ← Stats row
│  │  1.2k  │  489   │  67  │ │
│  │ Posts  │  Likes │Saved │ │
│  └────────┴────────┴──────┘ │
│                             │
│  [Follow]  [Message]        │ ← Action buttons, gap: 8
└─────────────────────────────┘
```

### Summary/Stats Card
```
┌─────────────────────────────┐ borderRadius: 12, padding: 16
│  [Icon]   Total Revenue     │ ← Icon + Label
│           ₹2,45,890         │ Large number, tabular-nums
│           ↑ 12.5% vs last   │ Trend indicator + color
│                             │
│  ━━━━━━━━━━━━━━━━━━━━━━━━━  │ ← Mini chart/sparkline
│  Mon  Tue  Wed  Thu  Fri    │
└─────────────────────────────┘
```

---

## 🔍 Real Search Implementation

> Search sirf input box nahi hai — **poora experience hai.**

### Search Bar Component
```
┌──────────────────────────────────────────┐ paddingHorizontal: 8
│  🔍  Search products, brands...    [×]  │ ← 40px height, 12px border radius
│──────────────────────────────────────────│ ← 1px divider
│                                          │
│  Recent Searches                         │ ← Section header, semibold
│  ─────────────────────────────────────── │ ← divider
│  🕐  wireless headphones                 │ ← Recent item with clock icon
│  ─────────────────────────────────────── │ ← divider
│  🕐  running shoes nike                  │
│  ─────────────────────────────────────── │ ← divider
│                                          │
│  Trending                                │ ← Section header
│  ─────────────────────────────────────── │ ← divider
│  🔥  iPhone 16 cases                     │ ← Trending with fire icon
│  ─────────────────────────────────────── │ ← divider
│  🔥  winter jackets                      │
└──────────────────────────────────────────┘
```

### Search Results Count + Active Filters
- **Results header**: `"248 results for \"wireless headphones\""` — **paddingHorizontal: 8.**
- **Active filter chips**: horizontal scroll row, **gap: 8**, with **clear all** button.
- **Sort bar**: `"Sort by: Relevance ▼"` — right-aligned, tappable.

---

## 👤 Real Profile Screen

> Profile screens **content-heavy** hote hain — real app me ye sab hota hai:

### Profile Screen Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│  ←  Profile                    [⚙️][✏️] │ Header: paddingHorizontal: 16
├──────────────────────────────────────────┤
│                                          │
│            ┌──────────┐                  │
│            │  Avatar  │                  │ 80px avatar, centered
│            │   80px   │                  │
│            └──────────┘                  │
│                                          │
│          Deepak Sharma                   │ Name: 20px, semibold, centered
│          @deepak7480                     │ Username: 14px, muted, centered
│                                          │
│    ┌────────┬────────┬────────┐          │ Stats row: gap 16px
│    │  1.2k  │  489   │  67   │          │
│    │ Posts  │Followers│Following│         │
│    └────────┴────────┴────────┘          │
│                                          │
│    Full-stack developer & designer       │ Bio: 14px, centered
│    Building beautiful experiences        │
│                                          │
│    [Edit Profile]  [Share Profile]       │ Action buttons, gap: 8
│                                          │ paddingHorizontal: 16
├──────────────────────────────────────────┤ ← 8px gap
│                                          │
│  ┌──┬──┬──┬──┐                          │ Tab bar: Posts | Saved | Tagged
│  │○ │○ │○ │○ │                          │ paddingHorizontal: 8
│  └──┴──┴──┴──┘                          │
│  ┌──┬──┬──┐                              │ Grid: 3 columns, gap: 2px
│  │  │  │  │                              │
│  └──┴──┴──┘                              │
│  ┌──┬──┬──┐                              │
│  │  │  │  │                              │
│  └──┴──┴──┘                              │
└──────────────────────────────────────────┘
```

---

## 🏠 Real Home/Dashboard Screen

> Home screen **content-dense** hota hai — real app me ye sab hota hai:

### Home Screen Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│  Good morning, Deepak!        [🔔][👤]  │ Header: paddingHorizontal: 16
│──────────────────────────────────────────│ ← divider
│                                          │
│  🔍  Search anything...                  │ Search bar: paddingHorizontal: 8
│                                          │
│  ┌────────────────────────────────┐      │ Banner/Carousel
│  │                                │      │ paddingHorizontal: 8
│  │     [Promotional Banner]       │      │ borderRadius: 12
│  │     50% OFF — Limited Time     │      │ height: 160
│  │                                │      │
│  └────────────────────────────────┘      │
│      ● ○ ○ ○                             │ Page dots: centered
│                                          │
│  Quick Actions              [See all →]  │ Section header: paddingHorizontal: 8
│  ┌────────────────────────────────┐      │
│  │ [📦]   [💳]   [📊]   [⚙️]    │      │ Horizontal scroll, gap: 8
│  │ Orders Wallet Stats Settings   │      │ Each: 72×72, borderRadius: 12
│  └────────────────────────────────┘      │
│                                          │
│  Recent Orders              [See all →]  │ Section header: paddingHorizontal: 8
│  ┌────────────────────────────────┐      │
│  │ Order #28491        ₹2,499     │      │ paddingHorizontal: 8
│  │ 3 items • Delivered ✅         │      │
│  │────────────────────────────────│      │ ← divider
│  │ Order #28490          ₹899     │      │
│  │ 1 item • In Transit 🚚        │      │
│  │────────────────────────────────│      │ ← divider
│  │ Order #28485        ₹4,199     │      │
│  │ 5 items • Processing ⏳        │      │
│  └────────────────────────────────┘      │
│                                          │
│  Recommended For You        [See all →]  │ Section header: paddingHorizontal: 8
│  ┌──────────┐  ┌──────────┐             │ Horizontal scroll, gap: 8
│  │ [Image]  │  │ [Image]  │             │ paddingHorizontal: 8
│  │ Product  │  │ Product  │             │
│  │ ₹1,299   │  │ ₹899     │             │
│  └──────────┘  └──────────┘             │
└──────────────────────────────────────────┘
│  [🏠]  [🔍]  [🛒]  [👤]               │ Bottom Tab Bar
└──────────────────────────────────────────┘
```

---

## 🛒 Real Cart/Checkout Screen

> Cart screens **data-dense + action-oriented** hain:

### Cart Screen Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│  ←  My Cart (3 items)         [🗑️]     │ Header: paddingHorizontal: 16
├──────────────────────────────────────────┤
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 8
│  │ ┌────────┐                     │      │
│  │ │        │  Product Name       │      │
│  │ │ [Img]  │  Size: M, Color: Blk│      │
│  │ │ 72×72  │                     │      │
│  │ └────────┘  ₹1,299            │      │
│  │              [-] 2 [+]         │      │ Quantity stepper
│  │────────────────────────────────│      │ ← divider
│  │ ┌────────┐                     │      │
│  │ │        │  Product Name 2     │      │
│  │ │ [Img]  │  Size: L, Color: Red│      │
│  │ │ 72×72  │                     │      │
│  │ └────────┘  ₹899              │      │
│  │              [-] 1 [+]         │      │
│  └────────────────────────────────┘      │
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 8
│  │ Apply Coupon            [→]    │      │ Tappable row
│  │────────────────────────────────│      │ ← divider
│  │ 🎫  SAVE20 applied      [×]   │      │ Applied coupon
│  └────────────────────────────────┘      │
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 8
│  │ Subtotal               ₹2,198 │      │
│  │ Discount               -₹399  │      │ Green text
│  │ Delivery               FREE   │      │ Green text
│  │────────────────────────────────│      │ ← divider (bold)
│  │ Total                  ₹1,799 │      │ Bold, 18px
│  └────────────────────────────────┘      │
│                                          │
│  ┌────────────────────────────────┐      │ Sticky bottom
│  │       [ Place Order ₹1,799 ]  │      │ paddingHorizontal: 8
│  └────────────────────────────────┘      │ SafeAreaView bottom
└──────────────────────────────────────────┘
```

---

## 📊 Real Form Screen — Registration/Checkout

> Forms **field-rich** hote hain — real app me proper grouping aur validation:

### Registration Form Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│  ←  Create Account             [Skip]   │ Header: paddingHorizontal: 16
├──────────────────────────────────────────┤
│                                          │
│  Personal Details                        │ Section header: paddingHorizontal: 16
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 8
│  │ First Name *                   │      │ Label: outside, semibold
│  │ ┌────────────────────────────┐ │      │
│  │ │ Deepak                     │ │      │ Input: height 48, borderRadius: 8
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ Last Name *                    │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ Sharma                     │ │      │
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ Email *                        │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ deepak@email.com     ✅   │ │      │ Success state: green check
│  │ └────────────────────────────┘ │      │
│  │ ✓ Looks good!                  │      │ Helper text: green
│  │                                │      │
│  │ Phone Number *                 │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ 🇮🇳 +91  │ 98765 43210    │ │      │ Country code + number
│  │ └────────────────────────────┘ │      │
│  └────────────────────────────────┘      │
│                                          │
│  Address                                 │ Section header: paddingHorizontal: 16
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 8
│  │ Street Address *               │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ 123 MG Road               │ │      │
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ ┌──────────────┬─────────────┐ │      │ Two columns, gap: 8
│  │ │ City *       │ State *     │ │      │
│  │ │ ┌──────────┐ │ ┌─────────┐ │ │      │
│  │ │ │ Mumbai   │ │ │ MH      │ │ │      │
│  │ │ └──────────┘ │ └─────────┘ │ │      │
│  │ └──────────────┴─────────────┘ │      │
│  │                                │      │
│  │ PIN Code *                     │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ 400001                     │ │      │
│  │ └────────────────────────────┘ │      │
│  └────────────────────────────────┘      │
│                                          │
│  ┌────────────────────────────────┐      │ Sticky bottom
│  │       [ Continue to Payment ]  │      │ paddingHorizontal: 16
│  └────────────────────────────────┘      │ SafeAreaView bottom
└──────────────────────────────────────────┘
```

---

## 💬 Real Chat/Messaging Screen

> Chat screens **message-dense** hote hain — proper spacing, grouping, timestamps:

### Chat Screen Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│  ←  [Avatar] Deepak Sharma     [📞][⋮]  │ Header: paddingHorizontal: 16
├──────────────────────────────────────────┤
│                                          │
│         ──── Today, 2:30 PM ────        │ Date divider: centered
│                                          │
│  ┌──────────────────────────────┐        │ padding: 12
│  │ Hey! How's the project?     │        │ borderRadius: 16, borderBottomLeft: 4
│  │                      2:31 PM │        │ Time: 11px, muted
│  └──────────────────────────────┘        │ maxWidth: 75%
│                                          │
│       ┌──────────────────────────────┐   │ Self message: right-aligned
│       │ Going great! Just finished   │   │ backgroundColor: primary
│       │ the design system updates.   │   │ textColor: white
│       │                     2:32 PM  │   │
│       └──────────────────────────────┘   │
│                                          │
│  ┌──────────────────────────────┐        │
│  │ That's awesome! Can you      │        │ Same sender, 2min = group
│  │ share the latest mockups?    │        │ 4px gap within group
│  │                      2:32 PM │        │
│  └──────────────────────────────┘        │
│                                          │
│       ┌──────────────────────────────┐   │
│       │ Sure, sending now...         │   │
│       │                     2:33 PM  │   │
│       └──────────────────────────────┘   │
│       ┌──────────────────────────────┐   │
│       │ 📎 design-v3-final.fig      │   │ Attachment: above text
│       │                     2:33 PM  │   │
│       └──────────────────────────────┘   │
│                                          │
│  ┌──┐                                   │ Typing indicator: with avatar
│  │A │  ● ● ●                            │ 3 dots animated
│  └──┘                                   │
│                                          │
├──────────────────────────────────────────┤
│  ┌──────────────────────────────────┐    │ Composer: paddingHorizontal: 8
│  │ [+]  Type a message...    [📤]  │    │ 44px height, grows to 5 lines
│  └──────────────────────────────────┘    │ SafeAreaView bottom
└──────────────────────────────────────────┘
```

---

## 🔐 Real Auth Screens — Login, Signup, Forgot Password

### Login Screen Layout
```
┌──────────────────────────────────────────┐ SafeAreaView
│                                          │
│            [App Logo 64px]               │ Centered, 48px top margin
│                                          │
│          Welcome Back!                   │ 24px, semibold, centered
│    Sign in to continue to your account   │ 14px, muted, centered
│                                          │
│  ┌────────────────────────────────┐      │ paddingHorizontal: 16
│  │                                │      │
│  │ Email or Phone                 │      │ Label: outside
│  │ ┌────────────────────────────┐ │      │
│  │ │ 📧  deepak@email.com      │ │      │ Leading icon + input
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ Password                       │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │ 🔒  ••••••••          👁️ │ │      │ Trailing eye icon toggle
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ Forgot Password?               │      │ Right-aligned link
│  │                                │      │
│  │ ┌────────────────────────────┐ │      │
│  │ │       [ Sign In ]          │ │      │ Full-width button, 48px height
│  │ └────────────────────────────┘ │      │
│  │                                │      │
│  │ ──── Or continue with ────    │      │ Divider with text
│  │                                │      │
│  │ [G] [f] [🍎]                  │      │ Social login buttons, gap: 12
│  │                                │      │
│  └────────────────────────────────┘      │
│                                          │
│  Don't have an account?  Sign Up         │ Bottom text: centered
│                                          │
└──────────────────────────────────────────┘
```

---

## 📱 Tab Bar — Bottom Navigation

> Real apps ka tab bar **not just icons** — ye poora navigation system hai:

### Tab Bar Anatomy
```
┌──────────────────────────────────────────┐
│  [🏠]    [🔍]    [🛒]    [👤]          │ height: 56px + safe area
│  Home    Search   Cart    Profile        │ paddingHorizontal: 8
│  ━━━━                                    │ Active: filled icon + primary color
│  ●                                       │ Badge: top-right of icon
└──────────────────────────────────────────┘
```

### Tab Bar Rules
- **3–5 tabs maximum** — zyada tabs = decision paralysis.
- **Active tab**: filled icon + primary color + semibold label.
- **Inactive tab**: outline icon + muted color + regular label.
- **Badge position**: top-right corner of icon, **red background, white text.**
- **Tab label**: 10px, single word preferred.
- **Safe area**: bottom safe area automatically handled.
- **Translucent background**: `backgroundColor: 'rgba(255,255,255,0.95)'` with `backdrop-filter: blur(20px)`.
- **Top border**: `borderTopWidth: 0.5, borderTopColor: 'rgba(0,0,0,0.1)'`.

---

## 🎭 Theming & Dark Mode — Real Implementation

### Theme Token System
```javascript
const theme = {
  colors: {
    // Backgrounds
    bg: {
      primary: '#FFFFFF',      // Main background
      secondary: '#F5F5F5',    // Card/section background
      tertiary: '#EBEBEB',     // Elevated surfaces
    },
    // Text
    text: {
      primary: '#1A1A1A',      // Headlines, primary content
      secondary: '#666666',    // Subtitles, descriptions
      muted: '#999999',        // Timestamps, placeholders
      inverse: '#FFFFFF',      // Text on dark/colored backgrounds
    },
    // Brand
    brand: {
      primary: '#6366F1',      // Primary actions, links
      secondary: '#8B5CF6',    // Secondary actions
      light: '#EEF2FF',        // Light tint backgrounds
    },
    // Semantic
    semantic: {
      success: '#10B981',      // Success states, confirmations
      warning: '#F59E0B',      // Warning states, caution
      error: '#EF4444',        // Error states, destructive
      info: '#3B82F6',         // Informational states
    },
    // Borders & Dividers
    border: {
      default: 'rgba(0,0,0,0.08)',
      strong: 'rgba(0,0,0,0.15)',
      divider: 'rgba(0,0,0,0.06)',
    }
  },
  dark: {
    // Same structure, dark values
    bg: {
      primary: '#121212',
      secondary: '#1E1E1E',
      tertiary: '#2C2C2C',
    },
    text: {
      primary: '#E5E5E5',
      secondary: '#A0A0A0',
      muted: '#6B6B6B',
      inverse: '#121212',
    },
    border: {
      default: 'rgba(255,255,255,0.08)',
      strong: 'rgba(255,255,255,0.15)',
      divider: 'rgba(255,255,255,0.06)',
    }
  }
};
```

### Dark Mode Specific Rules
- **Har color ka dark variant hona chahiye** — sirf invert mat karo.
- **Elevation = lightness** — upar ki surface lighter.
- **Text opacity**: Primary 87%, Secondary 60%, Disabled 38%.
- **Images**: brightness 90% in dark mode — **100% brightness glare karta hai.**
- **Dividers**: `rgba(255,255,255,0.08)` — alpha-based, not fixed gray.

---

