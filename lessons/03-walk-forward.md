# 3. Walk-forward test

Model ko purane data par train karo, phir **aage ke aise data par test karo jo usne kabhi nahi dekha.** Phir window aage khiskao aur dohrao.

```
Train: 2015-2017  →  Test: 2018
Train: 2016-2018  →  Test: 2019
Train: 2017-2019  →  Test: 2020
...
```

Saare test saalon ko jodkar jo result banta hai, wahi model ki asli taaqat ke kareeb hota hai.

## Hold-out: sabse zaroori niyam

Sabse naya hissa (jaise 2024-2026) **bilkul alag rakho.** Saari research khatam hone ke baad use **sirf ek baar** chalao.

Agar hold-out ko baar baar dekhoge aur model badalte rahoge, to wo bhi dheere dheere "train" ho jata hai aur uska matlab khatam ho jata hai.

**Hamara example:** hamare swing models dev period (2012-2023) mein benchmark se aage the. 2024-26 ke hold-out mein sab benchmark se peeche aaye. Isliye humne unhe asli paisa nahi diya, sirf paper par record ke liye chala rahe hain.

➡️ Agla: [Cost sab kuch hai](04-cost.md)
