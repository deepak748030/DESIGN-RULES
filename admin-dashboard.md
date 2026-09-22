# Admin Dashboard — System Prompt Rules

> AI-generated UI ko real human-like best UI banane ke liye Admin Dashboard specific guidelines.

## 🎯 AI-Look Khatam Karna — 5 Tells & Fixes

> Dashboard "AI-generated" lagta hai kyunki ye 5 galtiyan hoti hain. Har tell ka ek fix hai:

### Tell 1: Gradient Overuse
- ❌ **Tell:** Purple-to-blue gradient har jagah — header, button, chart fill. Generated UI wahan gradient lagata hai jahan uske paas kehne ke liye kuch nahi hota.
- ✅ **Fix:** Sirf **ek flat accent color** use karo — tab color ka kuch matlab banta hai.

### Tell 2: Icons in Pastel Tiles
- ❌ **Tell:** Har card pe alag pastel tile — blue, green, purple, orange. Chaar numbers ke liye chaar colors **decoration hai, information nahi.**
- ✅ **Fix:** Tiles hata do — **number hi hero hai.**

### Tell 3: Identical Cards / No Hierarchy
- ❌ **Tell:** Chaar ek-jaise cards — same size, same weight, same green badge. Bina hierarchy ka dashboard sirf **padding wala spreadsheet** hai.
- ✅ **Fix:** **Ek primary metric bada**, teen secondary chhote. User ki aankh **sirf ek jagah land honi chahiye.**

### Tell 4: 16px Radius + Drop Shadow on Everything
- ❌ **Tell:** Har cheez pe 16px corners aur drop shadow — cards, inputs, badges, chart. Jab **har card float karta hai, to koi bhi card float nahi karta.**
- ✅ **Fix:**
  - **Hairline borders** use karo (shadow ki jagah).
  - Chhote components pe **tighter border-radius.**
  - Shadow **sirf un elements pe jo page ke upar khulte hain** (modals, dropdowns, popovers).

### Tell 5: Placeholder Copy & Shapeless Numbers
- ❌ **Tell:** "Welcome back, Jordan 👋" jaisi generic copy, aur "+12.5% from last month" bina context ke — placeholder copy aur bina shape ke numbers.
- ✅ **Fix:**
  - **Period ko naam do** (exact date range/context batao).
  - **Tabular digits** use karo (numbers align rehte hain).
  - Badge ki jagah **sparkline** dikhao.

> Source: UX Engine ("kills the AI look" series)

## 📤 File Upload Flow — Feedback, Progress & Retry

### File Upload — Drop Zone Reaction
- Jab user file drag karke over kare aur **kuch react na ho** → UI broken feel hoti hai, users hesitate karte hain.
- Ek version broken lagta hai, dusra safe — farq sirf **feedback** ka hai.
- Drop zone ko **answer back karna chahiye** — drop se pehle **3 signals**:
  1. **Border** change
  2. **Glow**
  3. **Copy shift** (text badalna, e.g. "Drop to upload")

### File Upload — Honest Progress
- ❌ Spinner **sach chhupata hai** — use mat karo.
- ✅ **Percent dikhao** (e.g. 47%).
- ✅ **Time left dikhao** (e.g. ~12s remaining).
- **Honest progress** user ko decide karne deta hai — **wait kare ya walk away.**

### File Upload — Failure & Retry
- Upload aksar **90% pe marta hai** — user ko **dobara start mat karwao.**
- **Inline retry** do — file already loaded rehti hai.
- **Ek tap me upload resume** ho jana chahiye.

### File Upload — File Identity Feedback
- **Sirf file name feedback nahi hai.**
- Dikhao: **thumbnail + file type + size.**
- Ye **visual proof** hai ki sahi file receive hui hai.

### File Upload — Multiple Files
- Agar **10 files ek saath** upload ho rahi hain, to **har file ka apna progress aur apna retry** ho.
- **Ek file ki failure baaki 9 ko kabhi block nahi karni chahiye.**

> Source: UX engineering series (upload flow)

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

## 📅 Weekly Calendar View — 6 Layout Rules

> 1 week, 40 events, zero overlap — ye 6 layout rules week view ko ek glance me readable banate hain:

### Rule 1: Grid Structure & "Now"
- **7 columns, 24 rows** — har row = 1 hour.
- Hour labels **line pe baithte hain, cell ke andar nahi.**
- Ek **red line "now" mark** karti hai.
- View open hote hi **us red line tak scrolled** khulti hai — **midnight pe nahi.**

### Rule 2: Color Per Calendar
- Event ke left me **3px color stripe**, aur fill sirf **10% opacity** pe.
- Title **har color pe readable** rehna chahiye.
- ❌ Full fills ek busy week ko **rainbow** bana dete hain.

### Rule 3: Overlap = Side-by-Side, Kabhi Stack Nahi
- Same hour me **2 events** → side-by-side, **half width** each.
- **3 events** → **third width** each.
- Events ko **kabhi stack mat karo**, aur **"+1" ke piche kabhi chhupao mat.**

### Rule 4: Height = Duration
- **1 hour = 60px** — height hamesha duration represent kare.
- **15-minute event** me bhi title **single line pe clipped** dikhe.
- Usse bhi chhote events ke liye: ek **bar jo hover pe expand/visible** ho.

### Rule 5: Direct Manipulation (Drag & Resize)
- **Empty space pe drag** karo → event draw hota hai.
- **15-minute snap** rakho.
- Event ko **body se move** karo; **resize sirf bottom edge** se ho.
- Time label **drag ke dauran live update** ho — drag ke baad nahi.

### Rule 6: All-Day Events Pinned Row Me
- All-day events grid ke **upar ek pinned row** me rehte hain.
- Wo **kabhi morning ka space nahi khaate.**
- Hours scroll karo — **pinned row apni jagah stay karti hai.**

**Yaad rakho:** 6 rules → ek week jo ek glance me read ho jata hai.

> Source: UX Engine ("kills the AI look" series — calendar layouts)

## 💎 Linear-Style Polish — 5 Decisions

> Linear "expensive" kyu lagta hai? Ye 5 decisions — kisi designer ki zaroorat nahi:

### Decision 1: Density
- **13px text**, **32px rows**, letter-spacing **−1% pulled in.**
- Ek hi screen pe **dugne issues** dikhte hain — **no scroll.**
- **Density confidence ki tarah read hoti hai.**

### Decision 2: No Shadows — Flat & Engineered
- ❌ Koi shadow nahi.
- ✅ Sirf **1px border at 8% white.**
- Depth **3 background values** se aati hai — **blur se nahi.**
- Hover pe **surface value change** hoti hai — **elevation nahi.**
- Flat surfaces **engineered** lagti hain; shadows **decorated** lagti hain.

### Decision 3: One Color Only
- **Ek hi color — indigo** — sirf **selected row** aur **primary button** pe. Kahin aur nahi.
- **Status ek icon hai, colored pill nahi.**
- Baaki sab kuch **gray** me baithta hai.

### Decision 4: Shortcuts & Instant Feedback
- **Har action apna shortcut dikhata hai** — `C` = create, `⌘K` = search.
- Hover feedback **80ms** me.
- Transitions **150ms se kam.**
- **No bounce, no overshoot.**
- UI **gesture khatam hone se pehle hi jawab** deta hai.

### Decision 5: 4px Grid & Alignment
- Sab kuch **4px grid** pe.
- **16px icons** text pe centered.
- **Labels left**, **numbers right** — **kuch bhi centered nahi.**
- Alignment sahi ho to **invisible** hota hai; galat ho to **loud.**

**Yaad rakho:** 5 decisions → UI jo deliberate aur premium lagti hai.

> Source: UX Engine ("kills the AI look" series — Linear-style polish)

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

## 📊 Tables — Spreadsheet Se Product Tak, 6 Decisions

> Table default me "disguised spreadsheet" hoti hai. Ye 6 decisions use product-grade banate hain:

### Decision 1: Alignment — Numbers Right, Text Left
- ❌ Amounts centered → digits kabhi align nahi hote, **aankh compare nahi kar paati.**
- ✅ **Numbers right-aligned + tabular figures on**; **text left-aligned.**
- Tab amounts ki column ek **receipt jaisi readable** lagti hai.

### Decision 2: No Zebra Stripes
- ❌ Zebra stripes content se **fight** karte hain — har dusri row bekar me scream karti hai.
- ✅ Rows ke beech sirf **ek hairline.**
- ✅ **Hover jis row pe ho, wahi light** ho.
- Stripes **sirf wide rows pe** apni jagah banate hain.

### Decision 3: Row Height Ek Decision Hai, Padding Nahi
- **Compact = 40px**, **Default = 48px**, **Comfortable = 56px.**
- **Teen modes, ek toggle** — dense ops ke liye, airy review ke liye.

### Decision 4: Pinning — Context Kabhi Screen Chhod Ke Na Jaye
- 12 columns me se screen sirf 6 dikhati hai → right scroll pe **row ka naam kho jata hai.**
- ✅ **First column pin** karo.
- ✅ Vertical scroll pe **header pin** karo.
- **Context kabhi screen se bahar nahi jana chahiye.**

### Decision 5: Empty Cells & Overflow
- Khali cell ek sawal hai — *missing? zero? loading?* → **dash (–) use karo.**
- Lamba text wrap hoke **row explode** karta hai → **truncate karo, hover pe tooltip.**
- **Numbers kabhi truncate nahi hote.**

### Decision 6: Actions — Har Row Pe Action Column Noise Hai
- ❌ 50 rows = 50 pencils — har row pe action icons mat rakho.
- ✅ Actions **hover ya focus pe reveal** ho.
- ✅ **Touch devices pe kebab menu** do.
- ✅ **Sort arrow sirf active column pe** dikhao.

> Source: UI systems series (dashboard tables)
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

## ↔️ Resizable Panels — Divider & Drag Rules

> Layout tab tak theek lagta hai jab tak divider ko drag karke screen se bahar na kar do:

### Grab Target vs Visible Divider
- Divider visible **1px** ho, lekin **grab target 12px** hona chahiye — miss hua to resize stuck feel hota hai.

### Min/Max Clamp
- Har drag ko **min aur max width ke beech clamp** karo — panel kabhi aisi state me collapse nahi hona chahiye jise dobara khola na ja sake.
- **Limits hi feature hai.**

### Edge Ke Paas Fully Snap
- Edge ke paas **pura closed snap** karo — sliver mat chhodo.
- Halfway states **bug jaisi** lagti hain — **open ya shut, commit karo.**

### Drag Ke Waqt Invisible Overlay
- Drag ke dauran **pure page pe invisible overlay** daalo — warna iframe ya text selection mouse kha jata hai aur panel beech me freeze ho jata hai.

### Resize Cursor Puri Body Pe
- Resize cursor **sirf handle pe nahi, puri body pe** set karo — ek pixel drift pe arrow flicker nahi hona chahiye.

### Width Reloads Ke Beech Yaad Rakho
- **Width ko reloads ke across remember** karo — warna user ne jo layout haath se set kiya, use phek rahe ho.

> Source: designmotionhq.com (UI systems — resizable panels)



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

## ☑️ Table Selection — Tri-State Checkbox System

### Header Checkbox Ke Teen States
- Header box tick karo → **saari 247 rows saath aati hain.**
- Header checkbox ke **3 states hote hain, 2 nahi**: **checked, empty, partial.**
- Partial state hataoge to users **track kho denge** ki unhone kya select kiya tha.
- Partial box pe click → **sab select ho, kabhi clear nahi.**

### "Select All" Number Bol Ke Kahe
- "Select all" screen ki **6 rows** pakadta hai, lekin table me **247** hain.
- ✅ Label **number bol ke kahe**: *"Select all 247 matching."*
- Filter number badalta hai → **label use live read kare.**

### Shift-Click Range
- **Shift-click range select** karta hai — har desktop user isko expect karta hai.

### Selection App State Me Rahe
- User page change kare → selection **marni nahi chahiye.**
- **Selection app state me rehti hai — visible rows me nahi.**

### Bulk Delete: Confirm Modal Nahi, Undo
- 247 rows delete karne ke liye **confirm modal ki zaroorat nahi.**
- ✅ Count **button ke andar echo** karo, run karo, phir **10 seconds ka undo** do.
- **Reversible beats careful.**

## ⚙️ Settings Page — Ek System Ki Tarah

### Blast Radius Ke Hisaab Se Model
- Toggles **instant apply** hote hain — flip, done.
- Identity fields nahi hote → unhe **save bar + cancel** mile.
- **Model ko blast radius se match karo.**

### Task Se Group Karo, Phone Book Mat Banao
- ❌ Ek list me 40 settings = **phone book.**
- ✅ **Task se group karo**; **advanced ko ek click ke piche chhupao.**
- Stripe job se split karta hai: **Payments, Billing, Team.**

### Power Users Search Karte Hain
- Power users **kabhi scroll nahi karte — search karte hain.**
- Ek input **3 levels deep dabi setting** bhi dhundh le — **match highlight karo, path dikhao.**

### Har Change Visible + Resettable
- Har changed setting pe **ek dot aur ek reset** dikhe (VS Code har override ko colored bar se mark karta hai).
- Jab **undo ek click dur** ho, tabhi users experiment karte hain.

### Destructive Actions Quarantine Me
- **Red border, page ke bottom me.**
- Delete ke liye **pehle naam type** karna pade — **button tab tak dead rahe jab tak naam match na ho.**

## 🏗️ "Database-Shaped" Interfaces — AI Ki Sabse Badi Galti

### Problem
- **12 columns, schema ka har field**, har row me delete edit ke bagal me.
- **No empty state, no loading state** — ek misclick aur disaster.

### Fix Process
- Pehle pucho: **ye page kaun use karta hai**, aur **unki sabse buri galti kya ho sakti hai.**
  - Example: support team ki worst mistake = galat account delete → **delete type-to-confirm ke piche** chala jata hai.
- **Search primary action** ban jati hai.
- **12 nahi, 5 columns.**

### Code Se Pehle Har State Spec Karo
- **Loading, empty, error, success, offline, partial** — code likhne se pehle har state spec karo.
- **Skeleton final layout se match** kare.

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

## 🖱️ Multiplayer Collaboration — Cursors, Presence, Locks

### Interpolation — Glide, Teleport Nahi
- Server **second me 10 positions** bhejta hai; screen **60 draw** karti hai.
- **Interpolation gaps bharta hai** — cursors teleport ki jagah **glide** karte hain.

### Identity = Hashed Color
- Har user ka color **uske ID se hash** hota hai — **same person, same color, har session.**
- Aisi identity jo **aankh ke kone se track** ho sake.

### Presence Bolne Se Pehle Dikhe
- **Avatars stack** hote hain kisi ke bolne se pehle — **3 faces, phir +5 counter.**
- Naam padhne se pehle hi **room feel hota hai.**

### Locks Conflict Paida Hone Se Pehle Rokte Hain
- Sarah card grab karti hai → wo **uske color me glow** karta hai, **locked.**
- Do log ek shape edit karein = **corrupted shape.**
- **Lock conflict ko exist hone se pehle hi rok deta hai.**

### Follow Mode
- Avatar pe click → **aapka viewport unka follow** karta hai; unke pans/zooms **live.**
- **Screen share ke bina design review.**

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

## ⌨️ Command Palette (⌘K) — 7 Rules

> Power users mouse chhue bina kuch bhi kar sakein — yahi command palette ka pura maksad hai.

### Rule 1: Core Shortcut — ⌘K
- **⌘K "jump anywhere" ka universal mental model** hai.
- Ek shortcut — koi bhi action run karo, kahin bhi navigate karo, settings badlo — **menus me click kiye bina.**

### Rule 2: Fuzzy Matching — Typos Bhi Chalne Chahiye
- **"stg → Settings"** — users exact naam yaad nahi rakhte.
- "stg", "set", "settins" — sab **Settings ko top result** dikhayein.
- ❌ Strict substring search nahi; ✅ **partial matches score karo**, aur **relevance + recent usage** se prioritize karo.

### Rule 3: Results Group Karo — Flat List Nahi
- ❌ 100 items ki flat list **overwhelming aur slow to scan** hai.
- ✅ Results ko categories me todo: **Recent, Actions, Pages, Settings.**
- Structure + context → user **visually scan karke sahi section me jaldi** jump karta hai.

### Rule 4: Hands Off The Mouse — Full Keyboard Navigation
- **↑/↓ arrows** se move, **Enter** se execute, **Escape** se dismiss.
- Command palette ka pura point **speed** hai — mouse tak pahunche to **fayda gaya.**
- **Focus palette se kabhi bahar nahi jana chahiye** jab tak user exit na kare.

### Rule 5: Empty State — Blank Void Nahi
- ❌ Khali search box jo kuch na dikhaye = **broken feel, zero guidance.**
- ✅ Search khali ho to **Recent Commands** dikhao — **instant value + shortcut history.**

### Rule 6: Async Commands — UI Freeze Nahi
- Kuch commands API call karte hain — "Deploy to production", "Fetch users."
- ❌ Screen freeze hui to users ko **crash** lagta hai.
- ✅ Action chalte waqt **result row me inline spinner**; **palette khula rakho** — user ko pata rahe ki kaam chal raha hai.

### Rule 7: Nested Commands — Drill-Down Support
- Kuch actions ke sub-actions hote hain: **"Change Theme → Dark / Light / System".**
- Nested command pe Enter → palette me **naya level push** ho.
- **Escape ek level piche jaye — pura palette band nahi kare.**

**Philosophy:** *"Hands off the mouse"* — jo palette sirf search box nahi, **professional tool** banata hai, wo yahi hai. Ye pattern un har SaaS/dashboard ke liye zaroori hai jahan **50+ actions** hon aur menus bahut deep ho jate hon.

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

## 📄 Pagination — Data Badle To Bhi Na Toote

### OFFSET Ka Problem: Duplicates
- OFFSET pagination = X rows skip karo, Y rows lo.
- User page 1 pe hai aur **top pe nayi row insert** ho gayi → sab kuch **ek position shift** ho jata hai.
- Jo item #10 pe tha wo #11 ban gaya → **page 2 pe dobara dikhta hai.**
- User ko **same item do baar** dikha = data pe trust toot gaya.

### Fix: CURSOR Pagination — Stable List
- OFFSET ki jagah **unique cursor** (record ka ID ya timestamp) use karo: *"ID=12345 ke baad ke next 10 items."*
- Nayi rows insert hone se **existing IDs ki position nahi badalti** — data kuch bhi kare, **user ki jagah stable** rehti hai.

### Teen Patterns — User Intent Se Chuno
- **Numbered** — kisi bhi page pe jump (*"10,000 rows → page 500 ek jump me"*). Data-heavy tables ke liye best. ⚠️ Total row count chahiye; massive datasets pe slow (andar se abhi bhi OFFSET).
- **Load More** — *user control me rehta hai.* Product catalogs, search results ke liye best. Koi unexpected jump/shift nahi — user khud next batch trigger karta hai.
- **Infinite Scroll** — feeds/exploration ke liye best (social, news). ⚠️ Specific position **bookmark/share nahi** kar sakte; browser back/forward messy ho jata hai.

### 500 Links Render Mat Karo
- ❌ 500 pages ke 500 numbers = overwhelming UI + performance hit.
- ✅ **Ellipsis se truncate** karo — lekin **pehla aur aakhri page hamesha clickable**, taaki orientation bani rahe.

### Back Pe Scroll Restore
- Row 247 ke item me jaake back dabao → user **row 247 pe hi land ho — top pe nahi.**
- Scroll position kho jana data-heavy apps ke **sabse frustrating UX bugs** me se ek hai.

### State URL Me Rahe
- **Current page, active filters, sort order** — sab **URL query params** me reflect ho.
- Page 500 ek **shareable link** ban jata hai; bookmark/refresh pe **same view**; browser back/forward **expected behave** karta hai.

**Summary:** Specific page pe jump chahiye → **Numbered** (dynamic data ke saath cursor logic pair karo). Control ke saath browsing → **Load More**. Endless exploration → **Infinite Scroll**. Aur hamesha: **list stable rakho, scroll preserve karo, state URL me rakho.**

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

## 📈 Charts — Honest Data-Viz Ke 5 Rules

### Rule 1: Bar Charts Zero Se Start Hote Hain — No Exceptions
- ❌ Y-axis ko zero se upar start karne se **chhote differences exaggerated** lagte hain — +4% increase **+400% jaisa** dikhta hai.
- ✅ Bar charts **hamesha zero se start.**

### Rule 2: Form Ko Question Se Match Karo
- **Comparison** ke liye → **bar chart.**
- **Trend** dikhane ke liye → **line chart.**
- ❌ Bahut zyada slices wale **pie charts avoid** karo.

### Rule 3: Color Meaning Encode Karta Hai
- **Color encoding hai, decoration nahi** — grouping ya highlighting ke liye functional tool ki tarah use karo.
- ❌ Sirf decoration ke liye zyada colors mat lagao.

### Rule 4: Jo Data Nahi Hai, Use Strip Karo
- **Data-ink ratio: har pixel data serve kare.**
- ❌ Heavy gridlines, 3D effects = **chartjunk** — remove karo.

### Rule 5: Aspect Ratio — Slope Ko 45° Bank Karo
- Line chart ki slope ko **~45 degrees** pe bank karo — change **visually sahi perceive** hota hai.
- ❌ Squashed ya tall chart **data ki story badal deta hai.**

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
