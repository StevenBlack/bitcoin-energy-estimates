<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1 plus MathML 2.0//EN"
        "HTMLFiles/xhtml-math11-f.dtd">

<!-- Created with the Wolfram Language : www.wolfram.com -->

<html xmlns="http://www.w3.org/1999/xhtml">
<head>
 <title>
  bitcoin-energy-estimates
 </title>
 <link href="HTMLFiles/readme.md.css" rel="stylesheet" type="text/css" />
</head>

<body style="font-size: Floor[150. Inherited]%;">

<p class="Title">
 Bitcoin Energy Estimates (DRAFT)
</p>



<p class="Subtitle">
 Estimating the energy use of the Bitcoin network using two different approaches.
</p>



<p class="Author">
 by Steven Black<br />Project home: https://github.com/StevenBlack/bitcoin-energy-estimates<br />Updated: October 22 2023
</p>



<p class="Section">
 Introduction
</p>



<p class="Text">
 Bitcoin mining uses a Proof-of-Work consensus mechanism. This is controversial for some because that supposedly requires a lot of electrical energy. We see claims the bitcoin network &ldquo;<span style='font-style: italic;'>uses as much electricity as a small country</span>&rdquo;, or <span style='font-style: italic;'>&ldquo;requires as much electricity as Belgium, or Chile.</span>&rdquo;
</p>



<p class="Text">
 This Mathematica notebook assessed those notions using the following approaches: 
</p>



<p class="ItemNumbered">
 <span style='font-style: italic;font-weight: bold;'>Presuming Bitcoin mining is marginally profitable, how much electical energy can be funded that balances actual mining rewards over time?</span>
</p>



<p class="ItemNumbered">
 <span style='font-style: italic;font-weight: bold;'>Given the reported hashrate, how much energy would be required to achieve that?</span>
</p>



<p class="Text">
 This paper uses <span style='font-weight: bold;'>Canadian dollars</span>, partly because that&rsquo;s my fiat currency, and because Canada publishes particularly good statistics about electricity generation and costs.
</p>



<p class="Subsection">
 Bitcoin price, block rewards, and fees
</p>



<p class="Text">
 Here we outline the major factors that play in the economics of Bitcoin mining.
</p>



<p class="Subsubsection">
 The bitcoin price right now
</p>



<p class="Text">
 What is the current price of Bitcoin in Canadian dollars?
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_1.png" alt="readme.md_1.png" width="35" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_2.png" alt="readme.md_2.png" width="283" height="40" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_3.png" alt="readme.md_3.png" width="944" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_4.png" alt="readme.md_4.png" width="170" height="34" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 Bitcoin block rewards
</p>



<p class="Text">
 Bitcoin miners are compensated with the block reward from blocks they successfully mine, plus all the transaction fees in that block. In the current epoch (2020 - 2024) the block reward is 6 1/4 BTC.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_5.png" alt="readme.md_5.png" width="406" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_6.png" alt="readme.md_6.png" width="89" height="38" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 Bitcoin transaction fees per block
</p>



<p class="Text">
 <span style='font-weight: bold;'>ASSUMPTION</span>: the average of transaction fees per block is 0.15 BTC.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_7.png" alt="readme.md_7.png" width="501" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_8.png" alt="readme.md_8.png" width="89" height="38" style="vertical-align:middle" />
</p>

<p class="Text">
 Therefore, the total Bitcoin paid to miners for an average block, denominated in Bitcoin.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_9.png" alt="readme.md_9.png" width="655" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_10.png" alt="readme.md_10.png" width="73" height="38" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 The actual block rate
</p>



<p class="Text">
 Historically Bitcoin blocks land at a rate faster then the block time target (6 per hour, or 144 blocks per day).&nbsp;&nbsp;Let's recon an average block rate over a sample interval to present day:
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_11.gif" alt="readme.md_11.gif" width="1000" height="58" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_12.png" alt="readme.md_12.png" width="187" height="39" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_13.png" alt="readme.md_13.png" width="794" height="58" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_14.png" alt="readme.md_14.png" width="213" height="34" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_15.png" alt="readme.md_15.png" width="751" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_16.png" alt="readme.md_16.png" width="252" height="38" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 Total miner compensation, per hour
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_17.png" alt="readme.md_17.png" width="675" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_18.png" alt="readme.md_18.png" width="274" height="39" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 Bitcoin price in Canadian dollars as a time series
</p>



<p class="Text">
 Let's gather data on bitcoin price over the past sampleIntervalTime.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_19.png" alt="readme.md_19.png" width="734" height="58" style="vertical-align:middle" />
</p>

<p class="Text">
 Let's graph that bitcoin price over time.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_20.png" alt="readme.md_20.png" width="994" height="244" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_21.gif" alt="Graphics:BTC Price&amp;nbsp;&amp;nbsp;&amp;mdash; last 100000 blocks CAD" width="864" height="551" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_22.png" alt="readme.md_22.png" width="4" height="26" style="vertical-align:middle" />
</p>

<p class="Subsubsection">
 Average bitcoin price over our sample time
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_23.png" alt="readme.md_23.png" width="411" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_24.png" alt="readme.md_24.png" width="170" height="34" style="vertical-align:middle" />
</p>

<p class="Section">
 1. Assuming mining is ecomomically marginal, how much electricity could be funded by mining rewards?
</p>



<p class="Subsection">
 Global revenue per hour
</p>



<p class="Text">
 The value, in Canadian Dollars, of all Bitcoin mined globally, per hour.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_25.png" alt="readme.md_25.png" width="1011" height="58" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_26.png" alt="readme.md_26.png" width="357" height="41" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Electricity cost, per kWh
</p>



<p class="Text">
 See: https://www.hydroquebec.com/business/customer-space/rates/comparison-electricity-prices.html
</p>



<p class="Text">
 <span><span><img src="HTMLFiles/readme.md_27.gif" alt="readme.md_27.gif" width="994" height="529" style="vertical-align:middle" /></span></span>
</p>



<p class="Text">
 Let&rsquo;s presume that nobody in their right mind would want to mine Bitcoin in New York or Boston. Here's the distribution of electricity input costs from the other 5 locations.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_28.png" alt="readme.md_28.png" width="499" height="182" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_29.png" alt="readme.md_29.png" width="578" height="38" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Business cost assumption
</p>



<p class="Text">
 Let&rsquo;s presume 85% of mining revenue is available to pay electricity cost. The rest covers wages, maintenance, depreciation, and taxes.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_30.png" alt="readme.md_30.png" width="350" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_31.png" alt="readme.md_31.png" width="65" height="34" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Energy economically sustainable
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_32.png" alt="readme.md_32.png" width="590" height="54" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_33.png" alt="readme.md_33.png" width="286" height="41" style="vertical-align:middle" />
</p>

<p class="Text">
 Cognitively we can say, Bitcoin's power consumption is in the order of 10 GWH.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_34.png" alt="readme.md_34.png" width="447" height="120" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_35.png" alt="readme.md_35.png" width="207" height="38" style="vertical-align:middle" />
</p>

<p class="Text">
 Cognitively we can say, Bitcoin's annual energy consumption is in the order of 90 TWH.
</p>



<p class="Subsection">
 Comparisons with large power generation facilities or regions
</p>



<p class="Text">
 Let&rsquo;s compare the Bitcoin network with the power and energy that generated, or used, by various things.
</p>



<p class="Text">
 Here's the raw data for various generation facilities and regions.
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_36.png" alt="readme.md_36.png" width="903" height="190" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_37.png" alt="readme.md_37.png" width="906" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_38.png" alt="readme.md_38.png" width="764" height="175" style="vertical-align:middle" />
</p>

<p class="Section">
 2. Given the reported hashrate, how much energy would be required to achieve that?
</p>



<p class="Text">
 Coming soon.
</p>



<p class="Chapter">
 Appendix
</p>



<p class="Subsection">
 Robert-<span>Bourassa</span> generating station &mdash; a.k.a. &ldquo;LG-2&rdquo;
</p>



<p class="Text">
 Here we compare the power consumption of the bitcoin network with the power generation capacity of the Robert Bourassa generating station in the James Bay region of northern Qu&eacute;bec. <br />See https://en.wikipedia.org/wiki/Robert-Bourassa_generating_station
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_39.png" alt="readme.md_39.png" width="532" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_40.png" alt="readme.md_40.png" width="122" height="34" style="vertical-align:middle" />
</p>

<p class="Text">
 What is Bitcoin&rsquo;s global energy use in terms of LG-2?
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_41.png" alt="readme.md_41.png" width="313" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_42.png" alt="readme.md_42.png" width="187" height="38" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Province of Qu&eacute;bec
</p>



<p class="Text">
 In 2019 the Province of Qu&eacute;bec produced 212.9 TWh of electricity.<br /><br />What is Bitcoin&rsquo;s global energy use as a proportion of Qu&eacute;bec&rsquo;s electricity production in 2019?
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_43.png" alt="readme.md_43.png" width="246" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_44.png" alt="readme.md_44.png" width="143" height="34" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_45.png" alt="readme.md_45.png" width="476" height="61" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_46.png" alt="readme.md_46.png" width="154" height="34" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_47.png" alt="readme.md_47.png" width="271" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_48.png" alt="readme.md_48.png" width="187" height="38" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Province of Ontario
</p>



<p class="Text">
 See https://www.cer-rec.gc.ca/en/data-analysis/energy-markets/provincial-territorial-energy-profiles/provincial-territorial-energy-profiles-ontario.html
</p>



<p class="Text">
 In 2019, the average annual power consumption per capita in Ontario was 9.6 megawatt-hours (MWh).
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_49.gif" alt="readme.md_49.gif" width="806" height="94" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_50.png" alt="readme.md_50.png" width="267" height="38" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_51.png" alt="readme.md_51.png" width="372" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_52.png" alt="readme.md_52.png" width="322" height="41" style="vertical-align:middle" />
</p>

<p class="Subsection">
 United States
</p>



<p class="Text">
 See https://www.worlddata.info/america/usa/energy-consumption.php
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_53.gif" alt="readme.md_53.gif" width="747" height="94" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_54.png" alt="readme.md_54.png" width="267" height="38" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_55.png" alt="readme.md_55.png" width="278" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_56.png" alt="readme.md_56.png" width="322" height="41" style="vertical-align:middle" />
</p>

<p class="Subsection">
 Europe
</p>



<p class="Text">
 Again see See https://www.worlddata.info/america/usa/energy-consumption.php
</p>



<p class="Input">
 <img src="HTMLFiles/readme.md_57.gif" alt="readme.md_57.gif" width="771" height="94" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_58.png" alt="readme.md_58.png" width="284" height="38" style="vertical-align:middle" />
</p>

<p class="Input">
 <img src="HTMLFiles/readme.md_59.png" alt="readme.md_59.png" width="313" height="26" style="vertical-align:middle" />
</p>

<p class="Output">
 <img src="HTMLFiles/readme.md_60.png" alt="readme.md_60.png" width="351" height="41" style="vertical-align:middle" />
</p>




<div style="font-family:Helvetica; font-size:11px; width:100%; border:1px none #999999; border-top-style:solid; padding-top:2px; margin-top:20px;">
 <a href="http://www.wolfram.com/language/" style="color:#000; text-decoration:none;">
  <span style="color:#555555">Created with the Wolfram Language</span> 
 </a>
</div>
</body>

</html>
