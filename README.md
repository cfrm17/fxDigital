# FX Digital Option Valuation


1.	Cash Settlement

This pays off nothing if the option is out of the money and pays a fixed amount, Q (in Base Currency – usually USD), if it ends up in the money at the maturity of the option. Let   be the forward exchange rate between the valuation date and the maturity of the option.   is the volatility of the forward exchange rate. Let also   be the time to maturity (settlement) date,  the strike price of the option, and   the continuously compounded risk-free rate of the base currency at time t. Using Black’s model, the prices of call and put options are given by 

 	 			(1)

where  ,    (1 or –1) is the call/put indicator, and   is the discount factor between the valuation date and the settlement date. 

2.	Asset Settlement

This pays off nothing if the option is out of the money and pays an amount equal to   (called Principal % Strike in Atlas) if it ends up in the money at the maturity of the option. Here,   is the FX rate at the maturity of the option. Thus, the prices of call and put options are given by

 			(2)

where  .

3.	Atlas System

In Atlas, the payoff currency is the base currency, which is usually USD. 

For direct quote, we have   and  . The dollar value Delta in USD (called USD Delta) is computed as

USD Delta                                         (3)

where   is the spot exchange rate and the perturbation on the spot rate   is set to be 0.00005. This dollar value delta is used for daily hedging. 

	For indirect quote, we have   and  . The price of the contract and the perturbation of the spot rate in delta calculation is in USD/CAD. Thus, the perturbation of the spot is done as   and   where  . Thus, the USD Delta is defined by

USD Delta =                                          (4)


We created 24 test cases for FX Digital option (12 for direct quote and 12 for indirect quote) and the following tables summarize the results. The valuation date is September 1, 2004 for direct quote and August 31, 2004 for indirect quote.  The principal amount, Q, is 1,000,000 USD for both direct / indirect quotes. The same principal applies to other securities or derivatives, such as bond (see https://finpricing.com/lib/FiZeroBond.html)

	Direct Quote:
	Base Currency: USD
	Underlying Currency: EUR
	Principal Amount: 1,000,000 USD
	Spot Rate: 1.20605 USD/EUR

	Indirect Quote:
	Base Currency: USD
	Underlying Currency: CAD
	Principal Amount: 1,000,000 USD
	Spot Rate: 1.31895 CAD/USD

Appendix 1. Test Cases (Direct Quote)

Case No.	Digital Type	Option Type	Maturity Date	Settlement Date	Strike Price
1	Cash	Call	31-Dec-2004	04-Jan-2005	1.200
2	Cash	Put	31-Dec-2004	04-Jan-2005	1.200
3	Cash	Call	01-Sep-2005	06-Sep-2005	1.150
4	Cash	Put	01-Sep-2005	06-Sep-2005	1.210
5	Cash	Call	15-Aug-2006	17-Aug-2006	1.170
6	Cash	Put	15-Aug-2006	17-Aug-2006	1.208
7	Asset	Call	31-Dec-2004	04-Jan-2005	1.187
8	Asset	Put	31-Dec-2004	04-Jan-2005	1.208
9	Asset	Call	01-Sep-2005	06-Sep-2005	1.200
10	Asset	Put	01-Sep-2005	06-Sep-2005	1.200
11	Asset	Call	10-Jul-2006	12-Jul-2006	1.185
12	Asset	Put	10-Jul-2006	12-Jul-2006	1.205


Appendix 2. Test Cases (Indirect Quote)

Case No.	Digital Type	Option Type	Maturity Date	Settlement Date	Strike Price
1	Cash	Call	31-Dec-2004	04-Jan-2005	1.300
2	Cash	Put	31-Dec-2004	04-Jan-2005	1.300
3	Cash	Call	01-Sep-2005	02-Sep-2005	1.307
4	Cash	Put	01-Sep-2005	02-Sep-2005	1.315
5	Cash	Call	30-Jun-2006	05-Jul-2006	1.289
6	Cash	Put	30-Jun-2006	05-Jul-2006	1.325
7	Asset	Call	31-Dec-2004	04-Jan-2005	1.300
8	Asset	Put	31-Dec-2004	04-Jan-2005	1.300
9	Asset	Call	01-Jun-2005	02-Jun-2005	1.307
10	Asset	Put	01-Jun-2005	02-Jun-2005	1.315
11	Asset	Call	30-Jul-2006	31-Jul-2006	1.289
12	Asset	Put	30-Jul-2006	31-Jul-2006	1.325

Appendix 3. Forward Foreign Exchange Rate

Number of Days from Valuation Date	USD/EUR Forward Points 
(bps)	USD/EUR Forward Outright	Number of Days from Valuation Date	CAD/USD Forward Points 
(bps)	CAD/USD Forward Outright
7	-1.1675	1.205933	7	1.1500	1.319065
14	-2.3350	1.205817	14	2.4500	1.319195
30	-4.6700	1.205583	30	5.4500	1.319495
61	-8.0750	1.205243	59	11.2000	1.320070
91	-10.1000	1.205040	91	17.5000	1.320700
124	-10.6000	1.204990	122	23.0000	1.321250
153	-11.1000	1.204940	153	29.0000	1.321850
181	-11.6000	1.204890	181	34.5000	1.322400
273	-8.6000	1.205190	273	52.0000	1.324150
365	-2.5000	1.205800	365	67.5000	1.325700
546	18.2500	1.207875	546	94.7500	1.328425
730	45.0000	1.210550	730	122.0000	1.331150


Appendix 4. Forward Foreign Exchange Rate Volatilities

Number of Days from Valuation Date	USD EUR FX Volatility	Number of Days from Valuation Date	USD CAD FX Volatility
0	0.10000	0	0.08750
5	0.10000	6	0.08750
12	0.09900	13	0.08630
28	0.09700	29	0.08500
57	0.10000	58	0.08450
89	0.10100	90	0.08250
177	0.10400	178	0.08100
268	0.10475	269	0.08050
363	0.10550	364	0.08000
728	0.10540	729	0.08000
1,093	0.10520	1,094	0.07950
1,457	0.10490	1,458	0.07950
1,822	0.10490	1,823	0.07950




