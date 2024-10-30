In this section, we will go over how to connect to the Qwiic Power Switch.


### Connecting Via Qwiic

Insert a Qwiic cable between your Arduino microcontroller and the Qwiic Power Switch&apos;s IN port. In this case, we used the SparkFun Thing Plus ESP32- USB-C for the Arduino microcontroller. Then connect Qwiic cable between the Qwiic Power Switch's OUT port to the second Qwiic-enabled device. In this case, we used the ZED-F9P SMA breakout board when toggling power and isolating the I<sup>2</sup>C lines. We also connected an external multiband antenna to the ZED-F9P. When ready, connect a USB cable to the Arduino to program, power, and control the Qwiic Power Switch through a serial terminal.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-26784_Qwiic_Power_Switch_ESP32_ZED-F9P_Hardware_Hookup.jpg"><img src="../assets/img/PRT-26784_Qwiic_Power_Switch_ESP32_ZED-F9P_Hardware_Hookup.jpg" width="600px" height="600px" alt="Thing Plus ESP32, Qwiic Power Switch, ZED-F9P Connected via Qwiic"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>Thing Plus ESP32, Qwiic Power Switch, ZED-F9P Connected via Qwiic</i></td>
    </tr>
  </table>
</div>



!!! note
    To isolate any Qwiic-enabled device, you will need to connect the Qwiic-enabled device from the OUT port.



### Connecting via PTH

For temporary connections to the PTHs, you could use IC hooks to test out the pins. However, you'll need to solder headers or wires of your choice to the board for a secure connection. You can choose between a combination of [header pins and jumper wires](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all), or [stripping wire and soldering the wire](https://learn.sparkfun.com/tutorials/working-with-wire/all) directly to the board.

<div class="grid cards col-2" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <b>How to Solder: Through Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG" style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>
