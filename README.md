<img src="banner.png" alt="ventry - onchain vibecoding" width="100%">

<p>
<img src="https://img.shields.io/badge/solana-14F195?style=flat-square&logo=solana&logoColor=000" alt="solana">
<img src="https://img.shields.io/badge/rust-000?style=flat-square&logo=rust&logoColor=fff" alt="rust">
<img src="https://img.shields.io/badge/python-3776AB?style=flat-square&logo=python&logoColor=fff" alt="python">
<img src="https://img.shields.io/badge/helius-0a0e14?style=flat-square" alt="helius">
<img src="https://img.shields.io/badge/jito-0a0e14?style=flat-square" alt="jito">
<img src="https://img.shields.io/badge/yellowstone_gRPC-0a0e14?style=flat-square" alt="yellowstone">
<a href="https://x.com/ventry089"><img src="https://img.shields.io/badge/@ventry089-000?style=flat-square&logo=x&logoColor=fff" alt="x"></a>
</p>

I spent two months pointing instruments at Solana instead of trading it.

Then I took every rule the niche repeats, and tested it.

---

### what the data says

**the fee is not the lever**

```
fastest wallets on pump.fun     0.0002 SOL per buy
what I paid                     0.002  SOL per buy
result                          they land 5x earlier
```

Ten times the fee, five times slower. Their edge is physical position, not money.

**the leader decides, and you cannot pay around it**

```
BAM Europe          17-22 ms     30 of 126 wallets under 30 ms
FD Europe           16-24 ms
JitoLabs Europe     25-28 ms
Harmonic Europe     36-40 ms     nobody under 30
terminal sniper    120-750 ms
```

Same chain, same code on your side, a 4-8x spread. Since 8 October every Harmonic
leader in Europe sits at ~137 ms **regardless of what you pay**.

**one missing instruction costs you rank**

```
no SetLoadedAccountsDataSizeLimit
  -> default 64 MiB
  -> 8 CU per 32 KiB
  -> 16,384 CU of pure penalty
```

And a pump.fun buy already drags **13,040,978 bytes** through the loader, of which
10,485,760 is the program itself, sitting at the 10 MiB ceiling an account cannot pass.

**eight rules everyone repeats are noise**

Pulled every numeric threshold from 631 videos across 268 channels, tested each on
1,148 of my own tokens. Base rate: 18% reach 2x within an hour.

| the rule | channels saying it | measured |
|---|---:|---|
| top-10 holders under 30% | 43 | 18% vs 18% |
| bundle over 20% is a red flag | 51 | slightly reversed |
| insiders over 10% | 51 | 18% vs 15%, noise |
| dev holds under 5% | 34 | no difference |
| duplicate image means scam | - | 23% vs 17%, slightly better |

The one signal that survived is the one they call a red flag. **Fresh wallets: 23% vs 11%,
p = 0.007**, same sign across all five market-cap buckets.

---

### open

**[leader-radar](https://github.com/ventry08/leader-radar)** - which validator client holds the ledger right now, and what that does to your transaction. No deps, no key.

```
  holding the ledger   Jito  (JitoLabs)
  how it orders you    rank formula + block engine auction every 50ms
  fastest bots land    25-28 ms
```

More coming: the rank-cost measurements, and 15 entry signals tested against 1,148 tokens with base rates.

### writing

- buying a memecoin moves 13 megabytes: inside the speed race `soon`
- seven rules that are noise: the niche's checklist, measured `soon`

---

### method

```
every claim ships with the file, the line, and the date it was measured
results that do not survive a multiple-comparisons correction are labelled as such
vendor numbers are labelled as vendor numbers, not measurements
```

None of this made me money. That is the point: most of what gets sold as edge does not
survive a base rate.

**no signals. no calls. no paid group.**

<sub>measurements from September and October 2026, nodes in Frankfurt and Amsterdam.
Solana infrastructure moves fast - Jito proved it on 5 September, Harmonic on 8 October.</sub>
