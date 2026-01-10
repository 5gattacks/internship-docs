# Configuration

## gnb.conf
- Here you can configure the frequencies used by the gNB. For instance, for DL frequencies, two of the known values for band `78` are:
    - `absoluteFrequencySSB = 642816` and `dl_absoluteFrequencyPointA = 641544`
    - `absoluteFrequencySSB = 641280` and `dl_absoluteFrequencyPointA = 640008`
- At RUs, you can specify which USRP to use by adding `sdr_addrs = "serial=8002816"`


## sib8.conf
- Don't put any space before or after `=`
- Line should end with `;`
- `messageIdentifier`: 
	- `1112`: Presidential Alert
	- `1113`: Extreme Alert
	- `1115`: Severe Alert
- `serialNumber`:
	- `3FF1`: you can just change the last number. 
	- This is useful while testing with Samsung as it store the serial and don't show the alert until new serial number is sent.
- `dataCodingScheme`:
	- `01`: GSM-7
	- `11`: UCS2
- `text`:
	- This is the alert message.
	- Use `|` for new line instead of  `\n`.
- `lang`: 
	- Language indicator in UCS2, encoded using GSM 7-bit
	- Arabic: `ar` -> `6139` 
	- English: `en` -> `6537`
	- You can send both languages in a same message.
	- This means nothing when you use GSM-7 coding scheme.

