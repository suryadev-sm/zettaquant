# 2. Backtest ke 3 jaal

Backtest mein sab kuch acha dikhna bahut aasaan hai. Ye teen galtiyan sabse aam hain.

## 1. Lookahead bias

Aisa data use karna jo us waqt pata hi nahi tha.

**Example:** din ke close price se signal banana, aur trade usi din ke open par lena. Asli zindagi mein subah 9:15 par shaam ka close kisi ko pata nahi hota.

**Bachav:** har signal ke saath likho ki wo kis time tak ke data se bana, aur trade usse **baad** ke price par lo.

## 2. Survivorship bias

Sirf aaj ke bache hue stocks par test karna. Jo companies doob gayi ya index se bahar ho gayi, wo data se gayab hain, isliye result zarurat se zyada acha dikhta hai.

**Bachav:** har din ke liye us din ki stock list use karo (point-in-time universe), aaj ki list nahi.

## 3. Overfitting

Itne saare versions try karna ki koi ek luck se acha dikh jaye.

**Hamara example:** humne 3,420 strategies ek saath test ki. Kuch ka Sharpe acha dikha, par itne trials ke hisaab se luck ki seema (deflated Sharpe) se upar ek bhi nahi gayi. Isliye saari reject ki.

**Bachav:**
- Test se **pehle** pass/fail rules likh lo.
- Ginti rakho ki kitne versions try kiye.
- Ek data ka hissa (hold-out) bilkul alag rakho aur use sirf ek baar dekho.

➡️ Agla: [Walk-forward test](03-walk-forward.md)
