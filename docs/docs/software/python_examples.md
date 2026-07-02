# SparkFun DE2290 Python Package Examples

The DE2290 Python package includes three examples to demonstrate the basics of using the 2D Barcode Scanner Breakout with Python. In this section we'll cover the examples and highlight how they work.

To use the examples, open them from the DE2290 Py location or copy the code from the [GitHub Repository](https://github.com/sparkfun/DE2290_Py/tree/main/examples) into your preferred Python interpreter.

**Reminder:** The DE2290 Python Package communicates with the 2D Barcode Scanner Breakout over USB so make sure to set the DE2290 to USB-COM mode by scanning the barcode below or sending the appropriate serial command:

<figure>
[![DE2290 TTL Mode Barcode](/img/TTLRS232-Barcode.png)]
</figure>

The 2D Barcode Scanner saves all settings during power cycles so you can configure the DE2290 however you would like (e.g. scanning mode, image flipping, LED settings, etc.) prior to using the examples.

## Example 1 - Serial Scan

This basic example demonstrates how to initialize the barcode scanner and output any barcodes it reads. The example attempts to initialize the barcode scanner and, if successful, starts polling the buffer for any data every 200ms. If there is data in the buffer, the code prints it. With a terminal window open to the correct port, try scanning barcodes with the breakout and watch the decoded barcode data print out.

## Example 2 - Serial Settings

This example shows how to configure various settings for the DE2290 using serial inputs sent over USB. The code creates an interactive menu for starting and stopping a scan along with the settings listed below:

* Enable/Disable Flashlight
* Enable/Disable Aiming Reticle
* Enable/Disable Decode Beep
* Enable/Disable Start Up Beep
* Change Buzzer Frequency
* Enablde/Disable Image Flipping
* Set Reading Area
* Set Reading Mode
* Enable/Disable Symbologies


Run the example and open a terminal window to the Barcode Scanner's port. To adjust a setting, type in the corresponding number and hit ENTER. A second menu for will open with the available options for the setting. Type in the number matching the preferred option and hit ENTER again. The code prints out if the setting is adjusted successfully and then returns to the main menu.

## Example 3 - Send Command

The third example demonstrates how to use the `send_command` function to send specific command strings to the DE2290. The `send_command` function takes two strings, links them together, adds the command prefix ("^_^") and suffix (".") and sends the command to the DE2290. 

Run the example and open a terminal window to the Barcode Scanner's port. Once the terminal window is open, type in the command you want to use and press ENTER. Refer to the [Scan Settings Manual](/ref/DY%20SCAN%202D%20barcode%20scanner%20DE2290D.%20DE2290H%20setting%20manual.pdf) for the Command Table. If the command is not recognized, the code prints out the code is invalid.