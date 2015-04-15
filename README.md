### X2Bus Energy Board
  
**Description**  
The MAX78630+PPM is an energy measurement processor for polyphase power-monitoring systems. It is designed for real-time monitoring for a variety of typical three-phase configurations in industrial applications. The MAX78630+PPM provides up to six analog inputs for interfacing to voltage and current sensors. Scaled voltages from the sensors are fed to the single converter front-end using a high-resolution delta-sigma converter. Supported current sensors include current transformers (CTs), Rogowski coils, and resistive shunts.  
  
In this Arduino Library we can read all data of energy parameters.

## Read RMS Voltage

The EnergyBoard reports true RMS measurements for each input. An RMS value is 
obtained by performing the sum of the squares of instantaneous values over a time 
interval (accumulation interval) and then performing a square root of the result 
after dividing by the number of samples in the interval.
	
	Syntax
	EnergyBoard.Voltage(char phase);
	
	Parameters
	phase : Phase of voltage (char) for example 'R', 'S', 'T'
	
	Returns
	Voltage value in float data type
	
	Example
	Float Voltage_R = EnergyBoard.Voltage('R');
	
  
| Data Type | Function                    | Description                               |
|-----------|-----------------------------|-------------------------------------------|
| float     | Voltage(char phase);		  | Read Voltage at selected phase            |
| float     | Current(char phase);		  | Read Current at selected phase            |
| float     | ActivePower(char phase);	  | Read Active Power at selected phase       |
| float     | ReactivePower(char phase);  | Read Re Active Power at selected phase    |
| float     | ApparentPower(char phase);  | Read Apparent Power at selected phase     |
| float     | PowerFactor(char phase);	  | Read Power Factor at selected phase       |
| float     | Frequency(void);			  | Read Frequency of system                  |

## Licences

All source code is licensed under the [MIT License](http://opensource.org/licenses/MIT)

	Copyright (c) 2015 X2bus <info@x2bus.com>
	 
	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is furnished
	to do so, subject to the following conditions:
	 
	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.
	 
	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
	THE SOFTWARE.
