
---
# Portfolio Manager

##Goals:

PMGR hopes to someday be a desktop/mobile personal portfolio manager. The goals it to be able to create a portfolio Idea with specific allocations assigned to various ETFs or stocks, etc. 

- [ ] Allow for one or more brokerage APIs to be integrated
- [ ] Allow for one or more data providers to be integrated
- [ ] Create portfolios with specific allocations (Ideas)
- [ ] Invest into an Idea throug the interface.
- [ ] Monitor implemented Ideas through a dashboard
- [ ] An overall portfolio analysis
- [ ] Basic stock/ETF research
- [ ] Basic portfolio analysis
- [ ] Portfolio Rebalancing (Automatic? Manual?)

## Maybes
- [ ] Electron 
- [ ] CouchDB syncing 
- [ ] Mobile version
- [ ] Multi-user/Account separation

Having a desktop version is one goal although I haven't gone through all of the options available. I expect to reduce some overhead using Svelte but not sure what overhead Electron (or similar) might bring. 

One idea is to use something like RxDB to allow for local storage/modification and then sync up with a remote database (CouchDB) sitting on a desktop when there are multiple client applications needing to share data.

A third idea is to allow for "multi-user" separation - so the UI/portfolio is segmented into separate boxes. 


## Get started



