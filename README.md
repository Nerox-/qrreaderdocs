# Welcome to QR Reader!

The QR Reader plugin lets you scan QR Codes and other barcodes in your Corona app.

Supported platforms: Android 4.0.3+.

The latest version requires Corona 2017.3068 or later.


## Project Settings
```lua
	settings = {
		plugins = {
			['plugin.qrreader'] = {
				publisherId = 'com.andrewwahid'
			}
		}
	}
```


## Functions

 ***startScan*** (params)

	> opens device's camera and starts scanning for barcodes

 + **params** <sub><sub>required</sub></sub>
<small> _[Table](https://docs.coronalabs.com/api/type/Table.html)._ Contains parameters for the call.</small>

> 	 **title**
> 	<small>_[String](https://docs.coronalabs.com/api/type/String.html)._ Title text.</small>
> 
> 	 **useFrontCamera** <sub><sub>optional</sub></sub>
> 	<small>[Boolean](https://docs.coronalabs.com/api/type/Boolean.html). Set to `true` to use the front camera if it’s available. If it’s not available, the rear camera will be used. 
> <small>Default is `false`.</small></small>
> 
> 	**beepEnabled**<sub><sub>optional</sub></sub>
>   <small>_[Boolean](https://docs.coronalabs.com/api/type/Boolean.html)._ Set to `true` to hear a beep sound when the barcode/qrcode is scanned.
>   <small>Default is `false`.</small></small>
> 
> 	**barcodeFormat**<sub><sub>optional</sub></sub>
> 	<small>[String](https://docs.coronalabs.com/api/type/String.html). scan barcode format. 	
>   **Available formats:** 	
>   **"all"**: <small>includes all barcode formats. </small>
>   **"one-d"**: <small>includes 'UPC_A', 'UPC_E', 'EAN_8', 'EAN_13', 'CODE_39', 'CODE_93', 'CODE_128', 'ITF', 'RSS_14', 'RSS_EXPANDED'</small> 	
>   **"qrcode"**: <small>includes 'QR_CODE'</small> 
>   **"product"**: <small>includes 'UPC_A', 'UPC_E', 'EAN_8', 'EAN_13', 'RSS_14'</small> 	
>   **"data-matrix"**: <small>includes 'DATA_MATRIX'</small> </small> 	
> 
> 	**onScanResult** <sub><sub>optional</sub></sub> 
>	<small> _[Listener](https://docs.coronalabs.com/api/type/Listener.html)._ Listener which receives the event when the scanning has been completed or cancelled. 	
> 	<small>**event.state: "completed" or "cancelled"
> 	event.isError: true or false 
>   event.result: decoded data from a QR
> 	code or a barcode.**</small></small>

##  Example

```lua
   qrscanner.startScan( {
   		onScanResult = function(event) 
   			print(event.state) -- "completed" or "cancelled"
   			print(tostring(event.isError)) -- "true" or "false"
   			print(event.result) -- scanned data
   		end,
   		title = "SCAN QR CODE",
   		useFrontCamera = false,
   		barcodeFormat = "qrcode",
   		beepEnabled = true,
   	} )
 ```

