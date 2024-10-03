SparkFun Qwiic Power Switch
========================================

A power switch for your Qwiic system.

[![SparkFun Qwiic Power Switch (PRT-26784)]()](https://www.sparkfun.com/products/26784)

[SparkFun Qwiic Power Switch (PRT-26784)](https://www.sparkfun.com/products/26784)

The Qwiic Power Switch is a simple little board which can be used to switch the power to your Qwiic
system. Many Qwiic boards draw very little current when not being used, but there are some that draw
significantly more. The power switch allows you to switch the power to those boards, so you can minimize the
current draw and extend your battery life when you need to.

When the Qwiic Power Switch is turned off, the I2C wires are isolated too which prevents the pull-up
resistors from feeding parasitic power to your Qwiic boards. The power switch can also be used to
isolate a 400kHz bus from a 100kHz bus; the slower bus can be disconnected during fast-mode communication
without disabling the power.

The heart of the Qwiic Power Switch is the TI PCA9536 4-Bit I2C I/O Expander. We have broken out GPIO pins
1 and 2 so you can use them as general purpose inputs or outputs.



Repository Contents
-------------------

* **.github/workflows** - YAML files used for GitHub Actions and GitHub Pages/mkdocs
* **/Firmware** - Example code
* **/Hardware** - Eagle design files (.brd, .sch)
  * **/Production** - Production panel files (.brd)
* **/docs** - Online documentation files
  * **/assets** - Folder containing all the file assets used for product documentation
    * **/board_files** - Copy of design files used for product documentation
    * **/component_documentation** - Datasheets and manuals for hardware components
    * **/img** - Images for product documentation
  * **/github** - Files stating how to contribute and filing issues used for product documentation
  * **/javascript** - Folder containing custom javascript used for product documentation
  * **/stylesheet** - Folder containing CSS files used for product documentation
* **/overrides** - Customization files used for product documentation
  * **/.icons** - Icons used for GitHub used for product documentation
  * **./partials** - Used for product documentation
- **LICENSE.md** contains the licence information



Documentation
-------------------

* **[Installing an Arduino Library Guide](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)** - Basic information on how to install an Arduino library.
* **[Arduino Library](https://github.com/sparkfun/SparkFun_Qwiic_Power_Switch_Arduino_Library)** - Library for the Qwiic Power Switch
* **[Hookup Guide](https://docs.sparkfun.com/SparkFun_Qwiic_Power_Switch/introduction/)** - Basic hookup guide for the Qwiic Power Switch.



Product Versions
----------------

* [PRT-26784](https://www.sparkfun.com/products/26784) - SparkFun Red Version
* [PRT-16740](https://www.sparkfun.com/products/16740) - SparkX Version



License Information
-------------------

This product is _**open source**_!

Please review the LICENSE.md file for license information.

If you have any questions or concerns on licensing, please contact technical support on our [SparkFun forums](https://forum.sparkfun.com/viewforum.php?f=123).

Distributed as-is; no warranty is given.

- Your friends at SparkFun.
