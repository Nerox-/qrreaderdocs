## onScanComplete(event)

Event recieved after Barcode/QR scanning is completed.

***Properties:***

* event.name<br>
<small>__[String](https://docs.coronalabs.com/api/type/String.html)__ "onScanComplete".</small>

* event.isError<br>
<small>__[Boolean](https://docs.coronalabs.com/api/type/Boolean.html)__ If an error occurred, this is 'true', otherwise 'false'.</small>

* event.result<br>
<small>__[String](https://docs.coronalabs.com/api/type/String.html)__ decoded data from a QR code or a barcode.</small>

* event.state<br>
<small>__[String](https://docs.coronalabs.com/api/type/String.html)__ "completed" or "cancelled".</small>
