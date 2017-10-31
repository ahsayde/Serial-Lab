<img src="/imgs/logo.png" width="290">  


 **Serial Lab** is a Windows application (Written in C#) that **reads**, **writes** and **plots** data from/to serial port.  
 
  
 <img src="/imgs/sc3.png" width="430">
 
## Youtube  
 
 [https://www.youtube.com/watch?v=9CP6luC7eBs](https://www.youtube.com/watch?v=9CP6luC7eBs)
   
## Features
* Read and write data to serial ports even under high traffic load without freezing.
* Serial plotter for up to 5 different channels with useful options for curve fitting.
* There are 3 different modes to write data to the serial port: **Send word** - **Key capture** - **Write from file**.
* Displaying incoming data as **String** or **Hex**.
* Data logger to save incoming data to a **.txt** or **.csv** file.

## How to plot serial data?
In order for the data to be plotted, variables must be **seperated by comma ( , )** and a **newline ( \n )** character must be added at the end.
####Here an example code for [**Arduino**](https://www.arduino.cc/) platform 
```arduino
void setup()
{
	float var1, var2, var3;
	Serial.begin(9600);
}					

void loop()
{
	for(int i=0; i<360; i++)
	{
		var1 = 	sin(i* DEG_TO_RAD);
		var2 = -1*sin(i* DEG_TO_RAD);
		var3 = 	0.5*sin(i* DEG_TO_RAD);
		//send variables
		serial.print(var1);
		serial.print(",");
		serial.print(var2);
		serial.print(",");
		serial.print(var3);
		serial.println();
	}
}
```
so data must be in this form 
```
var1,var2,var3\n
```
and the result will be as shown in the image below   
  
<img src="/imgs/plotter.png" width="500">  

## Download  
Available versions  
[**SerialLabSetupV1.0.0.msi**](https://github.com/ahmedelsayed93/Serial-Lab/raw/master/SerialLabSetupV1.0.0.msi)
## Author 
**Ahmed El-Sayed**  
[**ahmed.m.elsayed93@gmail.com**](mailto:ahmed.m.elsayed93@gmail.com)  
## License
Licensed under the **GNU GPLv3**  
**Icon** is designed by [**Freepik**](www.freepik.com) from [**Flaticon**](www.flaticon.com)
