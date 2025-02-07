# sd-boost-delegation-twavp

This strategy is used by Stake DAO to vote with sdToken using Time Weigthed Averaged Voting Power (TWAVP) system and adapted for veSDT boost delegation.

```
VotingPower(user) = veToken.balanceOf(liquidLocker) * (average.sdTokenGauge.working_balances(user) / sdTokenGauge.working_supply)
```

>_sampleSize: in days_
>_sampleStep:  the number of block for `average` calculation (max 5)_
>_avgBlockTime: in seconds_

Here is an example of parameters:

```json
{
  "veToken": "0x5f3b5DfEb7B28CDbD7FAba78963EE202a494e2A2",
  "liquidLocker": "0x52f541764E6e90eeBc5c21Ff570De0e2D63766B6",
  "sdTokenGauge": "0x7f50786A0b15723D741727882ee99a0BF34e3466",
  "symbol": "sdToken",
  "decimals": 18,
  "sampleSize": 30,
  "sampleStep": 5,
  "avgBlockTime": 12.0
}
```