# Tangled up in Unicode

This module provides access to character properties for all Unicode characters, from the Unicode Character Database (UCD) .
This module provides an alternative to Python's standard library [`unicodedata`](https://docs.python.org/3/library/unicodedata.html).
`Tangled up in Unicode` provides three main benefits compared to the standard library:
- The [latest version](http://www.unicode.org/versions/latest/) of the Unicode database is used.
- Adds human-readable class names (Property value aliases).
- Extends the properties to use more potential of the database.

Please read the [docs](#) for details.


## Example

The default lookup in `unicodedata` for `$`:

| Property 					| Value 		 	|
|---------------------------|-------------------|
| Name	   					| Dollar Sign 		|
| Category (Short)			| Sc 		 		|
| Bidirectional (Short) 	| ET 				|
| Combining					| 0					|
| Mirrored					| 0					|
| East Asian Width (Short)	| Na				|
| Decomposition				| 					|

Extra information provided by this package

| Property 						| Value 		 		|
|-------------------------------|-----------------------|
| Category Alias (Long)			| Currency_Symbol		|
| Bidirectional Alias (Long)	| European_Terminator	|
| East Asian Width Alias (Long)	| Narrow				|
| Script (Long)					| Common				|
| Script (Short)				| Zyyy					|
| Block (Long)					| Basic_Latin			|
| Block (Short)					| ASCII					|
| PropList						| Pattern_Syntax		|
| Uppercase Character			|						|
| Lowercase Character			|						|
| Titlecase	Character			|						|


## Properties comparison

| Property					| `tangled-up-in-unicode`			| `unicodedata` 		|
|---------------------------|-------------------------------|-----------------------|
| Name						| &#9745;						| &#9745;  				|
| Decimal					| &#9745;						| &#9745;  				|
| Digit						| &#9745;						| &#9745;  				|
| Numeric					| &#9745;						| &#9745;  				|
| Combining           		| &#9745; + alias				| &#9745;  				|
| Mirrored           		| &#9745;						| &#9745;  				|
| Decomposition        		| &#9745;						| &#9745;  				|
| Category					| &#9745; + alias				| &#9745;  				|
| Bidirectional				| &#9745; + alias				| &#9745;  				|
| East Asian Width			| &#9745; + alias				| &#9745;  				|
| Script					| &#9745; + alias				| -  					|
| Block						| &#9745; + alias				| -  					|
| Age						| &#9745; + alias				| -  					|
| Binary Property Values 	| &#9745;						| -  					|
| Version					| 12.0.1 ([latest](http://www.unicode.org/versions/latest/))				| 11.0.0				|
_Table 1: presence of properties is denoted by &#9745; (Unicode Character 'BALLOT BOX WITH CHECK' (U+2611))._		

## Usage

```python
import tangled_up_in_unicode as unicodedata
```

The package can be installed via pip:

```
pip install tangled-up-in-unicode
```

## Performance

The module is written in Python. 
It can be compiled with Cython to gain [competitive performance](# "Meaning the null hypothesis of the two libraries having the same average runtime could not be rejected.") with the native library.

## Unsupported features

Some of the features in `unicodedata` are not supported. 

| Feature				| `tangled-up-in-unicode`		| `unicodedata` 		|
|-----------------------|-------------------------------|-----------------------|
| lookup	           	| -								| &#9745;  				|
| normalize           	| -								| &#9745;  				|
| ucd_3_2_0      		| -								| &#9745;  				|

## Acknowledgements
Where possible, code and documentation of the original module are used.
This repository is part of the Dylan Profiling project.