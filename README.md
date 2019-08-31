# Overview 
NI offers various Python drivers for its hardware, such as NI-DAQmx. I thought it would be nice to create the Voltage - Continuous Input shipping example using Python. A demonstration video of a replicated version made using Python is shown below.

![Alt Text](https://ni.i.lithium.com/t5/image/serverpage/image-id/248842i2F311D6F454116D7/image-size/large?v=1.0&px=999)

# Description
The GUI is built using [Tkinter](https://docs.python.org/3/library/tk.html) and [Matplotlib](https://matplotlib.org/). I tried to emulate the LabVIEW shipping example as closely as possible. Once everything is positioned properly on the window, the user can start the acquisition. The GUI will poll the task until the required number of samples are available to read. The task will stop and be closed when the user presses the stop button. 

# Hardware and Software Requirements
- Python 3.6
- Matplotlib
- NI-DAQmx
- NI-DAQmx Python Package
- NI-DAQmx supported device or [simulated device](http://www.ni.com/tutorial/3698/en/) with an analog input channel. 

# Steps to Implement or Execute Code
1. You will need to install [Python](https://www.python.org/downloads/) 3.6 or newer, the latest version of [Matplotlib](https://matplotlib.org/3.1.0/users/installing.html), and [NI-DAQmx](http://www.ni.com/en-us/support/downloads/drivers/download.ni-daqmx.html#301173), and the [NI-DAQmx Python Package](https://nidaqmx-python.readthedocs.io/en/latest/). 
2. Once these are installed, you can download the two attached files and place them in a folder next to each other.
3. Run the Python application in an IDE or text editor of your choice. During development, I used [Sublime Text](https://www.sublimetext.com/). You can run Python scripts from the editor with the shortcut ctrl+b defined in the Tools dropdown menu of Sublime.
4. Insure that you have a device in NI MAX that has an analog input channel and that it is listed in the Physical Channel entry box of the Python GUI.  
5. Click Start Task to begin acquiring data.

# Additional Information or References
Please feel free to suggest additional improvements and best practices. I would really appreciate any and all advice. My class architecture felt a little clumsy, but the different classes I had could easily be reused in other programs down the road. I also thought of several minor improvements could be made:

- There is no error handling for improper user inputs or NI-DAQmx exceptions.
- The choice of physical channels is not a drop down of options available in NI MAX.
- Additional settings and trigger options are missing that are present in the LabVIEW example.
- The start and stop button should probably belong to the graph class. 
- The stop button should be disabled unless the task is running. 
- Channel expansion is not supported.
