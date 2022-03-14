# mdf
Convert multiple s2p files to mdf format

```
./mdf [--unique] --var-(literal|code) 'var_name=MODEL-(...).s2p' [--var ...] file1.s2p [file2...] > mymdf.mdf
   --var-code specifies the variable to be assigned and a regular
	expression to match the capacitance code (or other unit): NNX or NRN. X is
	the exponent, N is a numeric value. A-Z is typically used by
	manufacturers to indicate the decimal point.

	Above (...) matches the code or literal to be placed in the MDF variable.  If
	a capacitor code is 111 then it will calculate 11*10^1 == 110 pF.
	A code of 1N4 or 14N would be 1.4 or 14.0, respectively.
	
	The --var-literal version does not parse the code.
	
	--unique will choose only the first matching code if multiple of the same code are found.
		
	Output is written to STDOUT so redirect into your .mdf file
```
