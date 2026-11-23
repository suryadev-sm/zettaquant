# 1. Algo trading kya hai

Algo trading ka matlab hai **pehle se tay rules ya model ke hisaab se trade karna**, mood ya emotion se nahi. Rule kuch bhi ho sakta hai: "Nifty pehle 15 minute ka high tode to buy" se lekar 100 features wala machine learning model tak.

## Sahi kram

```
Idea → Backtest → Walk-forward test → Paper trading → Bahut chhota live → Dheere dheere badhana
```

1. **Idea:** koi pattern jo aapko lagta hai kaam karega.
2. **Backtest:** purane data par check karna ki rule ne kya kiya hota.
3. **Walk-forward:** aise data par test jo model ne kabhi nahi dekha ([Lesson 3](03-walk-forward.md)).
4. **Paper trading:** asli market mein, asli time par, bina paise ke.
5. **Chhota live:** itna kam paisa ki galti sasti pade.

Zyada log seedha live paisa lagate hain aur beech ke teen kadam chhod dete hain. Sabse badi galti yahi hai.

## Algo ka asli fayda

- Rules har baar ek jaise follow hote hain, darr ya lalach beech mein nahi aata.
- Har trade ka record rehta hai, isliye pata chalta hai ki kya kaam kar raha hai.
- Ek saath bahut saare stocks par nazar rakh sakte hain.

## Jo algo nahi kar sakta

Algo kharab idea ko acha nahi bana sakta. Agar rule mein edge nahi hai, to algo sirf tezi se paisa ganwayega.

➡️ Agla: [Backtest ke 3 jaal](02-backtest-ke-jaal.md)
