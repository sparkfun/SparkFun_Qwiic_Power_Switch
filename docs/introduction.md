


Many of our Qwiic products draw very little current when in standby, but there are some that draw considerably more. Products like our top-end [u-blox GNSS boards](https://www.sparkfun.com/products/16481) in particular. There are times when you wish you could switch them off to save power, and the [SparkFun Qwiic Power Switch (QPS)](https://www.sparkfun.com/products/26784) allows you to do exactly that!

<div class="grid cards" style="width:500px; margin: 0 auto;" markdown>

-   <a href="https://www.sparkfun.com/products/26784">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/7/8/6/7/PRT-26787-Qwiic-Power-Switch-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Power Switch">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26784">
      <b>SparkFun Qwiic Power Switch</b>
      <br />
      PRT-26784
      <br />
      <center>[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/26784){ .md-button .md-button--primary }</center>
    </a>
</div>

In this tutorial, we'll go over the hardware and how to hookup the SparkFun Qwiic Power Switch to an Arduino. We will also go over an Arduino example to get started.



### Required Materials

To follow along with this tutorial, you will need the following materials. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.

<div class="grid cards col-4" markdown>

<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/15424">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/9/8/3/15424-Reversible_USB_A_to_C_Cable_-_2m-02.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Reversible USB A to C Cable - 2m">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15424">
      <b>Reversible USB A to C Cable - 2m</b>
      <br />
      CAB-15424
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/20168">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/9/9/6/8/20168Diagonal.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Thing Plus - ESP32 WROOM (USB-C)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/20168">
      <b>SparkFun Thing Plus - ESP32 WROOM (USB-C)</b>
      <br />
      WRL-20168
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/26784">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/7/8/6/7/PRT-26787-Qwiic-Power-Switch-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Power Switch">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26784">
      <b>SparkFun Qwiic Power Switch</b>
      <br />
      PRT-26784
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14427">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/3/14427-Qwiic_Cable_-_100mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 100mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14427">
      <b>Qwiic Cable - 100mm</b>
      <br>
      PRT-14427
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>

You will also need a Qwiic-enabled device and an additional Qwiic cable. In this case, we used a ZED-F9P for demonstration purposes. Of course, you could use a different Qwiic-enabled device.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/16481">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/5/3/5/2/16481-SparkFun_GPS-RTK-SMA_Breakout_-_ZED-F9P__Qwiic_-01a.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun GPS-RTK-SMA Breakout - ZED-F9P (Qwiic)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/16481">
      <b>SparkFun GPS-RTK-SMA Breakout - ZED-F9P (Qwiic)</b>
      <br />
      GPS-16481
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/15192">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/6/1/1/15192-GNSS_Multi-band_Magnetic_Mount_Antenna_SMA_-_5m-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GNSS L1/L2 Multi-Band Magnetic Mount Antenna - 5m (SMA)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15192">
      <b>GNSS L1/L2 Multi-Band Magnetic Mount Antenna - 5m (SMA)</b>
      <br />
      GPS-15192
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14429">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/5/14429-Qwiic_Cable_-_500mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 500mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14429">
      <b>Qwiic Cable - 500mm</b>
      <br />
      PRT-14429
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>


### Qwiic Cables

For those that want to take advantage of the Qwiic connector, you'll want to grab a Qwiic cable. There are a variety of other cable lengths available in the SparkFun catalog to choose from.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/15081">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/4/3/1/15081-_01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Qwiic Cable Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15081">
      <b>SparkFun Qwiic Cable Kit</b>
      <br />
      KIT-15081
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14427">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/3/14427-Qwiic_Cable_-_100mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 100mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14427">
      <b>Qwiic Cable - 100mm</b>
      <br>
      PRT-14427
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14429">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/5/14429-Qwiic_Cable_-_500mm-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - 500mm">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14429">
      <b>Qwiic Cable - 500mm</b>
      <br />
      PRT-14429
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14425">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/4/5/1/14425-Qwiic_Cable_-_Breadboard_Jumper__4-pin_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Qwiic Cable - Breadboard Jumper (4-pin)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14425">
      <b>Qwiic Cable - Breadboard Jumper (4-pin)</b>
      <br />
      PRT-14425
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Tools _(Optional)_

For users connecting to the plated through holes, you will need a soldering iron, solder, and [general soldering accessories](https://www.sparkfun.com/categories/49).

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/24063">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="PINECIL Soldering Iron Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/24063">
      <b>PINECIL Soldering Iron Kit</b>
      <br />
      TOL-24063
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9163">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/5/8/7/09162-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Solder Lead Free - 15-gram Tube">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9163">
      <b>Solder Lead Free - 15-gram Tube</b>
      <br>
      TOL-09163
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11375">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hook-Up Wire - Assortment (Stranded, 22 AWG)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11375">
      <b>Hook-Up Wire - Assortment (Stranded, 22 AWG)</b>
      <br />
      PRT-11375
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12630">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/9/3/1/2/12630-Hakko-Wire-Strippers-30AWG-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Wire Strippers - 30AWG (Hakko)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12630">
      <b>Wire Strippers - 30AWG (Hakko)</b>
      <br />
      TOL-12630
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11952">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/4/2/2/11952-Hakko-Flush-Cutters-feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flush Cutters - Hakko">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11952">
      <b>Flush Cutters - Hakko</b>
      <br />
      TOL-11952
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12966">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/9/9/0/7/12966-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Digital Multimeter - Basic">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12966">
      <b>Digital Multimeter - Basic</b>
      <br />
      TOL-12966
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Prototyping Accessories  _(Optional)_

Depending on your setup, you may want to use IC hooks for a temporary connection. However, you will want to solder header pins to connect devices to the plated through holes for a secure connection.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/12002">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Self-Adhesive (White)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12002">
      <b>Breadboard - Self-Adhesive (White)</b>
      <br />
      PRT-12002
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9741">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="IC Hook with Pigtail">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9741">
      <b>IC Hook with Pigtail</b>
      <br>
      CAB-09741
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/553">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/7/8/00553-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Male Headers - Right Angle">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/553">
      <b>Break Away Male Headers - Right Angle</b>
      <br />
      PRT-00553
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/115">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/0/5/00115-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Female Headers">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/115">
      <b>Female Headers</b>
      <br />
      PRT-00115
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/8431">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/1/8/1/JumperWire-Male-01-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/M Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/8431">
      <b>Jumper Wires Premium 6" M/M Pack of 10</b>
      <br />
      PRT-08431
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9140">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/5/5/7/09140-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/F Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9140">
      <b>Jumper Wires Premium 6" M/F Pack of 10</b>
      <br />
      PRT-09140
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Suggested Reading

If you aren't familiar with the Qwiic Connection System, we recommend reading [here for an overview](https://www.sparkfun.com/qwiic).

<div style="text-align: center">
  <table style="border-style:none">
    <tr>
     <td style="text-align: center; vertical-align: middle;">
     <div style="text-align: center"><a href="https://www.sparkfun.com/qwiic"><img src="../assets/Qwiic-registered-updated.png" alt="Qwiic Connection System" title="Click to learn more about the Qwiic Connection System!"></a>
     </div>
    </td>
    </tr>
    <tr>
      <td style="text-align: center; vertical-align: middle;"><div style="text-align: center"><i><a href="https://www.sparkfun.com/qwiic">Qwiic Connection System</a></i></div></td>
    </tr>
  </table>
</div>

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through-Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <b>How to Solder: Through-Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/arduinoThumb.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Installing Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <b>Installing Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/esp32-thing-plus-usb-c-hookup-guide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/2/3/5/3/assembly_batt.jpg" style="width:264px; height:148px; object-fit:contain;" alt="ESP32 Thing Plus (USB-C) Hookup Guide">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/esp32-thing-plus-usb-c-hookup-guide">
      <b>ESP32 Thing Plus (USB-C) Hookup Guide</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG" style="width:264px; height:148px; object-fit:contain;" alt="Installing Board Definitions in the Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <b>Installing Board Definitions in the Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/9/0/8/USB-to-serial_converter_CH340-closeup.jpg" style="width:264px; height:148px; object-fit:contain;" alt="How to Install CH340 Drivers">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <b>How to Install CH340 Drivers</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/6/spiThumb_Updated2.png" style="width:264px; height:148px; object-fit:contain;" alt="Serial Peripheral Interface (SPI)">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi">
      <b>Serial Peripheral Interface (SPI)</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png" style="width:264px; height:148px; object-fit:contain;" alt="Logic Levels">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <b>Logic Levels</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>
