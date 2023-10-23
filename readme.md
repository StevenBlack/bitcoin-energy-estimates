# Bitcoin Energy Estimates (DRAFT)

**Estimating the energy use of the Bitcoin network using two different approaches.**

 by Steven Black<br />Project home: https://github.com/StevenBlack/bitcoin-energy-estimates<br />Updated: October 22 2023

## Introduction

 Bitcoin mining uses a Proof-of-Work consensus mechanism. This is controversial for some people because that supposedly requires a lot of electrical energy. We see claims the bitcoin network &ldquo;<span style='font-style: italic;'>uses as much electricity as a small country</span>&rdquo;, or <span style='font-style: italic;'>&ldquo;requires as much electricity as Belgium, or Chile.</span>&rdquo;

 This Mathematica notebook assessed those notions using the following approaches: 

1. ***Presuming Bitcoin mining is marginally profitable, how much electical energy can be funded that balances actual mining rewards over time?***

1. ***Given the reported hashrate, how much energy would be required to achieve that?***

 This paper uses **Canadian dollars**, partly because that&rsquo;s my fiat currency, and because Canada publishes particularly good statistics about electricity generation and costs.

### Bitcoin price, block rewards, and fees

 Here we outline the major factors that play in the economics of Bitcoin mining.

#### The bitcoin price right now

 What is the current price of Bitcoin in Canadian dollars?

 <img src="HTMLFiles/bitcoin-energy-estimates_1.png" alt="bitcoin-energy-estimates_1.png" width="35" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_2.png" alt="bitcoin-energy-estimates_2.png" width="286" height="40" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_3.png" alt="bitcoin-energy-estimates_3.png" width="944" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_4.png" alt="bitcoin-energy-estimates_4.png" width="170" height="34" style="vertical-align:middle" />

#### Bitcoin block rewards

 Bitcoin miners are compensated with the block reward from blocks they successfully mine, plus all the transaction fees in that block. In the current epoch (2020 - 2024) the block reward is 6 1/4 BTC.

 <img src="HTMLFiles/bitcoin-energy-estimates_5.png" alt="bitcoin-energy-estimates_5.png" width="406" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_6.png" alt="bitcoin-energy-estimates_6.png" width="89" height="38" style="vertical-align:middle" />

#### Bitcoin transaction fees per block

 **ASSUMPTION**: the average of transaction fees per block is 0.15 BTC.

 <img src="HTMLFiles/bitcoin-energy-estimates_7.png" alt="bitcoin-energy-estimates_7.png" width="501" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_8.png" alt="bitcoin-energy-estimates_8.png" width="89" height="38" style="vertical-align:middle" />

 Therefore, the total Bitcoin paid to miners for an average block, denominated in Bitcoin.

 <img src="HTMLFiles/bitcoin-energy-estimates_9.png" alt="bitcoin-energy-estimates_9.png" width="655" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_10.png" alt="bitcoin-energy-estimates_10.png" width="73" height="38" style="vertical-align:middle" />

#### The actual block rate

 Historically Bitcoin blocks land at a rate faster then the block time target (6 per hour, or 144 blocks per day).&nbsp;&nbsp;Let's recon an average block rate over a sample interval to present day:

 <img src="HTMLFiles/bitcoin-energy-estimates_11.gif" alt="bitcoin-energy-estimates_11.gif" width="1000" height="58" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_12.png" alt="bitcoin-energy-estimates_12.png" width="187" height="39" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_13.png" alt="bitcoin-energy-estimates_13.png" width="794" height="58" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_14.png" alt="bitcoin-energy-estimates_14.png" width="213" height="34" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_15.png" alt="bitcoin-energy-estimates_15.png" width="751" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_16.png" alt="bitcoin-energy-estimates_16.png" width="252" height="38" style="vertical-align:middle" />

#### Total miner compensation, per hour

 <img src="HTMLFiles/bitcoin-energy-estimates_17.png" alt="bitcoin-energy-estimates_17.png" width="675" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_18.png" alt="bitcoin-energy-estimates_18.png" width="274" height="39" style="vertical-align:middle" />

#### Bitcoin price in Canadian dollars as a time series

 Let's gather data on bitcoin price over the past sampleIntervalTime.

 <img src="HTMLFiles/bitcoin-energy-estimates_19.png" alt="bitcoin-energy-estimates_19.png" width="734" height="58" style="vertical-align:middle" />

 Let's graph that bitcoin price over time.

 <img src="HTMLFiles/bitcoin-energy-estimates_20.png" alt="bitcoin-energy-estimates_20.png" width="994" height="244" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_21.gif" alt="Graphics:BTC Price&amp;nbsp;&amp;nbsp;&amp;mdash; last 100000 blocks CAD" width="864" height="551" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_22.png" alt="bitcoin-energy-estimates_22.png" width="4" height="26" style="vertical-align:middle" />

#### Average bitcoin price over our sample time

 <img src="HTMLFiles/bitcoin-energy-estimates_23.png" alt="bitcoin-energy-estimates_23.png" width="411" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_24.png" alt="bitcoin-energy-estimates_24.png" width="170" height="34" style="vertical-align:middle" />

## 1. Assuming mining is ecomomically marginal, how much electricity could be funded by mining rewards?

### Global revenue per hour

 The value, in Canadian Dollars, of all Bitcoin mined globally, per hour.

 <img src="HTMLFiles/bitcoin-energy-estimates_25.png" alt="bitcoin-energy-estimates_25.png" width="1011" height="58" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_26.png" alt="bitcoin-energy-estimates_26.png" width="357" height="41" style="vertical-align:middle" />

### Electricity cost, per kWh

 See: https://www.hydroquebec.com/business/customer-space/rates/comparison-electricity-prices.html

 <span><span><img src="HTMLFiles/bitcoin-energy-estimates_27.gif" alt="bitcoin-energy-estimates_27.gif" width="994" height="529" style="vertical-align:middle" /></span></span>

 Let&rsquo;s presume that nobody in their right mind would want to mine Bitcoin in New York or Boston. Here's the distribution of electricity input costs from the other 5 locations.

 <img src="HTMLFiles/bitcoin-energy-estimates_28.png" alt="bitcoin-energy-estimates_28.png" width="499" height="182" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_29.png" alt="bitcoin-energy-estimates_29.png" width="578" height="38" style="vertical-align:middle" />

### Business cost assumption

 Let&rsquo;s presume 85% of mining revenue is available to pay electricity cost. The rest covers wages, maintenance, depreciation, and taxes.

 <img src="HTMLFiles/bitcoin-energy-estimates_30.png" alt="bitcoin-energy-estimates_30.png" width="350" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_31.png" alt="bitcoin-energy-estimates_31.png" width="65" height="34" style="vertical-align:middle" />

### Energy economically sustainable

 <img src="HTMLFiles/bitcoin-energy-estimates_32.png" alt="bitcoin-energy-estimates_32.png" width="590" height="54" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_33.png" alt="bitcoin-energy-estimates_33.png" width="286" height="41" style="vertical-align:middle" />

 Cognitively we can say, Bitcoin's power consumption is in the order of 10 GWH.

 <img src="HTMLFiles/bitcoin-energy-estimates_34.png" alt="bitcoin-energy-estimates_34.png" width="447" height="120" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_35.png" alt="bitcoin-energy-estimates_35.png" width="207" height="38" style="vertical-align:middle" />

 Cognitively we can say, Bitcoin's annual energy consumption is in the order of 90 TWH.

### Comparisons with large power generation facilities or regions

 Let&rsquo;s compare the Bitcoin network with the power and energy that generated, or used, by various things.

 Here's the raw data for various generation facilities and regions.

 <img src="HTMLFiles/bitcoin-energy-estimates_36.png" alt="bitcoin-energy-estimates_36.png" width="903" height="190" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_37.png" alt="bitcoin-energy-estimates_37.png" width="906" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_38.png" alt="bitcoin-energy-estimates_38.png" width="764" height="175" style="vertical-align:middle" />

## 2. Given the reported hashrate, how much energy would be required to achieve that?

 Coming soon.

## Appendix

### Robert-<span>Bourassa</span> generating station &mdash; a.k.a. &ldquo;LG-2&rdquo;

 Here we compare the power consumption of the bitcoin network with the power generation capacity of the Robert Bourassa generating station in the James Bay region of northern Qu&eacute;bec. <br />See https://en.wikipedia.org/wiki/Robert-Bourassa_generating_station

 <img src="HTMLFiles/bitcoin-energy-estimates_39.png" alt="bitcoin-energy-estimates_39.png" width="532" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_40.png" alt="bitcoin-energy-estimates_40.png" width="122" height="34" style="vertical-align:middle" />

 What is Bitcoin&rsquo;s global energy use in terms of LG-2?

 <img src="HTMLFiles/bitcoin-energy-estimates_41.png" alt="bitcoin-energy-estimates_41.png" width="313" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_42.png" alt="bitcoin-energy-estimates_42.png" width="187" height="38" style="vertical-align:middle" />

### Province of Qu&eacute;bec

 In 2019 the Province of Qu&eacute;bec produced 212.9 TWh of electricity.<br /><br />What is Bitcoin&rsquo;s global energy use as a proportion of Qu&eacute;bec&rsquo;s electricity production in 2019?

 <img src="HTMLFiles/bitcoin-energy-estimates_43.png" alt="bitcoin-energy-estimates_43.png" width="246" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_44.png" alt="bitcoin-energy-estimates_44.png" width="143" height="34" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_45.png" alt="bitcoin-energy-estimates_45.png" width="476" height="61" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_46.png" alt="bitcoin-energy-estimates_46.png" width="154" height="34" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_47.png" alt="bitcoin-energy-estimates_47.png" width="271" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_48.png" alt="bitcoin-energy-estimates_48.png" width="187" height="38" style="vertical-align:middle" />

### Province of Ontario

 See https://www.cer-rec.gc.ca/en/data-analysis/energy-markets/provincial-territorial-energy-profiles/provincial-territorial-energy-profiles-ontario.html

 In 2019, the average annual power consumption per capita in Ontario was 9.6 megawatt-hours (MWh).

 <img src="HTMLFiles/bitcoin-energy-estimates_49.gif" alt="bitcoin-energy-estimates_49.gif" width="806" height="94" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_50.png" alt="bitcoin-energy-estimates_50.png" width="267" height="38" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_51.png" alt="bitcoin-energy-estimates_51.png" width="372" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_52.png" alt="bitcoin-energy-estimates_52.png" width="322" height="41" style="vertical-align:middle" />

### United States

 See https://www.worlddata.info/america/usa/energy-consumption.php

 <img src="HTMLFiles/bitcoin-energy-estimates_53.gif" alt="bitcoin-energy-estimates_53.gif" width="747" height="94" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_54.png" alt="bitcoin-energy-estimates_54.png" width="267" height="38" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_55.png" alt="bitcoin-energy-estimates_55.png" width="278" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_56.png" alt="bitcoin-energy-estimates_56.png" width="322" height="41" style="vertical-align:middle" />

### Europe

 Again see See https://www.worlddata.info/america/usa/energy-consumption.php

 <img src="HTMLFiles/bitcoin-energy-estimates_57.gif" alt="bitcoin-energy-estimates_57.gif" width="771" height="94" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_58.png" alt="bitcoin-energy-estimates_58.png" width="284" height="38" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_59.png" alt="bitcoin-energy-estimates_59.png" width="313" height="26" style="vertical-align:middle" />

 <img src="HTMLFiles/bitcoin-energy-estimates_60.png" alt="bitcoin-energy-estimates_60.png" width="351" height="41" style="vertical-align:middle" />

<div style="font-family:Helvetica; font-size:11px; width:100%; border:1px none #999999; border-top-style:solid; padding-top:2px; margin-top:20px;">
 <a href="http://www.wolfram.com/language/" style="color:#000; text-decoration:none;">
  <span style="color:#555555">Created with the Wolfram Language</span> 
 </a>
</div>
