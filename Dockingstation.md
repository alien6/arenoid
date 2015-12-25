# UART with a modified Dockingstation #


---

## <u>1. Introduction</u> ##
> ### <u>1.1 The Dockingstation</u> ###
> <img width='50%' height='50%' border='0' src='http://img4.imageshack.us/img4/1905/ds3n.png' /><br>
<blockquote>The LG SDT-120 Dockingstation</blockquote>

<blockquote><h3><u>1.2 Why all the effort?</u></h3>
<table><thead><th> <img width='80%' align='center' height='80%' border='0' src='http://img541.imageshack.us/img541/4400/ds1o.png' /><br>Plug of the standard USB cable (5 pin) </th><th> <img width='80%' height='80%' border='0' src='http://img694.imageshack.us/img694/9005/ds2t.png' /><br>Plug of the dockingstation (18 pin) </th></thead><tbody></blockquote></tbody></table>

<blockquote>So, the connector on the docking station got all 18 pins. In this guide, we describe how to connect the UART pins of the plug, with your COM-Port on your computer. All connections are present on the dockingstation plug, so we have to make any changes on the ARENA and the warranty remains!</blockquote>


<blockquote><font color='red'><b>WARNING:</b></font><br>
<font color='red'><b>The MAX3232(RS232-TTL-Converter) is a level converter that feeds the -12V/+12V signals (from PC) in 5V/0V signals (to AVR/ARM processor). If you connect the dockingstation directly with the COM-Port cable (RS232-Cable), you'll destroy the processor of the KM900 ARENA and your phone is irreversible damaged. YOU NEED THE RS232-TTL-Converter!</b></font></blockquote>

<hr />
<h2><u>2. What you need</u></h2>

<ol><li>LG Docking Station SDT-120, <a href='http://www.amazon.de/LG-SDT-120-Dockingstation-KM900/dp/B0028OFHX6/ref=sr_1_1?ie=UTF8&s=ce-de&qid=1279733593&sr=8-1,'>LINK</a>
</li><li>RS232 Cable, <a href='http://www.amazon.de/gp/product/B000L38KMG/sr=8-1/qid=1279733509/ref=olp_product_details?ie=UTF8&me=&qid=1279733509&sr=8-1&seller='>LINK</a>
</li><li>RS232-TTL-Converter, <a href='http://www.virtualvillage.de/rs232-auf-seriell-com-port-ttl-converter-adapter-003602-008.html,'>LINK</a>
</li><li>Cable "stripe" from an IDE cable<br>
</li><li>Soldering iron & solder</li></ol>

<hr />
<h2><u>3. Instructions</u></h2>

<blockquote><h3><u>3.1 Disassemble the dockingstation (LG SDT-120)</u></h3></blockquote>

<blockquote><h4><u>3.1.1 Expose the screws</u></h4>
<img width='50%' height='50%' border='0' src='http://img843.imageshack.us/img843/6369/da1.png' /><br>At the bottom of the DS, there are two gumstripes. Below you will find  two screws on each side.</blockquote>

<blockquote><img width='50%' height='50%' border='0' src='http://img690.imageshack.us/img690/4075/da1b.png' /><br>One screw left under the serialnumber sticker.</blockquote>

<blockquote><h4><u>3.1.2 Open the plastic case</u></h4>
<img width='50%' height='50%' border='0' src='http://img823.imageshack.us/img823/3464/da2.png' /></blockquote>

<blockquote><h4><u>3.1.3 Remove the plug</u></h4>
<img width='50%' height='50%' border='0' src='http://img821.imageshack.us/img821/2869/da3.png' /><br>Open these four screws (green circle). <b>Attention:</b> They are very tightly screwed.</blockquote>

<blockquote><h4><u>3.1.4 Remove the clip & the plug case</u></h4></blockquote>

<blockquote><img width='50%' height='50%' border='0' src='http://img833.imageshack.us/img833/1791/da4.png' /><br>Remove this clip by pulling it out.</blockquote>

<blockquote><img width='50%' height='50%' border='0' src='http://img237.imageshack.us/img237/3198/da5.png' /><br>The plug case can be removed now easily.</blockquote>

<blockquote><img width='50%' height='50%' border='0' src='http://img34.imageshack.us/img34/6654/da6.png' /><br>The plug is ready for soldering some cable on it.</blockquote>

<blockquote><h3><u>3.2 Connection between dockingstation & RS232-TTL-Converter</u></h3>
<h4><u>3.2.1 Construct a cable</u></h4>
At first you'll need to construct a cable for the connection between the DS and the RS232-TTL-Converter:</blockquote>

<blockquote><img width='25%' height='25%' border='0' src='http://img807.imageshack.us/img807/4641/p2027210710.png' /> <img src='http://img408.imageshack.us/img408/7234/arrowa.png' /> <img width='25%' height='25%' border='0' src='http://img688.imageshack.us/img688/6515/p2028210710.png' /> <img src='http://img408.imageshack.us/img408/7234/arrowa.png' /> <img width='25%' height='25%' border='0' src='http://img210.imageshack.us/img210/9275/p2034210710.png' /><br>(I opted for a strip from an IDE cable.)</blockquote>

<blockquote><h4><u>3.2.2 Solder the cables</u></h4>
<img src='http://img809.imageshack.us/img809/4175/tablel.png' /></blockquote>

<blockquote><h3><u>3.3 Build a connection via UART</u></h3></blockquote>

<hr />
<h2><u>4. Credits</u></h2>
<ul><li>Fragger255, this guide is based on his knowledge. He has figured out how to build a UART connection between PC and KM900.<br>
</li><li>okNNN, more detailed pictures.