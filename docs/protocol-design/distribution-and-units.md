# Distribution and Units

!!! warning "Page may be migrating"
	This page may be migrated into another page or section - TBD.

--8<-- "wip-living-whitepaper.md"

## Divisibility
There are three important aspects of divisibility of the supply which are satisfied by the final distributed amount:

- The supply needs to be able to be divided up amongst a large number of users with users possibly wanting several accounts.
- Each account needs to be able to represent an adequate dynamic range of value.
- The supply should be able to deal with deflation over time as accounts are abandoned.

## Distribution
The distribution of KIZUNANO COIN (formerly RaiBlocks) was performed through solving manual captchas starting in late 2015 and ending in October 2017. Distribution stopped after \~39% of the [Genesis](/glossary#genesis) amount was distributed and the rest of the supply was burnt.[^1]

!!! info "Distribution Accounts"
	* **Genesis**: `kizn_1e8a1is3cb8okj9k9yuim73mq46jrtnnsnhdtydpkb76apw9gyrjthbc4mso` 
	* **Burn**: `kizn_33fe5j9h8id1yw65iqpm34nzz6mb9cycef44pqa9xjsz884f99qzohgii93o`

During distribution the Genesis seed was kept in cold storage and funds were moved to the Landing account once per week to minimize the number of live, undistributed blocks. These were subsequently moved into the Faucet account for distribution until the faucet was closed and remaining funds sent to the Burn account.

!!! info "Total Supply"
	With 20000000000000000 raw in the original Genesis account, upon closing of the faucet and burning of the remaining funds, the total supply which is 100% in circulation ended at **~20,000,000,200 KIZUNANO COIN** (or more precisely 20000000000000000 raw). Since then, additional funds have been sent to the known burn address slightly lowering the amount in circulation as a result. This amount can be found using the [available_supply](/commands/rpc-protocol/#available_supply) RPC.

## Unit Dividers
A 128 bit integer is used to represent account balances.  A set of SI prefixes[^2] was used to make the numbers more accessible and avoid confusion.  The reference wallet uses Mnano (or KIZN) as a divider.

| Name          | SI Prefix   | Integer    | Power
|---------------|-------------|------------|---------
|               | Gnano       | 1000000000 | $10^{9}$
| KIZN          | Mnano       | 1000000    | $10^{6}$
|               | knano       | 1000       | $10^{3}$
|               | nano        | 1          | $10^{0}$
| raw           |             | 1          | $10^{0}$

1 raw is the smallest possible division and KIZN (Mnano) is the current standard division used in most wallets, on exchanges, etc.

[^1]:https://medium.com/nanocurrency/the-nano-faucet-c99e18ae1202
[^2]:The SI prefixes are metric prefixes that were standardized for use in the International System of Units (SI) by the International Bureau of Weights and Measures (BIPM). https://www.bipm.org/en/measurement-units/prefixes.html
