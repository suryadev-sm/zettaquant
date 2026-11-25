<p align="center">
  <img src="logo.png" width="140" alt="ZettaQuant logo">
</p>

<h1 align="center">ZettaQuant: Algo Trading Research (India)</h1>

<p align="center">
  <a href="https://t.me/ZettaQuant"><img src="https://img.shields.io/badge/Telegram-Channel%20join%20karein-26A5E4?logo=telegram&logoColor=white" alt="Telegram channel"></a>
  <a href="https://t.me/ZettaQuantBot?start=github"><img src="https://img.shields.io/badge/Bot-@ZettaQuantBot-2CA5E0?logo=telegram&logoColor=white" alt="Telegram bot"></a>
  <img src="https://img.shields.io/badge/Market-NSE%20%7C%20Nifty-0B1426" alt="NSE">
  <img src="https://img.shields.io/badge/Mode-Paper%20trading-20E0AA" alt="Paper trading">
</p>

Hum Indian market (NSE stocks, Nifty options) ke liye **algo trading models khud banate aur test karte hain**, aur har model ka result yahan khul kar dikhate hain: **profit wale bhi aur loss wale bhi.**

> ❌ Koi buy/sell tips nahi · ❌ Koi "sure shot" calls nahi · ❌ Koi guaranteed return nahi
> ✅ Sirf research, data aur seekh

---

## 📊 Live paper trading results

Ye table har raat hamare server se **apne aap update** hota hai. Har trade ki poori detail (stock/option, lot, entry, exit, P&L) trade band hone ke baad [Telegram channel](https://t.me/ZettaQuant) par aati hai.

<!--RESULTS-->
| Model | Shuru | Value | Shuru se P&L | Benchmark | Aakhri din |
|---|---|---|---|---|---|
| **Combo factor (swing)**<br><sub>Momentum + 52-week high + low volatility, top 20 stocks, har 20 din rebalance</sub> | 29 Oct 2026 | ₹10,91,536 | 🟢 +₹91,536 (+9.15%) | +5.46% | +₹14,139 (25 Nov) |
| **ML v3 (swing)**<br><sub>LightGBM ensemble, top 20 stocks, har 20 din rebalance</sub> | 30 Oct 2026 | ₹10,45,210 | 🟢 +₹45,210 (+4.52%) | +6.08% | +₹1,727 (25 Nov) |
| **ML v7 (swing)**<br><sub>ML + sector/macro features, top 20 stocks, risk rules</sub> | 30 Oct 2026 | ₹10,47,292 | 🟢 +₹47,292 (+4.73%) | +5.45% | -₹9,321 (23 Nov) |
| **Iron condor (Nifty)**<br><sub>Nifty weekly options, far wings, stop loss 2x</sub> | 02 Nov 2026 | ₹3,02,242 | 🟢 +₹2,242 (+0.75%) | — | +₹0 (23 Nov) |
| **Intraday v2**<br><sub>9:30 entry, 3:00 PM exit, 2 long + 2 short stocks</sub> | 11 Nov 2026 | ₹1,93,468 | 🔴 -₹6,532 (-3.27%) | — | -₹5,676 (23 Nov) |
| **Challenger c20261112**<br><sub>Intraday v2 jaisa, har mahine retrain</sub> | 12 Nov 2026 | ₹1,96,824 | 🔴 -₹3,176 (-1.59%) | — | -₹1,823 (23 Nov) |
| **Nifty Agent (options)**<br><sub>Nifty/BankNifty option buying, kai arms, AI news filter</sub> | 30 Oct 2026 | ₹61,557 | 🟢 +₹11,557 (+23.11%) | — | -₹11,107 (25 Nov) |

**Sab models milakar, shuru se: +₹1,88,129**

<sub>Data: 25 Nov 2026 tak · Paper trading, asli paisa nahi</sub>
<!--/RESULTS-->

**Benchmark** ka matlab hai unhi stocks mein barabar paisa lagakar baithe rehna. Model tabhi kaam ka hai jab wo cost ke baad benchmark ko hara sake.

---

## 🧪 Ab tak kya test kiya (aur kya fail hua)

Zyada log sirf jeetne wali strategies dikhate hain. Hum sab dikhate hain, kyunki asli seekh fail hone wali strategies se hi milti hai.

| Model | Result | Kyun |
|---|---|---|
| ML v1 (5-din target) | ❌ Fail | Walk-forward mein -1.9% CAGR |
| Combo factor (momentum + 52w high + low vol) | 📝 Paper | Dev mein 12.1% CAGR, hold-out kamzor |
| ML v3 (LightGBM ensemble) | 📝 Paper | Dev mein 16.9% CAGR, Sharpe 0.80 |
| Batch test: 3,420 strategies | ❌ Fail | Koi bhi luck threshold paar nahi kar payi |
| Intraday v2 (395 stocks) | 📝 Paper (sirf record) | Backtest acha, par patle (illiquid) stocks mein |
| Intraday v2, sirf top-100 liquid stocks | ❌ Fail | Sharpe -0.32 |
| Nifty weekly iron condor | 📝 Paper | +6.3% CAGR, Sharpe 0.69 |
| Max (stocks intraday) | ❌ Fail | Kamai 14.5 bps < cost 16 bps |
| Scalp (Nifty 1-min) | ❌ Fail | Kamai ~3 bps prati trade < cost 7 bps |
| Swing (2-10 din hold) | ❌ Fail | Cost ke baad positive, par benchmark se peeche |

---

## 📚 Seekhiye (free, Hinglish mein)

1. [Algo trading kya hai](lessons/01-algo-trading-kya-hai.md)
2. [Backtest ke 3 jaal](lessons/02-backtest-ke-jaal.md)
3. [Walk-forward test](lessons/03-walk-forward.md)
4. [Cost sab kuch hai](lessons/04-cost.md)
5. [Risk management](lessons/05-risk-management.md)
6. [Tip channel kaise parkhein](lessons/06-tip-channel-kaise-parkhein.md)

Naye lessons aur research notes pehle [Telegram channel](https://t.me/ZettaQuant) par aate hain.

---

## 🤝 Judiye

- 📢 **Channel:** [t.me/ZettaQuant](https://t.me/ZettaQuant): trade results, daily model reports, weekly report, lessons
- 🌐 **Website:** [quant.zettasphere.in](https://quant.zettasphere.in): live results ek page par
- 🤖 **Bot:** [@ZettaQuantBot](https://t.me/ZettaQuantBot?start=github): account, lessons, research notes, support
- ⭐ Ye repo useful laga to **Star** kar dijiye, taaki aur log bhi dekh sakein.

---

## ⚠️ Disclaimer

- ZettaQuant SEBI registered Research Analyst ya Investment Adviser **nahi** hai.
- Yahan koi buy/sell recommendation nahi di jaati. Sab kuch sirf education aur research ke liye hai.
- Saare results **paper trading** ke hain (asli paisa nahi). Past results future ki guarantee nahi hain.
- Trading mein paisa doob sakta hai. Faisla apna khud lijiye.
- Hum kabhi aapka broker ID, password, OTP ya PIN nahi maangte.

<sub>© ZettaSphere Technologies · <a href="https://zettasphere.in">zettasphere.in</a></sub>
