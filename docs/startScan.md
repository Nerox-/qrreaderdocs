## .startScan(params)

Launches the camera and starts scanning for barcodes and QR codes.

*Parameters:*

* params
<small>__[Table](https://docs.coronalabs.com/api/library/table/index.html)__ Contains parameters for the call.</small>

title<sub>optional</sub>
<small>__[String](https://docs.coronalabs.com/api/type/String.html)__ Title text.<br>Default is `SCAN BARCODE`</small><br>
useFrontCamera<sub>optional</sub>
<small>__[Boolean](https://docs.coronalabs.com/api/type/Boolean.html)__ Set to `true` to use the front camera if it’s available. If it’s not available, the rear camera will be used.<br>Default is `false`.</small><br>
beepEnabled<sub>optional</sub>
<small>__[Boolean](https://docs.coronalabs.com/api/type/Boolean.html)__ Set to `true` to hear a beep sound when the barcode/qrcode is scanned.<br>Default is `false`.</small><br>
barcodeFormat<sub>optional</sub>
<small>__[String](https://docs.coronalabs.com/api/type/String.html)__ scan barcode format.<br>Default is `all`<br>
**Available formats:**<br>
**"all"**: includes all barcode formats.<br>
**"one-d"**: includes 'UPC_A', 'UPC_E', 'EAN_8', 'EAN_13', 'CODE_39', 'CODE_93', 'CODE_128', 'ITF', 'RSS_14', 'RSS_EXPANDED' <br>
**"qrcode"**: includes 'QR_CODE' <br>
**"product"**: includes 'UPC_A', 'UPC_E', 'EAN_8', 'EAN_13', 'RSS_14' <br>
**"data-matrix"**: includes 'DATA_MATRIX' <br>
</small><br>
onScanComplete<sub>optional</sub>
<small>__[Listener](https://docs.coronalabs.com/api/type/Listener.html)__ Listener which receives the [scan complete event](onScanComplete.md) when the scanning has been completed.</small><br>